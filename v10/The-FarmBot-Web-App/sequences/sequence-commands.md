---
title: "Sequence Commands"
slug: "sequence-commands"
description: "Descriptions of all the commands you can use in a sequence"
---

* toc
{:toc}

Below are descriptions of all the commands you can use in a sequence. When using the web app, hover over the <i class='fa fa-question-circle'></i> icon in the top right of any sequence step to view usage information.

# Move to
The <span class="fb-step fb-move-absolute">Move To</span> command moves FarmBot to an absolute coordinate position. To use this command, first choose a location from the **LOCATION** dropdown. Options include:

  * Custom coordinates
  * Location variables
  * Tool and seed container locations
  * Plant locations
  * Map points

## Custom coordinates
When choosing the **custom coordinates** option, three input fields will be revealed allowing you to specify the exact <span class="fb-input">X</span>, <span class="fb-input">Y</span>, and <span class="fb-input">Z</span> coordinates you want FarmBot to move to.

![Screen Shot 2019-05-02 at 11.25.20 AM.png](_images/Screen_Shot_2019-05-02_at_11.25.20_AM.png)

## Location variables
When choosing a **location variable**, a variable form will be added to the sequence header. Upon selecting a variable value in the sequence header, the dropdown selections in all <span class="fb-step fb-move-absolute">Move To</span> steps set to that variable will be updated. See the [variables](../sequences/variables.md) documentation for more information.

![2 Variable Form.png](_images/2_Variable_Form.png)

## Other locations
When choosing a tool or seed container location, a plant location, or a map point, those resources will then become _in-use_, meaning that they cannot be deleted until you remove them from your sequence. If you update their coordinates, your sequence steps will be automatically updated.

![Screen Shot 2019-07-05 at 11.28.32 PM.png](_images/Screen_Shot_2019-07-05_at_11.28.32_PM.png)



{%
include callout.html
type="warning"
title="Be careful when moving to tools or seed containers"
content="Under most circumstances you will need to mount a tool or pick up a seed from a seed container in **multiple steps**. First, you should move to the tool or seed container with a **positive z-axis offset**. This will allow FarmBot to then descend onto the tool or into the seed container from above in a second step (with no z-offset).

If you try to move to a location to mount a tool or pick up a seed in one step, you risk the z-axis traveling too low too quickly and the FarmBot crashing into the tool and/or bending a seed injection needle."
%}

## Advanced options
Within the **More [+]** dropdown, you will find options for adding **offsets** to the location and changing the **speed** at which FarmBot performs this movement. In the example below, an **X-OFFSET** of `100` will pull the Watering Nozzle tool out of the tool slot by 100mm. Meanwhile, the **SPEED (%)** option has been set to `50`, meaning FarmBot will perform this movement at 50% of the maximum speed it normally moves at.

You can add offsets for multiple axes at once, and also use negative offsets. The default values for all offsets are `0`, while the default speed is `100%`. By default, the app will only load the **More [+]** dropdowns in an open state if you've changed any of the offset or speed values from the defaults. If you would like the **More [+]** dropdowns to always load in an open state, enable **OPEN OPTIONS BY DEFAULT** from the <i class='fa fa-gear'></i> menu in the sequence header.

![Screen Shot 2019-07-05 at 11.32.24 PM.png](_images/Screen_Shot_2019-07-05_at_11.32.24_PM.png)

# Move relative
The <span class="fb-step fb-move-relative">Move Relative</span> command moves FarmBot a specific distance in any direction, relative from the current position. This is command is best used *after* a <span class="fb-step fb-move-absolute">Move To</span> command. For example, you could use several <span class="fb-step fb-move-relative">Move Relative</span> commands to water in a square *after* the FarmBot has <span class="fb-step fb-move-absolute">Moved To</span> a plant's location.

You can move relative along multiple axes at once, and in both negative and positive directions. The **SPEED (%)** option allows you to slow down the movement for delicate operations, as a percentage of the maximum speed FarmBot normally moves at.

![Screen Shot 2019-05-02 at 11.23.35 AM.png](_images/Screen_Shot_2019-05-02_at_11.23.35_AM.png)

