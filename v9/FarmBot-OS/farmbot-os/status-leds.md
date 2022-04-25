---
title: "Status LEDs"
slug: "status-leds"
description: "The meaning behind the blinking"
---

# Raspberry Pi LEDs
The Raspberry Pi has two LED lights that convey information about its status.

![RASPBERRY_PI_LIGHTS.jpg](_images/RASPBERRY_PI_LIGHTS.jpg)

## Red (power) LED
Red (power) | Status
:--- | :---
<span class="fa fa-circle led red"></span> (solid red) | Low power - Try a more powerful power supply or a different cable.
<span class="fa fa-sun-o led red"></span> (blinking red) | Low power - Try a more powerful power supply or a different cable.
<span class="fa fa-circle-thin led red"></span>  (off) | No power / low power - Plug in to a 5V, 3A power supply.

## Green (activity) LED

|Green (activity)              |Status                        |
|------------------------------|------------------------------|
|<span class="fa fa-circle led green"></span> (solid green)|Busy working/booting
|<span class="fa fa-sun-o led green"></span> (blinking randomly)|Busy working/booting
|<span class="fa fa-sun-o led green"></span> (blinking consistently)|Network disconnected or emergency stopped - [Configure FarmBot](configurator.md), press <span class="fb-button fb-yellow">UNLOCK</span> in the Web App, or check that the network FarmBot is connected to is online.
|<span class="fa fa-circle-thin led green"></span> (off)|Ready and waiting for the next task

# Electronics box LEDs
In addition to the LEDs located on the Raspberry Pi, Genesis v1.4+ kits feature LEDs mounted on top of the electronics box.

![LEDs.png](_images/LEDs.png)

## LED 1 (sync)
This green LED indicates the **sync status** between FarmBot and the web app. It is connected to Raspberry Pi GPIO BCM pin 24.

|Green (sync)                  |Status                        |
|------------------------------|------------------------------|
|<span class="fa fa-circle led green"></span> (solid green)|Synced and ready
|<span class="fa fa-sun-o led green"></span> (blinking slowly)|Needs sync (Will not execute any unsynced events or sequences)
|<span class="fa fa-sun-o led green"></span> (blinking quickly)|Syncing
|<span class="fa fa-circle-thin led green"></span> (off)|Offline - Check the connection status LED

## LED 2 (connection)
This blue LED indicates the **connection status** between FarmBot and the internet and web app. It is connected to Raspberry Pi GPIO BCM pin 25.

|Blue (connection)             |Status                        |
|------------------------------|------------------------------|
|<span class="fa fa-circle led blue"></span> (solid blue)|Connected and working
|<span class="fa fa-sun-o led blue"></span> (blinking slowly)|Needs configuration - [Configure FarmBot](configurator.md), press <span class="fb-button fb-yellow">UNLOCK</span> in the Web App, or check that the network FarmBot is connected to is online.
|<span class="fa fa-circle-thin led blue"></span> (off)|Offline - Check your internet connection.<br><br>If you are connected to the internet but the Blue LED is off, one or more of your ports may be blocked. Get your network administrator to check the ports listed in the [Firewall is blocking network traffic](../../Extras/troubleshooting/connecting-farmbot-to-the-web-app.md#6-firewall-is-blocking-network-traffic) troubleshooting section.

## LED 3 (custom)
This white LED is user controllable via the <span class="fb-step fb-write-pin">Control Peripheral</span> sequence command. It is connected to Raspberry Pi GPIO BCM pin 12.

## LED 4 (custom)
This white LED is user controllable via the <span class="fb-step fb-write-pin">Control Peripheral</span> sequence command. It is connected to Raspberry Pi GPIO BCM pin 13.

# Electronics box buttons
Some kits also include push buttons featuring integrated LED lights.

## E-Stop Button
The **E-Stop Button** (included with all Genesis v1.4+ and Express v1.0+ kits) has a red LED that indicates if FarmBot is <span class="fb-button fb-red">E-STOPPED</span> or not. It is connected to Raspberry Pi GPIO BCM pin 17.

|Red (E-stop)                  |Status                        |
|------------------------------|------------------------------|
|<span class="fa fa-circle led red"></span> (solid red)|Unlocked and ready
|<span class="fa fa-circle-thin led red"></span> (off)|Locked - Check the Button 2 LED status

## Unlock Button
The **Unlock Button** (included with all Genesis v1.4+) has a yellow LED that indicates if FarmBot is <span class="fb-button fb-yellow">UNLOCKED</span> or not. It is connected to Raspberry Pi GPIO BCM pin 23.

|Yellow (unlock)               |Status                        |
|------------------------------|------------------------------|
|<span class="fa fa-sun-o led orange"></span> (blinking)|Locked - When safe to do so, press this button to unlock FarmBot.
|<span class="fa fa-circle-thin led orange"></span> (off)|Unlocked and ready

