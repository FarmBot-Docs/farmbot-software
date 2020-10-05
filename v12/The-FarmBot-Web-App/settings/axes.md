---
title: "Axes"
slug: "axes"
description: "[Open these settings in the app](https://my.farm.bot/app/designer/settings?highlight=axes)"
---

* toc
{:toc}


![Screen Shot 2020-08-24 at 12.31.36 PM.png](_images/Screen_Shot_2020-08-24_at_12.31.36_PM.png)

# Find home
Finding home instructs FarmBot to find the home (minimum) position by moving towards home until an endstop, rotary encoder, or stepper driver signals that the end of the axis has been reached. Note that **ENCODERS**, **STALL DETECTION**, or **LIMIT SWITCHES** must be <span class="fb-peripheral-on">ON</span> for FarmBot to automatically find home.

Please note that **LIMIT SWITCHES** are not part of the standard FarmBot kit hardware and they typically only used by expert users.  **LIMIT SWITCHES** for CNC devices are switches that are triggered when the CNC device reaches the limit of the track. Please do not enable the  **LIMIT SWITCHES** for your device if you have not specifically installed them on your FarmBot.



![LIMIT_SWITCH.jpg](_images/LIMIT_SWITCH.jpg)

_Example of Limit Switch for CNC devices.  [Model SS-5GL13T  Omeron Electronics]_

To home an axis, click the <span class="fb-button fb-yellow">FIND HOME X</span>, <span class="fb-button fb-yellow">FIND HOME Y</span>, or <span class="fb-button fb-yellow">FIND HOME Z</span> buttons. To home all three axes, you can use the <span class="fb-button fb-gray"><i class='fa fa-home'></i></span> button in the controls widget (assuming that that button is set to its default behavior).

{%
include callout.html
type="info"
title="\"Homing\" is different than \"Going to Home\""
content="Homing is the act of _finding_ the home (zero) position by using endstops or encoders. _Going to Home_ is the act of moving to (0, 0, 0)."
%}

# Set home
Pressing the <span class="fb-button fb-yellow">SET HOME X</span>, <span class="fb-button fb-yellow">SET HOME Y</span>, and <span class="fb-button fb-yellow">SET HOME Z</span> buttons allows you to *manually* set FarmBot's current location as the home position for that axis. This is used for *manually* setting the Home position when **ENCODERS**, **STALL DETECTION**, or **LIMIT SWITCHES** are <span class="fb-peripheral-off">OFF</span>.

However, because stock FarmBots have encoders and stall detecting, it is recommended to instead use the [Homing](#homing) function for *automatically* finding the Home position of each axis and setting that position to zero.

So in general, the Set Zero buttons should not be regularly used because it does not make sense to change your zero position once you have your garden growing, and because all FarmBots should have either encoders or endstops enabled which allows for automatically finding and setting the Home position.

These buttons may come in handy though when playing around with experimental sequences or exploring alternate coordinate system configurations for your FarmBot.

# Find home on boot
Enabling this setting will run a homing command for each axis upon boot. This is most useful for allowing FarmBot to recover and resume operations after a power outage. Note that this requires encoders or endstops to be enabled.

# Stop at home
Enabling software limits for an axis will prevent FarmBot from moving through zero. For example, if an axis is normally moving in positive coordinates, then the software limit will prevent it from moving through zero into negative coordinates. If an axis has **NEGATIVE COORDINATES ONLY** enabled, then it normally moves in negative coordinates and the software limit will prevent it from moving through zero into positive coordinates.

{%
include callout.html
type="success"
title="Recommended"
content="We recommend turning software limits on for all axes so that FarmBot will never try to move through the home (0, 0, 0) position."
%}

# Stop at max
If values are inputted using the **AXIS LENGTH** setting, FarmBot will stop at the axis maximum.

# Negative coordinates only
This setting will allow movements to only occur in negative coordinates for the chosen axis. This is most useful for the z-axis if you want your home position to be at the highest point and for FarmBot to move down into negative coordinates.

# Find axis length
Finding an axis length instructs FarmBot to find the maximum position and then find the minimum (home) position while measuring the distance between the two, which is the length of the axis. Note that **ENCODERS**, **STALL DETECTION**, or **LIMIT SWITCHES** must be <span class="fb-peripheral-on">ON</span> for FarmBot to automatically find an axis length.

Also note that you must enable **STOP AT MAX** for FarmBot to stop at the measured maximum.

{%
include callout.html
type="info"
title=""
content="The speed of finding an axis length is currently determined by the **HOMING SPEED** setting."
%}

# Set axis length
With these inputs you can manually specify the length in mm of each axis. This is useful if you want to limit your FarmBot's movements along an axis with software rather than a physical hardware stop such as a belt clip or an endstop. For example: you may occasionally want to prevent movements at the far end of your garden because you put a seasonal garden gnome there, but you don't want to adjust the belts and belt clips. You must enable **STOP AT MAX** for FarmBot to stop at the values inputted.

{%
include callout.html
type="info"
title="Reminder"
content="The length values of each axis are measured and auto-filled whenever your use the [find axis length](#calibration) function."
%}

