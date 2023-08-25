---
title: "Use the FarmBot Genesis Rotary Tool"
slug: "use-the-rotary-tool"
description: "**In this guide:** See how to use the FarmBot Genesis rotary tool"
---

FarmBot Genesis v1.6+ kits include a **[rotary tool](https://genesis.farm.bot/docs/rotary-tool)** featuring a 24 volt DC motor, interchangeable implements, and an adjustable motor angle allowing FarmBot to perform light duty weed whacking, soil surface milling, and drilling operations.

{% include youtube.html id="f_GqlMAMWPk" %}

![rotary tool](_images/rotary_tool.png)

# Controlling the rotary tool

The rotary tool's motor can be activated using a peripheral pin:

- Pin 2 is used for forward operation
- Pin 3 is used for reverse operation

These pins can be used in either `Analog` or `Digital` modes, where a digital ON will result in full-speed operation while an analog value between 0 and 255 will result in a proportional speed from 0 to 100%.

You can set Pin 2 or Pin 3's mode and value in several ways:

## Manual control

To manually control the rotary tool, open up the [peripherals tab](../../app/controls/peripherals.md) of the controls popup. From there, you can configure Pins 2 and 3 to be in `Analog` or `Digital` mode and manually control them using the toggle switches or sliders.

{%
include callout.html
type="info"
content="Activating both Pin 2 and Pin 3 at the same time will result in the rotary tool not moving. While this will not cause any damage, it is not recommended."
%}

![rotary tool manual control](_images/rotary_tool_manual_control.png)

## Sequence commands

You can also control the rotary tool programatically using the following sequence commands:

- <span class="fb-step fb-write-pin">CONTROL PERIPHERAL</span>
- <span class="fb-step fb-write-pin">TOGGLE PERIPHERAL</span> (only toggles between Digital ON and OFF)
- <span class="fb-step fb-if-statement">LUA</span> using custom code. See our [developer documentation](http://lua.farm.bot/) for additional details.

{% include gallery.html images='
![rotary tool control peripheral](_images/rotary_tool_control_peripheral.png)
![rotary tool toggle peripheral](_images/rotary_tool_toggle_peripheral.png)
![rotary tool lua](_images/rotary_tool_lua.png)
' %}
