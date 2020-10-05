---
title: "Stall Detection"
slug: "stall-detection"
description: "Hardware that allows FarmBot to detect stalls and find home and axis maximums"
---

* toc
{:toc}

To move around the garden, FarmBot sends electronic pulses to its motors. **Under normal circumstances**, these pulses cause the motors to rotate an exact amount and move FarmBot to exactly where it needs to be.

However, the garden environment is **unpredictable**, and FarmBot cannot always rely on circumstances being normal. For example, if a :tomato: plant grows across the tracks, FarmBot might get stuck on its vines, causing one or more motors to **stall**.

In situations like this, FarmBot needs a way to **detect** the stall so that it can either retry the movement, e-stop, or go back to the home position to reorient itself. If FarmBot had no way of detecting a stall, it would continue operating without realizing its position is incorrect, and potentially destroy the whole garden.

# Rotary encoders
**Rotary encoders** are sensors that can be attached to the back of motors to measure the exact rotation of the motor shafts in real-time. With rotary encoders, FarmBot can detect when a motor has stalled, which could be caused by one of the following reasons:

* A motor is not moving correctly due to unreasonable speed and/or acceleration settings, a lack of power, or another hardware malfunction.
* FarmBot has collided with an object such as plant branches :seedling:, a hand :hand:, or an animal :dog:.
* There is too much resistance or friction for FarmBot to overcome. This could be caused by dirt on the tracks, eccentric spacers that are too tight, belts that are too tight, excessive machine weight, cold temperatures causing cabling and tubing to become stiff, or other factors.
* The end of an axis has been reached during [automatic calibration](../../Extras/how-do-i/calibrate-and-home-farmbot.md#automatic-calibration) or [homing](../../Extras/how-do-i/calibrate-and-home-farmbot.md#homing), or in error.

In addition to detecting stalls, rotary encoders also keep track of FarmBot's position. This even works when FarmBot is idle and you move an axis _by hand_.
