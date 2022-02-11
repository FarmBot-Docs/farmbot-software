---
title: "Use FarmBot's Buttons"
slug: "use-farmbots-buttons"
description: "**In this guide:** See examples for how to use FarmBot's buttons"
---

* toc
{:toc}

FarmBot Genesis v1.4+ kits include five **push buttons** on top of the electronics box. Two of these buttons are reserved for triggering <span class="fb-button fb-red">E-STOP</span> and <span class="fb-button fb-yellow">UNLOCK</span> actions while the other three buttons are user customizable. In this guide we'll show you how you can configure your buttons to:

[:flashlight: Toggle lights for nighttime harvesting](#example-1-toggle-lights-for-nighttime-harvesting)

[:sweat_drops: Wash your bounty and your hands](#example-2-wash-your-bounty-and-your-hands)

[:arrow_double_up: Get FarmBot out of the way](#example-3-get-farmbot-out-of-the-way)

# Example 1: Toggle lights for nighttime harvesting

A common need for FarmBot owners is to turn lights on for nighttime harvesting. Rather than having to use your phone to log into the app and toggle FarmBot's lights on and off, you can configure one of the push buttons to act as a switch.

## Step 1: Create sequences to turn the lights on and off

Create two sequences, one to turn the lights ON, and one to turn the lights OFF. Each sequence only needs to have one step in it, a <span class="fb-step fb-write-pin">CONTROL PERIPHERAL</span> command for the `Lighting` peripheral.

![lights on sequence](_images/lights_on_sequence.png)



![lights off sequence](_images/lights_off_sequence.png)

## Step 2: Create a sequence to toggle the lights

Make a third sequence with an <span class="fb-step fb-if-statement">IF STATEMENT</span> command that allows FarmBot to determine which of the previous two sequences should be executed when the button is pressed, based on the current state of the lighting peripheral.

If the lighting is currently off (a value of `0`), and the button is pressed, FarmBot should execute the sequence that turns the lighting on. Else, it should turn the lighting off.

![toggle lights sequence](_images/toggle_lights_sequence.png)

## Step 3: Create the pin binding

Create a **[pin binding](../../app/settings/pin-bindings.md)** that binds an available button to your sequence that toggles the lights. Press <span class="fb-button fb-green">SAVE</span> and then try everything out by pressing the button on your FarmBot!

![toggle lights pin binding](_images/toggle_lights_pin_binding.png)

# Example 2: Wash your bounty and your hands

If you've just pulled some fresh carrots out of the ground you may want to wash them off (and your hands) before returning to the kitchen. Luckily, FarmBot can help you out.

## Step 1: Create a water dosing sequence

Create a sequence with the following commands:

**Step 1:** <span class="fb-step fb-write-pin">CONTROL PERIPHERAL</span> to turn the water ON

**Step 2:** <span class="fb-step fb-wait">WAIT</span> for the amount of time you'll need to wash your produce and hands. We recommend choosing a short amount of time, such as 10 seconds. If you need more water after the first dose, you can always press the button again for another dose.

**Step 3:** <span class="fb-step fb-write-pin">CONTROL PERIPHERAL</span> to turn the water OFF

![water dose sequence](_images/water_dose_sequence.png)

## Step 2: Create the pin binding

Create a **[pin binding](../../app/settings/pin-bindings.md)** that binds an available button to your sequence that doses water. Press <span class="fb-button fb-green">SAVE</span> and then try everything out by pressing the button on your FarmBot!

![water dose pin binding](_images/water_dose_pin_binding.png)

# Example 3: Get FarmBot out of the way

Whether you're adding transplants to your garden, harvesting, or repairing your greenhouse, sometimes you just need FarmBot to get out of the way. This example will show you how one button can be configured to always get FarmBot to safely move somewhere else.

## Step 1: Create sequences to move to the home and max positions

Create two sequences, one to <span class="fb-step fb-move-absolute">MOVE TO</span> the home (0, 0, 0) position and one to <span class="fb-step fb-move-absolute">MOVE TO</span> the max X/Y position. In this example our max position is (2800, 1200, 0), but yours will be different.

Both sequences should start with a <span class="fb-step fb-find-home">FIND HOME</span> command set to **FIND Z**. This will raise the Z-axis before the X and Y axes begin moving so FarmBot does not run into any plants.

![move home sequence](_images/move_home_sequence.png)



![move to max sequence](_images/move_to_max_sequence.png)

## Step 2: Create a sequence to move to either the home or the max position

Make a third sequence with an <span class="fb-step fb-if-statement">IF STATEMENT</span> command that allows FarmBot to determine which of the previous two sequences should be executed when the button is pressed, based on the current location of FarmBot.

If FarmBot's current `X position` is in the first half of the bed (a value less than `1400`), and the button is pressed, FarmBot should execute the sequence that moves it to the max position. Else, it should move to the home position.

![move away sequence](_images/move_away_sequence.png)

## Step 3: Create the pin binding

Create a **[pin binding](../../app/settings/pin-bindings.md)** that binds an available button to your sequence that determines where FarmBot should move to. Press <span class="fb-button fb-green">SAVE</span> and then try everything out by pressing the button on your FarmBot!

![move away pin binding](_images/move_away_pin_binding.png)

