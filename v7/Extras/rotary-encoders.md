---
title: "Rotary Encoders"
slug: "rotary-encoders"
excerpt: "These components provide FarmBot a closed-loop feedback control system"
type: "link"
link_url: "https://software.farm.bot/docs/stall-detection"
---

* toc
{:toc}

Rotary encoders attached to the back of each motor constantly monitor FarmBot's position. This enables FarmBot to know when:

* a motor is not moving due to incorrect speed settings or lack of power.
* it has collided with an object such as dirt on the tracks, plant branches, or animals.
* the end of an axis has been reached during [Automatic Calibration and Homing](calibration-and-homing.md) or in error.
* someone is physically pushing the device to a different location.

With rotary encoders, FarmBot can be aware that it has not reached the intended location instead of continuing in the wrong position and accidentally destroying the whole garden.

In the future, rotary encoders could be used to:

* send a notification when something goes wrong.
* send a photo of an obstruction such as a fallen branch.
* record a path inputted by moving the axes by hand to replay later.
