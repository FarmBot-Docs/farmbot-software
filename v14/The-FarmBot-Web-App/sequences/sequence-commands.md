---
title: "Sequence Commands"
slug: "sequence-commands"
description: "Categories of commands you can use in a sequence"
---

The next pages include detailed information for all of the commands you can use in a sequence, organized by category. When using the web app, hover over the <i class='fa fa-question-circle'></i> icon in the top right of any sequence step to view quick-access usage information.

|Movements||
|---------||
|<span class="fb-step fb-move">[Move](sequence-commands/movements.md#move)</span>|Move FarmBot's X, Y, and Z axes to various locations
|<span class="fb-step fb-move">[Find home](sequence-commands/movements.md#find-home)</span>|Use FarmBot's stall detection features to find the home position
|<span class="fb-step fb-move">[Set home](sequence-commands/movements.md#set-home)</span>|Manually set the home position
|<span class="fb-step fb-move">[Find axis length](sequence-commands/movements.md#find-axis-length)</span>|Use FarmBot's stall detection features to find the length of an axis
|<span class="fb-step fb-move">[Control servo](sequence-commands/movements.md#control-servo)</span>|Set the angle of a servo
|**Peripherals and Sensors**|
|<span class="fb-step fb-write-pin">[Control Peripheral](sequence-commands/peripherals-and-sensors.md#control-peripheral)</span>|Control FarmBot's peripherals such as the solenoid valve
|<span class="fb-step fb-write-pin">[Toggle Peripheral](sequence-commands/peripherals-and-sensors.md#toggle-peripheral)</span>|Toggle FarmBot's peripherals
|<span class="fb-step fb-read-pin">[Read Sensor](sequence-commands/peripherals-and-sensors.md#read-sensor)</span>|Read sensors such as the soil moisture sensor
|**Image Processing**|
|<span class="fb-step fb-take-photo">[Take Photo](sequence-commands/image-processing.md#take-photo)</span>|Takes a photo using the FarmBot's camera
|<span class="fb-step fb-run-farmware">[Detect Weeds](sequence-commands/image-processing.md#detect-weeds)</span>|Takes a photo and detects any weeds in view
|<span class="fb-step fb-run-farmware">[Measure Soil Height](sequence-commands/image-processing.md#measure-soil-height)</span>|Takes several photos and calculates the average height of the soil in view
|**Logic**|
|<span class="fb-step fb-wait">[Wait](sequence-commands/logic.md#wait)</span>|Pauses sequence execution for the specified amount of time
|<span class="fb-step fb-if-statement">[If Statement](sequence-commands/logic.md#if-statement)</span>|Evaluates a condition and then executes a subsequence
|<span class="fb-step fb-execute">[Execute](sequence-commands/logic.md#execute)</span>|Executes a subsequence
|<span class="fb-step fb-mark-as">[Mark as](sequence-commands/logic.md#mark-as)</span>|Updates the properties of plants, points, weeds, and more
|<span class="fb-step fb-send-message">[Send Message](sequence-commands/logic.md#send-message)</span>|Sends a message to any number of available channels such as email
|<span class="fb-step fb-e-stop">[E-stop](sequence-commands/logic.md#e-stop)</span>|Emergency stops FarmBot
|<span class="fb-step fb-reboot">[Reboot](sequence-commands/logic.md#reboot)</span>|Reboots FarmBot
|<span class="fb-step fb-shutdown">[Shutdown](sequence-commands/logic.md#shutdown)</span>|Shuts FarmBot down
|**Advanced**|
|<span class="fb-step fb-assertion">[Assertion](sequence-commands/advanced.md#assertion)</span>|Tests if a condition is true or false for automated testing purposes
|<span class="fb-step fb-lua">[Lua](sequence-commands/advanced.md#lua)</span>|Execute Lua code fragments for custom advanced functionality

# What's next?

 * [Movement Commands](sequence-commands/movements.md)
 * [Peripheral and Sensor Commands](sequence-commands/peripherals-and-sensors.md)
 * [Image Processing Commands](sequence-commands/image-processing.md)
 * [Logic Commands](sequence-commands/logic.md)
 * [Advanced Sequence Commands](sequence-commands/advanced.md)
