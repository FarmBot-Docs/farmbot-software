---
title: "Movement Commands"
slug: "movements"
description: "Move FarmBot's motors"
---

# Move

The <span class="fb-step fb-move">Move</span> command instructs FarmBot to move to a new location. To use this command, first choose a **LOCATION**  from the dropdown. Options include:

  * Custom coordinates
  * Offset from current location
  * Location variables
  * Tool and seed container locations
  * Plant locations
  * Map points
  * Weed locations

## Custom coordinates

When choosing the **custom coordinates** option, three input fields will be revealed allowing you to specify the exact **X, Y, Z** coordinates you want FarmBot to move to.

![move to custom coordinates](_images/move_to_custom_coordinates.png)

## Offset from current location

When choosing the **offset from current location** option, three input fields will be revealed allowing you to specify the **OFFSET** amount you want FarmBot to move to.

![move to offset](_images/move_to_offset.png)

## Location variables

When choosing **variable - add new**, a variable form will be added to the sequence header. Upon selecting a variable value in the sequence header, the dropdown selections in all <span class="fb-step fb-move">Move</span> steps set to that variable will be updated. See the [variables](../variables.md) documentation for more information.

![location variable](_images/location_variable.png)

## Other locations

When choosing a **tool or seed container location**, a **plant location**, a **map point**, or a **weed location**, those resources will then become _in-use_, meaning that they cannot be deleted until you remove them from your sequence. If you update their coordinates, your sequence steps will be automatically updated.

![move to location](_images/move_to_location.png)

{%
include callout.html
type="warning"
title="Be careful when moving to tools or seed containers"
content="Under most circumstances you will need to mount a tool or pick up a seed from a seed container in **multiple steps**. First, you should move to the tool or seed container with a **positive z-axis offset**. This will allow FarmBot to then descend onto the tool or into the seed container from above in a second step (with no z-offset).

If you try to move to a location to mount a tool or pick up a seed in one step, you risk the z-axis traveling too low too quickly and the FarmBot crashing into the tool and/or bending a seed injection needle."
%}

## Advanced options

Within the **[+]** dropdown, you will find several options to modify the base **LOCATION** and several options for changing how FarmBot performs the movement. By default, the app will only load the **[+]** options in an open state if you've changed any of options from the default values. If you would like the **[+]** options to always load in an open state, set **OPEN OPTIONS BY DEFAULT** to <span class="fb-peripheral-on">YES</span> from the <i class='fa fa-gear'></i> menu in the sequence header.

![move to advanced options](_images/move_to_advanced_options.png)

### Override

**OVERRIDE** allows you to override the X, Y, and/or Z values from the **LOCATION** field with new values. You may type in a custom coordinate, a formula, or disable an axis entirely. The Z axis override dropdown also includes special **[Safe height](../../settings/axes.md#safe-height)** and [Soil height](../../settings/axes.md#fallback-soil-height) options.

{%
include callout.html
type="info"
title=""
content="If you choose custom coordinates for the **LOCATION** field, **OVERRIDE** will appear as **X, Y, Z (MM)**."
%}

![move to axis override dropdown](_images/move_to_axis_override_dropdown.png)

### Offset

**OFFSET** allows you to add positive or negative offsets to the base **LOCATION**. This is useful when pulling tools out of slots, or when watering around or above a plant.

![move to location offset](_images/move_to_location_offset.png)

### Variance

**VARIANCE** allows you to add randomness to a movement, in case you want to perform an action repeatedly (such as suppressing a weed) but with small variations between repetitions. In the example below FarmBot will move to 288 +/- a random variance between 0 and 4 on the X axis. Thus, the final X location will be a random value between 284 and 292.

![move to location variance](_images/move_to_location_variance.png)

### Speed

**SPEED (%)** allows you to slow down movement along an axis for greater precision, for example when mounting and dismounting tools. Speed is a percentage of the **MAX SPEED** for each axis.

![move to location speed](_images/move_to_location_speed.png)

### Safe Z

**SAFE Z** allows you to instruct FarmBot to perform a MOVE command as three distinct movements:

  1. Move Z to the [Safe Z height](../../settings/axes.md#safe-height)
  2. Move X and Y to the new location
  3. Move Z to the new location

This is useful when you need FarmBot to move across the garden but want to ensure it does not run into any plants or other objects.

![move to location safe z](_images/move_to_location_safe_z.png)

# Find home

The <span class="fb-step fb-find-home">Find Home</span> command instructs FarmBot to automatically find the home position for the chosen axis. If you choose **ALL**, FarmBot will find home for each axis one at a time in the order: z-axis, y-axis, x-axis.

![find home](_images/find_home.png)

{%
include callout.html
type="info"
title=""
content="**ENCODERS**, **STALL DETECTION**, or **LIMIT SWITCHES** must be <span class=\"fb-peripheral-on\">ON</span> for FarmBot to automatically find home."
%}

# Set home

The <span class="fb-step fb-set-zero">Set home</span> command instructs FarmBot to set the current location along an axis to `0`, also known as the `Home` position for that axis. If you choose **ALL**, FarmBot will set all axes to zero.

![set home](_images/set_home.png)

# Find axis length

The <span class="fb-step fb-calibrate">FIND AXIS LENGTH</span> command instructs FarmBot to automatically find the length of the chosen axis. If you choose **ALL**, FarmBot will find the length of each axis one at a time in the order: z-axis, y-axis, x-axis.

![find axis length](_images/find_axis_length.png)

{%
include callout.html
type="info"
title=""
content="**ENCODERS**, **STALL DETECTION**, or **LIMIT SWITCHES** must be <span class=\"fb-peripheral-on\">ON</span> for FarmBot to automatically find axis lengths."
%}

# Control servo

The <span class="fb-step fb-set-servo-angle">Control servo</span> command instructs FarmBot to move a servo to the provided **ANGLE**.

![control servo](_images/control_servo.png)

{%
include callout.html
type="pause"
title="Pause for a moment"
content='Because the microcontroller will not know when the servo has reached the desired **ANGLE**, you may need to use a <span class="fb-step fb-wait">Wait</span> command directly after the <span class="fb-step fb-set-servo-angle">Control servo</span> command to ensure the servo reaches its destination before FarmBot moves onto the next step in your sequence.'
%}

# What's next?

 * [Peripheral and Sensor Commands](peripherals-and-sensors.md)
 * [Building a Sequence](../building-a-sequence.md)
