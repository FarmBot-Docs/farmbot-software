---
title: "Sequence Commands"
slug: "sequence-commands"
description: "Descriptions of the basic commands you can use in a sequence"
---

* toc
{:toc}

Below are descriptions of the basic commands you can use in a sequence. When using the web app, hover over the <i class='fa fa-question-circle'></i> icon in the top right of any sequence step to view usage information.

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

When choosing **variable - add new**, a variable form will be added to the sequence header. Upon selecting a variable value in the sequence header, the dropdown selections in all <span class="fb-step fb-move">Move</span> steps set to that variable will be updated. See the [variables](variables.md) documentation for more information.

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

**OVERRIDE** allows you to override the X, Y, and/or Z values from the **LOCATION** field with new values. You may type in a custom coordinate, a formula, or disable an axis entirely. The Z axis override dropdown also includes a special **Safe Height** value. Currently the Safe Height is set to Z = 0, though this will be customizable in the settings panel in the future. Coming soon is a Soil Height option.

{%
include callout.html
type="info"
title=""
content="If you choose custom coordinates for the **LOCATION** field, **OVERRIDE** will appear as **X, Y, Z (MM)**."
%}

![move to axis override dropdown](_images/move_to_axis_override_dropdown.png)

**OFFSET** allows you to add positive or negative offsets to the base **LOCATION**. This is useful when pulling tools out of slots, or when watering around or above a plant.

![move to location offset](_images/move_to_location_offset.png)

**VARIANCE** allows you to add randomness to a movement, in case you want to perform an action repeatedly (such as suppressing a weed) but with small variations between repetitions. In the example below FarmBot will move to 288 +/- a random variance between 0 and 4 on the X axis. Thus, the final X location will be a random value between 284 and 292.

![move to location variance](_images/move_to_location_variance.png)

**SPEED (%)** allows you to slow down movement along an axis for greater precision, for example when mounting and dismounting tools. Speed is a percentage of the **MAX SPEED** for each axis.

![move to location speed](_images/move_to_location_speed.png)

**SAFE Z** allows you to instruct FarmBot to perform a MOVE command as three distinct movements:

  1. Move Z to the Safe Z height
  2. Move X and Y to the new location
  3. Move Z to the new location

This is useful when you need FarmBot to move across the garden but want to ensure it does not run into any plants or other objects.

![move to location safe z](_images/move_to_location_safe_z.png)

# Control peripheral

The <span class="fb-step fb-write-pin">Control Peripheral</span> command allows you to control **peripherals** such as the vacuum pump, solenoid valve, and lights. To use this command, first select a peripheral from the **PERIPHERAL** dropdown. Options include:

  * All of the peripherals you have defined in the [peripherals section of the controls panel](../controls/peripherals.md)
  * The Box LEDs, if you have any included with your FarmBot version

Next, select the **MODE** which you would like to control the peripheral with. You can choose either `Digital` or `Analog`.

Last, specify what value you would like the peripheral to be **SET TO**. The digital mode allows for turning the peripheral **ON** and **OFF**, while the analog mode allows for controlling the peripheral with PWM (pulse width modulation) to any value between `0` and `255`.

![control peripheral](_images/control_peripheral.png)

## Advanced options

In the **sequence editor options menu** (<span class="fa fa-gear"></span> icon next to the copy sequence button), there is an option to **SHOW PINS**. Enabling this setting will show additional options in the **PERIPHERAL** dropdown for all of the Arduino's raw **pins**. If you have hooked up custom peripherals to any of the Digital Out or Analog Out pins on your electronics board, this is one way you can control them from a sequence like any other peripheral.

{%
include callout.html
type="info"
title="Under the hood, most peripherals are just pins"
content="Remember in the controls panel how you defined your peripherals with a **name** and **pin number**? That's because at the microcontroller level, those peripherals (vacuum pump, etc) are hooked up to a specific pin on the Arduino. Giving them a name just makes them much easier to work with here in the sequence editor."
%}

