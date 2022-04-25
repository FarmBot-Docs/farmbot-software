---
title: "Calibrate and Home FarmBot"
slug: "calibrate-and-home-farmbot"
description: "**In this guide:** Learn how to home and calibrate FarmBot"
---

Accurate position tracking is imperative for FarmBot to sow seeds one day and return to water the plants week after week. To keep track of its location within the garden coordinate system, FarmBot must:

  * Base all movements off a fixed **home position**, also known as the **origin**, or **(0, 0, 0)**.
  * Keep track of every movement so FarmBot always knows its **current position**.
  * Detect when a motor has **stalled** due to debris, hardware malfunction, or user error.
  * Know all three **axis lengths**, so FarmBot does not try to move farther than allowed.

# Homing
**Homing** is the process that will let FarmBot know where the **home position** is located. It is recommended to find the home position regularly:

  * After powering up FarmBot
  * After any kind of movement error
  * After moving FarmBot by hand
  * At the start of long-running sequences
  * At the start of any sequences that require a high degree of precision such as a tool mounting sequence

Homing can be performed automatically or manually. **Automatic homing** utilizes special hardware to signal to FarmBot when the home position has been reached. **Manual homing** allows you to set the home position for each axis anywhere you want.

## Automatic homing

{%
include callout.html
type="info"
title=""
content="**ENCODERS**, **STALL DETECTION**, or **ENDSTOPS** must be enabled for FarmBot to automatically find the home position. See the [how it works](#how-it-works) section below for more information."
%}

Instruct FarmBot to automatically find the home position on a regular basis by using the <span class="fb-step fb-find-home">FIND HOME</span> command in a sequence. This is recommended at the start of long-running sequences and sequences that require a high degree of precision.

Alternatively you can use the <span class="fb-button fb-yellow">FIND HOME X</span>, <span class="fb-button fb-yellow">FIND HOME Y</span>, and <span class="fb-button fb-yellow">FIND HOME Z</span> buttons in the settings panel to have FarmBot find home whenever you wish, or the <span class="fb-button fb-gray"><i class='fa fa-home'></i></span> button on the controls page to perform homing for all three axes in the order Z, Y, X. This is recommended after powering up FarmBot, any kind of movement error, or after moving FarmBot by hand.

## Manual homing
1. Move FarmBot to the desired home position with the manual controls or by hand.
2. Press the <span class="fb-button fb-yellow">ZERO X</span>, <span class="fb-button fb-yellow">ZERO Y</span>, and <span class="fb-button fb-yellow">ZERO Z</span> buttons in the settings panel to instruct FarmBot to set the chosen location as the home position for that axis.

# Calibration
**Calibration** is the process that will let FarmBot know **the length of an axis**. It is recommended to calibrate FarmBot after any hardware changes that affect the length of an axis:

* After assembling your FarmBot
* After adjusting belts or hardstops
* After making any other adjustment that may change the distance FarmBot can travel along any axis

Calibration can be performed automatically or manually. **Automatic calibration** utilizes special hardware to signal to FarmBot when the maximum and minimum (home) positions along an axis have been reached. **Manual calibration** allows you to type in the length of an axis.

## Automatic calibration

{%
include callout.html
type="info"
title=""
content="**ENCODERS**, **STALL DETECTION**, or **ENDSTOPS** must be enabled for FarmBot to automatically calibrate. See the [how it works](#how-it-works) section below for more information."
%}

Instruct FarmBot to automatically calibrate an axis with the <span class="fb-button fb-yellow">CALIBRATE X</span>, <span class="fb-button fb-yellow">CALIBRATE Y</span>, and <span class="fb-button fb-yellow">CALIBRATE Z</span> buttons in the settings panel. FarmBot will first find the maximum position of an axis and then find the minimum (home) position, and measure the distance in millimeters between the two. FarmBot will then update the **AXIS LENGTH** setting.

You may also automatically calibrate FarmBot on a regular basis by using the <span class="fb-step fb-move-absolute">CALIBRATE</span> command in a sequence. However, this is generally not necessary because axis lengths do not change on a regular basis.

## Manual calibration

You can manually set the **AXIS LENGTH** for any axis by typing in a custom value. This can be useful if you would like to shorten an axis via software instead of using a hardware hardstop.

# How it works

Automatic homing and automatic calibration utilize special hardware to signal to FarmBot when an end location (an axis maximum or the home position) has been reached. There are three types of hardware supported by different FarmBot models that serve this purpose:

## Rotary encoders

FarmBot Genesis kits include **rotary encoders** on each motor that monitor how much the motor shafts have rotated. Whenever FarmBot reaches a hardware hardstop located at an axis end, the motors will stall, and the rotary encoders will signal to FarmBot that the axis end has been reached.

{%
include callout.html
type="info"
title=""
content="See the [stall detection](../../FarmBot-OS/arduino-firmware/stall-detection.md) page for more information."
%}

## Back-current sensing stepper drivers

FarmBot Express kits include **back-current sensing stepper drivers** that can detect when a motor has stalled. Whenever FarmBot reaches a hardware hardstop located at an axis end, the motors will stall, and the stepper drivers will signal to FarmBot that the axis end has been reached.

{%
include callout.html
type="info"
title=""
content="See the [stall detection](../../FarmBot-OS/arduino-firmware/stall-detection.md) page for more information."
%}

## Endstop limit switches

DIY FarmBot builders may use **endstop limit switches** which are small buttons that can be positioned at axis end locations. Whenever FarmBot reaches an end location, it will press the button, which creates a signal indicating the axis end has been reached.

# Troubleshooting

It is possible for automatic homing and automatic calibration to provide inaccurate results, or for FarmBot's position to be lost. If you are having trouble, try to identify the underlying cause and fix it. Here are some common situations that may occur:

  * Debris or other factors may cause FarmBot to incorrectly identify a location as an end position. For example, if a tree branch falls onto FarmBot's tracks and prevents it from reaching the true home position, FarmBot may incorrectly identify the position where it stalls against the tree branch as the home position. Ensure there is no debris preventing FarmBot from moving along any axis.
  * A misconfiguration of some motor settings, such as **STEPS PER MM**, **MICROSTEPS PER STEP**, or **ENCODER SCALING** can make FarmBot think it is traveling more or less distance than it actually is. This would result in incorrect axis length measurements and incorrect position tracking. Review your settings to ensure they are correct for your hardware.
  * Motor settings that are too fast or accelerate too quickly, or a **MOTOR CURRENT** that is too extreme can cause back-current detecting stepper drivers (used by FarmBot Express) to incorrectly detect stalls. Do not set the motor current too much more or less than the default value.
  * Moving a FarmBot by hand that does not have rotary encoders enabled will change the true position without FarmBot knowing it. To prevent accidental movements, consider enabling **ALWAYS POWER MOTORS**.
