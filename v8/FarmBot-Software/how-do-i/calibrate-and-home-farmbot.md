---
title: "Calibrate and Home FarmBot"
slug: "calibrate-and-home-farmbot"
description: "Manual and automatic approaches"
---


# Manual calibration

1. Move FarmBot to the desired home position.
2. Press the <span class="fb-button fb-yellow">ZERO X</span>, <span class="fb-button fb-yellow">ZERO Y</span>, and <span class="fb-button fb-yellow">ZERO Z</span> buttons in the [hardware settings widget](../../Web-App/device/hardware-settings.md).

FarmBot will now set the chosen location as the origin (also known as `Home`, `Zero`, or `(0, 0, 0)`).

# Automatic calibration

Run an axis calibration to have FarmBot determine the home position and the length of the axis.

{%
include callout.html
type="info"
title=""
content="Either endstops or encoders must be enabled in the [hardware settings widget](../../Web-App/device/hardware-settings.md) for an axis to be automatically calibrated. See the [how it works](#how-it-works) section below for more information."
%}

Use the <span class="fb-button fb-gray">CALIBRATE X</span>, <span class="fb-button fb-gray">CALIBRATE Y</span>, and <span class="fb-button fb-gray">CALIBRATE Z</span> buttons in the [hardware settings widget](../../Web-App/device/hardware-settings.md) to home and calibrate the length of each axis.

# Homing



{%
include callout.html
type="info"
title=""
content="Either endstops or encoders must be enabled in the [hardware settings widget](../../Web-App/device/hardware-settings.md) for FarmBot to find the home position. See the [how it works](#how-it-works) section below for more information."
%}

Use the <span class="fb-button fb-gray">HOME X</span>, <span class="fb-button fb-gray">HOME Y</span>, and <span class="fb-button fb-gray">HOME Z</span> buttons in the [hardware settings widget](../../Web-App/device/hardware-settings.md) to find home for each axis.

# How it works

There are three mechanisms by which automatic calibration and homing can work:

## With rotary encoders or back-current sensing stepper drivers (included in FarmBot kits)
FarmBot moves in the zero direction of the axis until either the [rotary encoders](../../Device/arduino-firmware/stall-detection.md#rotary-encoders) or [stepper drivers](../../Device/arduino-firmware/stall-detection.md#back-current-sensing-stepper-drivers) detect missed motor steps when the axis reaches the end. This location is recorded as zero for the axis. If performing calibration in addition to homing, FarmBot will move the opposite direction from zero and record the distance traveled (length of axis) when the other end is reached, and then move back home.

## With end-stops (DIY option)
FarmBot moves in the zero direction of the axis until the end-stop triggers when the axis reaches the end. This location is recorded as zero for the axis. If performing calibration in addition to homing, FarmBot will move the opposite direction from zero and record the distance traveled (length of axis) when the end-stop on the other end is reached, and then move back home.