# Toggle peripheral

{%
include callout.html
type="info"
title="Coming soon"
content=""
%}

The <span class="fb-step fb-write-pin">Toggle Peripheral</span> command allows you to toggle the state of a **digital peripheral**. For example, if a peripheral is currently ON, and then FarmBot _toggles_ that peripheral, it will get turned OFF.

To use this command, select a peripheral from the **PERIPHERAL** dropdown. Options include:

  * All of the peripherals you have defined in the [peripherals section of the controls panel](../controls/peripherals.md)
  * The Box LEDs, if you have any included with your FarmBot version

![toggle peripheral](_images/toggle_peripheral.png)

# Read sensor

The <span class="fb-step fb-read-pin">Read Sensor</span> command instructs FarmBot to read the value of a **sensor**. For example, you would use this command to measure the soil moisture content with the soil moisture sensor. To use this command, first select a sensor from the **SENSOR** dropdown. Options include:

  * All of the sensors you have defined in the [sensors panel](../sensors.md)
  * All of the peripherals you have defined in the [peripherals section of the controls panel](../controls/peripherals.md)

Next, select the **MODE** which you would like to read the sensor with. You can choose either `Digital` or `Analog`. Use digital for a `0` (LOW) or `1` (HIGH) response, and analog for a reading between `0` and `1023` for 0-5V.

Last, optionally provide a **DATA LABEL** to allow your recorded sensor reading to be more searchable at a later date.

![read sensor](_images/read_sensor.png)

## Advanced options

In the **sequence editor options menu** (<span class="fa fa-gear"></span> icon next to the copy sequence button), there is an option to **SHOW PINS**. Enabling this setting will show additional options in the **SENSOR OR PERIPHERAL** dropdown for all of the Arduino's raw **pins**. If you have hooked up custom sensors to any of the Digital In or Analog In pins on your electronics board, this is one way you can read them from a sequence like any other sensor.

{%
include callout.html
type="info"
title="Under the hood, most sensors are just pins"
content="Remember in the sensors panel how you defined your sensors with a **name** and **pin number**? That's because at the microcontroller level, those sensors (soil moisture, etc) are hooked up to a specific pin on the Arduino. Giving them a name just makes them much easier to work with here in the sequence editor."
%}

# Control servo

The <span class="fb-step fb-set-servo-angle">Control servo</span> command instructs FarmBot to move a servo to the provided **ANGLE**.

![control servo](_images/control_servo.png)

# Wait

The <span class="fb-step fb-wait">Wait</span> command causes a delay before executing the next step in the sequence. This could be used to hold the solenoid valve open for FarmBot to water a plant for `2000` milliseconds (2 seconds), for example.

The maximum time allowed is 3 minutes (`180,000` milliseconds). If you need to have FarmBot wait for longer, use multiple steps.

![wait](_images/wait.png)

# Send message

The <span class="fb-step fb-send-message">Send Message</span> command instructs FarmBot to send a message. This is useful for error and success notifications and debugging. To use this command, simply type in the **MESSAGE** you would like FarmBot to send, choose a **TYPE**, and select the channels you would like the message to be sent to.

`{{ x }}` can be used as a text variable for FarmBot's current x-axis position (`y` and `z` can also be used). `{{ pin13 }}` can be used to write the current value of pin 13 (pins 0 through 69 can also be used).

![send message](_images/send_message.png)

# E-stop

The <span class="fb-step fb-e-stop">E-stop</span> command instructs FarmBot to stop operations (halt motor movements and turn off peripherals). To continue operations, you will need to manually unlock the device.

![e-stop](_images/e-stop.png)

# Reboot

The <span class="fb-step fb-reboot">Reboot</span> command instructs FarmBot to power cycle the onboard computer.

![reboot](_images/reboot.png)

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

# If

