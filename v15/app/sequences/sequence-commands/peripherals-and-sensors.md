---
title: "Peripheral and Sensor Commands"
slug: "peripherals-and-sensors"
description: "Control peripherals and sensors"
---

# Control peripheral

The <span class="fb-step fb-write-pin">Control Peripheral</span> command allows you to control **peripherals** such as the vacuum pump, solenoid valve, and lights. To use this command, first select a peripheral from the **PERIPHERAL** dropdown. Options include:

  * All of the peripherals you have defined in the [peripherals section of the controls panel](../../controls/peripherals.md)
  * The Box LEDs, if you have any included with your FarmBot version

Next, select the **MODE** which you would like to control the peripheral with. You can choose either `Digital` or `Analog`.

Last, specify what value you would like the peripheral to be **SET TO**. The digital mode allows for turning the peripheral **ON** and **OFF**, while the analog mode allows for controlling the peripheral with PWM (pulse width modulation) to any value between `0` and `255`.

![control peripheral](_images/control_peripheral.png)

# Toggle peripheral

The <span class="fb-step fb-write-pin">Toggle Peripheral</span> command allows you to toggle the state of a **digital peripheral**. For example, if a peripheral is currently ON, and then FarmBot _toggles_ that peripheral, it will get turned OFF.

To use this command, select a peripheral from the **PERIPHERAL** dropdown.

![toggle peripheral](_images/toggle_peripheral.png)

# Read sensor

The <span class="fb-step fb-read-pin">Read Sensor</span> command instructs FarmBot to read the value of a **sensor**. For example, you would use this command to measure the soil moisture content with the soil moisture sensor. To use this command, first select a sensor from the **SENSOR** dropdown. Options include:

  * All of the sensors you have defined in the [sensors panel](../../sensors.md)
  * All of the peripherals you have defined in the [peripherals section of the controls panel](../../controls/peripherals.md)

Next, select the **MODE** which you would like to read the sensor with. You can choose either `Digital` or `Analog`. Use digital for a `0` (LOW) or `1` (HIGH) response, and analog for a reading between `0` and `1023` for 0-5V.

Last, optionally provide a **DATA LABEL** to allow your recorded sensor reading to be more searchable at a later date.

![read sensor](_images/read_sensor.png)

# Advanced options

In the **sequence editor options menu** (<span class="fa fa-gear"></span> icon), there is an option to **SHOW PINS**. Enabling this setting will show additional options in **SENSOR** and **PERIPHERAL** dropdowns for all of the Arduino's raw **pins**. If you have hooked up custom peripherals or sensors to any of the Digital Analog I/O pins on your electronics board, this is one way you can interact with them from a sequence.

{%
include callout.html
type="info"
title="Under the hood, most sensors and peripherals are just pins"
content="Remember in the controls and sensors panels how you defined your peripherals and sensors with a **name** and **pin number**? That's because at the microcontroller level, those peripherals and sensors (LED strip, vacuum pump, soil moisture sensor, etc) are all hooked up to a specific input/output pin on the Arduino. Giving them a name just makes them much easier to work with in the sequence editor."
%}

# What's next?

 * [Image Processing Commands](image-processing.md)
 * [Building a Sequence](../building-a-sequence.md)