# Control peripheral
The <span class="fb-step fb-write-pin">Control Peripheral</span> command allows you to control **peripherals** such as the vacuum pump, solenoid valve, and lights. To use this command, first select a peripheral from the **PERIPHERAL** dropdown. Options include:

  * All of the peripherals you have defined in the [peripherals widget on the controls page](../../The-FarmBot-Web-App/controls/peripherals.md)
  * The Box LEDs, if you have any included with your FarmBot version

Next, select the **MODE** which you would like to control the peripheral with. You can choose either `Digital` or `Analog`.

Last, specify what value you would like the peripheral to be **SET TO**. The digital mode allows for turning the peripheral **ON** and **OFF**, while the analog mode allows for controlling the peripheral with PWM (pulse width modulation) to any value between `0` and `255`.

![Screen Shot 2019-05-02 at 11.23.50 AM.png](_images/Screen_Shot_2019-05-02_at_11.23.50_AM.png)

## Advanced options
In the **sequence editor options menu** (<span class="fa fa-gear"></span> icon next to the copy sequence button), there is an option to **SHOW PINS**. Enabling this setting will show additional options in the **PERIPHERAL** dropdown for all of the Arduino's raw **pins**. If you have hooked up custom peripherals to any of the Digital Out or Analog Out pins on your electronics board, this is one way you can control them from a sequence like any other peripheral.

{%
include callout.html
type="info"
title="Under the hood, most peripherals are just pins"
content="Remember on the controls page how you defined your peripherals with a **name** and **pin number**? That's because at the microcontroller level, those peripherals (vacuum pump, etc) are hooked up to a specific pin on the Arduino. Giving them a name just makes them much easier to work with here in the sequence editor."
%}

# Toggle peripheral
The <span class="fb-step fb-write-pin">Toggle Peripheral</span> command allows you to toggle the state of a **digital peripheral**. For example, if a peripheral is currently ON, and then FarmBot _toggles_ that peripheral, it will get turned OFF.

To use this command, select a peripheral from the **PERIPHERAL** dropdown. Options include:

  * All of the peripherals you have defined in the [peripherals widget on the controls page](../../The-FarmBot-Web-App/controls/peripherals.md)
  * The Box LEDs, if you have any included with your FarmBot version

![Screen Shot 2020-01-06 at 12.24.47 PM.png](_images/Screen_Shot_2020-01-06_at_12.24.47_PM.png)

# Read sensor
The <span class="fb-step fb-read-pin">Read Sensor</span> command instructs FarmBot to read the value of a **sensor**. For example, you would use this command to measure the soil moisture content with the soil moisture sensor. To use this command, first select a sensor from the **SENSOR** dropdown. Options include:

  * All of the sensors you have defined in the [sensors widget on the controls page](../../The-FarmBot-Web-App/sensors.md)
  * All of the peripherals you have defined in the [peripherals widget on the controls page](../../The-FarmBot-Web-App/controls/peripherals.md)

Next, select the **MODE** which you would like to read the sensor with. You can choose either `Digital` or `Analog`. Use digital for a `0` (LOW) or `1` (HIGH) response, and analog for a reading between `0` and `1023` for 0-5V.

Last, optionally provide a **DATA LABEL** to allow your recorded sensor reading to be more searchable at a later date.

![Screen Shot 2019-05-02 at 11.24.09 AM.png](_images/Screen_Shot_2019-05-02_at_11.24.09_AM.png)

## Advanced options
In the **sequence editor options menu** (<span class="fa fa-gear"></span> icon next to the copy sequence button), there is an option to **SHOW PINS**. Enabling this setting will show additional options in the **SENSOR OR PERIPHERAL** dropdown for all of the Arduino's raw **pins**. If you have hooked up custom sensors to any of the Digital In or Analog In pins on your electronics board, this is one way you can read them from a sequence like any other sensor.

{%
include callout.html
type="info"
title="Under the hood, most sensors are just pins"
content="Remember on the controls page how you defined your sensors with a **name** and **pin number**? That's because at the microcontroller level, those sensors (soil moisture, etc) are hooked up to a specific pin on the Arduino. Giving them a name just makes them much easier to work with here in the sequence editor."
%}

# Control servo
The <span class="fb-step fb-move-absolute">Control servo</span> command instructs FarmBot to move a servo to the provided angle.

![Screen Shot 2020-02-10 at 12.01.17 PM.png](_images/Screen_Shot_2020-02-10_at_12.01.17_PM.png)

