---
title: "Calibration and Homing"
slug: "calibration-and-homing"
description: "Manual and automatic approaches"
---

* toc
{:toc}


# Manual Calibration

1. Move FarmBot to your desired home position
2. Press the <span class="fb-button fb-yellow">ZERO X</span>, <span class="fb-button fb-yellow">ZERO Y</span>, and <span class="fb-button fb-yellow">ZERO Z</span> buttons in the **Hardware** widget on the **Device** page.

FarmBot will now set the chosen location as the origin (also known as `Home`, `Zero`, or `(0, 0, 0)`).

# Automatic Calibration

Run an axis calibration to let FarmBot determine home and the length of the axis. Either **ENABLE ENDSTOPS** or **ENABLE ENCODERS** in the [hardware settings widget](https://software.farmbot.io/docs/device#hardware) must be enabled for the axis to be calibrated.

Use the <span class="fb-button fb-gray">CALIBRATE X</span>, <span class="fb-button fb-gray">CALIBRATE Y</span>, and <span class="fb-button fb-gray">CALIBRATE Z</span> axis buttons in the [hardware settings widget](https://software.farmbot.io/docs/device#hardware) to home and calibrate the length of each axis.

Use the <span class="fb-button fb-gray">HOME X</span>, <span class="fb-button fb-gray">HOME Y</span>, and <span class="fb-button fb-gray">HOME Z</span> buttons in the [hardware settings widget](https://software.farmbot.io/docs/device#hardware) to home each axis.

## Process with rotary encoders (included in FarmBot Genesis kits)

FarmBot moves in the zero direction of the axis until the [rotary encoders](rotary-encoders.md) detects missed motor steps when the axis reaches the end. This location is recorded as zero for the axis. If performing calibration in addition to homing, FarmBot will move the opposite direction from zero and record the distance traveled (length of axis) when the other end is reached.

## Process with end-stops (DIY option if not using rotary encoders)

FarmBot moves in the zero direction of the axis until the end-stop triggers when the axis reaches the end. This location is recorded as zero for the axis. If performing calibration in addition to homing, FarmBot will move the opposite direction from zero and record the distance traveled (length of axis) when the end-stop on the other end is reached.
