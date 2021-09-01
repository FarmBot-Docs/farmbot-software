---
title: "Sequence Commands"
slug: "sequence-commands"
description: "Categories of commands you can use in a sequence"
---

* toc
{:toc}

The next pages include detailed information for all of the commands you can use in a sequence, organized by category. When using the web app, hover over the <i class='fa fa-question-circle'></i> icon in the top right of any sequence step to view quick-access usage information.

|Movements||
|---------||
|<span class="fb-step fb-move">Move</span>|Move FarmBot's X, Y, and Z axes to various locations
|<span class="fb-step fb-move">Find home</span>|Use FarmBot's stall detection features to find the home position
|<span class="fb-step fb-move">Set home</span>|Manually set the home position
|<span class="fb-step fb-move">Find axis length</span>|Use FarmBot's stall detection features to find the length of an axis
|<span class="fb-step fb-move">Control servo</span>|Set the angle of a servo
|**Peripherals and Sensors**|
|<span class="fb-step fb-write-pin">Control Peripheral</span>|Control FarmBot's peripherals such as the solenoid valve
|<span class="fb-step fb-write-pin">Toggle Peripheral</span>|Toggle FarmBot's peripherals
|<span class="fb-step fb-read-pin">Read Sensor</span>|Read sensors such as the soil moisture sensor
|**Image Processing**|
|<span class="fb-step fb-take-photo">Take Photo</span>|Takes a photo using the FarmBot's camera
|<span class="fb-step fb-run-farmware">Detect Weeds</span>|Takes a photo and detects any weeds in view
|<span class="fb-step fb-run-farmware">Measure Soil Height</span>|Takes several photos and calculates the average height of the soil in view
|**Logic**|
|<span class="fb-step fb-wait">Wait</span>|Pauses sequence execution for the specified amount of time
|<span class="fb-step fb-if-statement">If Statement</span>|Evaluates a condition and then executes a subsequence
|<span class="fb-step fb-execute">Execute</span>|Executes a subsequence
|<span class="fb-step fb-mark-as">Mark as</span>|Updates the properties of plants, points, weeds, and more
|<span class="fb-step fb-send-message">Send Message</span>|Sends a message to any number of available channels such as email
|<span class="fb-step fb-e-stop">E-stop</span>|Emergency stops FarmBot
|<span class="fb-step fb-reboot">Reboot</span>|Reboots FarmBot
|<span class="fb-step fb-shutdown">Shutdown</span>|Shuts FarmBot down
|**Advanced**|
|<span class="fb-step fb-assertion">Assertion</span>|Tests if a condition is true or false for automated testing purposes
|<span class="fb-step fb-lua">Lua</span>|Execute Lua code fragments for custom advanced functionality

# What's next?

 * [Movement Commands](sequence-commands/movements.md)
 * [Peripheral and Sensor Commands](sequence-commands/peripherals-and-sensors.md)
 * [Image Processing Commands](sequence-commands/image-processing.md)
 * [Logic Commands](sequence-commands/logic.md)
 * [Advanced Sequence Commands](sequence-commands/advanced.md)