# Wait
The <span class="fb-step fb-wait">Wait</span> command causes a delay before executing the next step in the sequence. This could be used to hold the solenoid valve open for FarmBot to water a plant for `2000` milliseconds (2 seconds), for example.

The maximum time allowed is 3 minutes (`180,000` milliseconds). If you need to have FarmBot wait for longer, use multiple steps.

![Screen Shot 2019-05-02 at 11.24.22 AM.png](_images/Screen_Shot_2019-05-02_at_11.24.22_AM.png)

# Send message
The <span class="fb-step fb-wait">Send Message</span> command instructs FarmBot to send a message. This is useful for error and success notifications and debugging. To use this command, simply type in the **MESSAGE** you would like FarmBot to send, choose a **TYPE**, and select the channels you would like the message to be sent to.

`{{ x }}` can be used as a text variable for FarmBot's current x-axis position (`y` and `z` can also be used). `{{ pin13 }}` can be used to write the current value of pin 13 (pins 0 through 69 can also be used).

![Screen Shot 2020-02-10 at 12.20.10 PM.png](_images/Screen_Shot_2020-02-10_at_12.20.10_PM.png)

# E-stop
The <span class="fb-step fb-e-stop">E-stop</span> command instructs FarmBot to stop operations (halt motor movements and turn off peripherals). To continue operations, you will need to manually unlock the device.

![Screen Shot 2020-02-10 at 12.20.15 PM.png](_images/Screen_Shot_2020-02-10_at_12.20.15_PM.png)

# Reboot
The <span class="fb-step fb-wait">Reboot</span> command instructs FarmBot to power cycle the onboard computer.

![Screen Shot 2020-02-10 at 12.05.37 PM.png](_images/Screen_Shot_2020-02-10_at_12.05.37_PM.png)

# Find home
The <span class="fb-step fb-find-home">Find Home</span> command instructs FarmBot to automatically find the home position for the chosen axis. If you choose to **FIND ALL**, FarmBot will find home for each axis one at a time in the order: z-axis, y-axis, x-axis. Note that **ENCODERS**, **STALL DETECTION**, or **LIMIT SWITCHES** must be <span class="fb-peripheral-on">ON</span> for FarmBot to automatically find home.

![Screen Shot 2019-05-02 at 11.24.44 AM.png](_images/Screen_Shot_2019-05-02_at_11.24.44_AM.png)

# Set home
The <span class="fb-step fb-find-home">Set home</span> command instructs FarmBot to set the current location along an axis to `0`, also known as the `Home` position for that axis. If you choose to **SET HOME ALL**, FarmBot will set all axes to zero.

![Screen Shot 2020-06-10 at 5.44.51 PM.png](_images/Screen_Shot_2020-06-10_at_5.44.51_PM.png)

# Find axis length
The <span class="fb-step fb-find-home">FIND AXIS LENGTH</span> command instructs FarmBot to automatically find the length of the chosen axis. If you choose to **FIND LENGTH ALL**, FarmBot will find the length of each axis one at a time in the order: z-axis, y-axis, x-axis. Note that **ENCODERS**, **STALL DETECTION**, or **LIMIT SWITCHES** must be <span class="fb-peripheral-on">ON</span> for FarmBot to automatically find axis lengths.

![Screen Shot 2020-06-10 at 5.44.59 PM.png](_images/Screen_Shot_2020-06-10_at_5.44.59_PM.png)

# If statement
The <span class="fb-step fb-if-statement">If Statement</span> command allows FarmBot to check if a condition is true or false and take an action based on the results. This allows for smarter, condition based farming, and for gracefully handling errors and failures.

If the condition that FarmBot checks is true, you can instruct FarmBot to execute another sequence or do nothing, in which case FarmBot will continue to the next step in the current sequence. If the condition that FarmBot checks is false, you can also instruct FarmBot to execute another sequence or do nothing.

In the example below, FarmBot will check **_IF..._** the **VARIABLE** (`Soil moisture`) `is less than` the **VALUE** (`500`). If that condition is true, **_THEN..._** FarmBot will execute a sequence to `Water the plant`. **_ELSE..._** (if the condition is not true), FarmBot will do nothing (ie: continue to the next step in the current sequence).

