---
title: "Rotary Encoders"
slug: "rotary-encoders"
description: "closed-loop feedback control system"
---

* toc
{:toc}


{%
include callout.html
type="warning"
title="Under Development"
content="Full firmware-level support for rotary encoders is coming soon."
%}

Rotary encoders attach to the back of each motor to constantly monitor FarmBot's position.

### Position monitoring enables FarmBot to know when something has gone wrong such as:

* motor not moving due to incorrect speed settings or lack of power
* collision with an object such as dirt on the tracks, plant branches, or animals
* end of axis reached
* person pushing the device to a different location

With rotary encoders, FarmBot can be aware that it has not reached the location intended instead of continuing on in the wrong position and accidentally destroying the whole garden.

Rotary encoders can also be used for device [Calibration and Homing](../Additional-Information/calibration-and-homing.md).

### In the future, rotary encoders could be used to:

* send a notification when something goes wrong
* send a photo of an obstruction such as a fallen branch
* record a path inputted by moving the axes by hand to replay later