The <span class="fb-step fb-if-statement">If...</span> command allows FarmBot to check if a condition is true or false and take an action based on the results. This allows for smarter, condition based farming, and for gracefully handling errors and failures.

If the condition that FarmBot checks is true, you can instruct FarmBot to execute another sequence or do nothing, in which case FarmBot will continue to the next step in the current sequence. If the condition that FarmBot checks is false, you can also instruct FarmBot to execute another sequence or do nothing.

In the example below, FarmBot will check **_IF..._** the **VARIABLE** (`Soil moisture`) `is less than` the **VALUE** (`500`). If that condition is true, **_THEN..._** FarmBot will execute a sequence to `Water the plant`. **_ELSE..._** (if the condition is not true), FarmBot will do nothing (ie: continue to the next step in the current sequence).

![if statement](_images/if_statement.png)

# Execute sequence

The <span class="fb-step fb-execute">Execute Sequence</span> command uses *existing sequences* as *steps* in a *new, larger sequence*. This allows you to re-use smaller, simpler sequences in different combinations to create far more complex sequences that are easier to modify, manage, and mashup later because of their modularity.

For example, you could make a sequence to `Mount the watering nozzle`, another sequence to `Water the plant`, and a third sequence to `Unmount the watering nozzle`. Then, in a new sequence, you could use three <span class="fb-step fb-execute">Execute Sequence</span> commands (one for each of the smaller sequences) to execute all the steps needed to water the plant.

![execute sequence steps](_images/execute_sequence_steps.png)

{%
include callout.html
type="success"
title="Pro tip"
content="You can drag and drop existing sequences from the **sequences list** into an open sequence in the **full sequence editor** to add an <span class=\"fb-step fb-execute\">Execute Sequence</span> step with that sequence selected."
%}

# Run farmware

The <span class="fb-step fb-run-farmware">Run Farmware</span> command instructs FarmBot to run a [farmware](../farmware.md). To use the command, select which farmware you would like to run from the **PACKAGE NAME** dropdown. Or, select `Manual Input` and type in the name of the package, for example, `plant-detection`.

![run farmware](_images/run_farmware.png)

# Detect weeds

The <span class="fb-step fb-run-farmware">Detect Weeds</span> command instructs FarmBot to take a photo and run the weed detection software. After taking the photo and processing it, FarmBot will upload it to the web app, along with the coordinates from where the photo was taken, the date and time. FarmBot will also add any weeds that it identified to the **PENDING** category in the weeds panel.

![detect weeds](_images/detect_weeds.png)

# Take photo

The <span class="fb-step fb-take-photo">Take Photo</span> command instructs FarmBot to take a photo with the USB camera or the Raspberry Pi camera (whichever is selected in [camera settings](../photos/camera-settings.md)). After taking the photo, FarmBot will upload it to the web app, along with the coordinates from where the photo was taken, and the date and time.

You can view the photos taken on the photos panel and in the farm designer.

![take a photo](_images/take_a_photo.png)

# Mark as

The <span class="fb-step fb-mark-as">Mark as</span> command instructs FarmBot to **MARK** an item's **PROPERTY**  **AS** the value of your choice. For example, you could mark a Spinach plant's `Plant stage` property as `Planted`. Using this command allows FarmBot to systematically update an item's properties as it works with that item. This step also accepts a Location Variable as an input, which can be used when running a sequence over a group of items.

![mark as](_images/mark_as.png)

While a variety of properties are available for each item type such as `X`, `Y`, `Z`, `Radius`, and `Color`, you can also set custom properties in the format `meta.custom-property`. These properties can then be viewed on the item's details panel in the farm designer, and you can also select items with these properties using advanced groups filters.

![mark as custom property](_images/mark_as_custom_property.png)

# What's next?

 * [Advanced Sequence Commands](advanced-sequence-commands.md)
 * [Building a Sequence](building-a-sequence.md)