![Screen Shot 2019-05-02 at 12.55.52 PM.png](_images/Screen_Shot_2019-05-02_at_12.55.52_PM.png)

# Execute sequence
The <span class="fb-step fb-execute">Execute Sequence</span> command uses *existing sequences* as *steps* in a *new, larger sequence*. This allows you to re-use smaller, simpler sequences in different combinations to create far more complex sequences that are easier to modify, manage, and mashup later because of their modularity.

For example, you could make a sequence to `Mount the watering nozzle`, another sequence to `Water the plant`, and a third sequence to `Unmount the watering nozzle`. Then, in a new sequence, you could use three <span class="fb-step fb-execute">Execute Sequence</span> commands (one for each of the smaller sequences) to execute all the steps needed to water the plant.

![Screen Shot 2019-05-02 at 2.12.30 PM.png](_images/Screen_Shot_2019-05-02_at_2.12.30_PM.png)



{%
include callout.html
type="success"
title="Pro tip"
content="You can drag and drop existing sequences from the **sequences list** into an open sequence in the **sequence editor** to add an <span class=\"fb-step fb-execute\">Execute Sequence</span> step with that sequence selected."
%}

# Run farmware
The <span class="fb-step fb-take-photo">Run Farmware</span> command instructs FarmBot to run a [farmware](../../The-FarmBot-Web-App/farmware.md). To use the command, select which farmware you would like to run from the **PACKAGE NAME** dropdown. Or, select `Manual Input` and type in the name of the package, for example, `plant-detection`.

![Screen Shot 2019-05-02 at 11.26.53 AM.png](_images/Screen_Shot_2019-05-02_at_11.26.53_AM.png)

# Take photo
The <span class="fb-step fb-wait">Take Photo</span> command instructs FarmBot to take a photo with the USB camera or the Raspberry Pi camera (whichever is selected in [device settings](../../The-FarmBot-Web-App/settings/farmbot-settings.md)). After taking the photo, FarmBot will upload it to the web app, along with the coordinates from where the photo was taken, and the date and time.

You can view the photos taken on the farmware page and in the farm designer.

![Screen Shot 2019-05-02 at 11.27.01 AM.png](_images/Screen_Shot_2019-05-02_at_11.27.01_AM.png)

# Mark as
The <span class="fb-step fb-wait">Mark as</span> command instructs FarmBot to **MARK** an item's **PROPERTY**  **AS** the value of your choice. For example, you could mark a Spinach plant's `Plant stage` property as `Planted`. Using this command allows FarmBot to systematically update an item's properties as it works with that item. This step also accepts a Location Variable as an input, which can be used when running a sequence over a group of items.

![Screen Shot 2020-05-21 at 10.31.55 PM.png](_images/Screen_Shot_2020-05-21_at_10.31.55_PM.png)

While a variety of properties are available for each item type such as `X`, `Y`, `Z`, `Radius`, and `Color`, you can also set custom properties in the format `meta.custom-property`. These properties can then be viewed on the item's details panel in the farm designer, and you can also select items with these properties using advanced groups filters.

![Screen Shot 2020-05-21 at 10.32.27 PM.png](_images/Screen_Shot_2020-05-21_at_10.32.27_PM.png)

# Assertion

{%
include callout.html
type="warning"
title="Advanced feature"
content="The assertion command is intended for power users and software developers only. See the [developer documentation](https://developer.farm.bot/docs/assertions) for a list of the available functions."
%}

The <span class="fb-step fb-if-statement">Assertion</span> command allows FarmBot to test if a condition is true or false for automated testing purposes. For example, you could set up a FarmBot to move back and forth repeatedly along an axis, and check the position after each movement. This type of test is useful for high-cycle hardware testing, and for continuous integration testing of software changes.

Assertions must be written in **Lua**, and will be evaluated against a Lua 5.2 interpreter. In the event that a **TEST FAILS**, FarmBot can either `Continue` execution, `Recover and continue`, `Abort and recover`, or just `Abort` execution altogether. The **RECOVERY SEQUENCE** allows you to reset FarmBot to a known state after a failure, send a message, or perform any other desired operations.

![Assertion.JPG](_images/Assertion.JPG)


# What's next?

 * [Building a Sequence](../sequences/building-a-sequence.md)
