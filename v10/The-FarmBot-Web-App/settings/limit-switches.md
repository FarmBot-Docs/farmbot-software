---
title: "Limit Switches"
slug: "limit-switches"
description: "[Open these settings in the app](https://my.farm.bot/app/designer/settings?highlight=limit_switches)"
---

**Limit switches**, are small switches or sensors that are used to tell a machine if it has reached an end position (home or an axis maximum).

Because both rotary encoders and stall detecting stepper drivers can [detect the home position and axis maximums](../../FarmBot-OS/arduino-firmware/stall-detection.md) as well, they make the use of limit switches **largely unnecessary**. That's why limit switches are not included with our kits.

Nonetheless, our firmware and electronics boards do support the use of limit switches for the DIY builders who need to be able to home their devices but do not want to pay for rotary encoders and the full stall detection and position tracking capabilities that they provide.

![Screen Shot 2020-06-12 at 11.33.49 AM.png](_images/Screen_Shot_2020-06-12_at_11.33.49_AM.png)

# Enable limit switches
If using limit switches instead of rotary encoders, enable them here. If you do not have limit switches hooked up, do not enable this setting.

# Swap limit switches
This switches the zero end of an axis to the other end of the axis. This allows you to set your home (0, 0, 0) position to any of the eight corners of FarmBot's working volume. You might need to use this setting in combination with **INVERT MOTORS**, **INVERT ENCODERS**, and **NEGATIVE COORDINATES ONLY** to set your FarmBot coordinate system exactly how you want it.

# Invert limit switches
This inverts limit switch operation from normally open (NC) to normally closed (NC).
