---
title: "Endstops"
slug: "endstops"
description: "Hardware for finding home and axis maximums"
---

* toc
{:toc}

**Endstops**, sometimes called **limit switches**, are small switches or sensors that are used to tell a machine if it has reached an end position (home or an axis maximum).

Because both rotary encoders and back-current sensing stepper drivers can [detect the home position and axis maximums](stall-detection.md) as well, they make the use of endstops **largely unnecessary**. That's why endstops are not included with our kits.

Nonetheless, our firmware and electronics boards do support the use of endstops for the DIY builders who need to be able to home their devices but do not want to pay for rotary encoders and the full stall detection and position tracking capabilities that they provide.
