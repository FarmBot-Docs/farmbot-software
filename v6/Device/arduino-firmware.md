---
title: "Arduino Firmware"
slug: "arduino-firmware"
description: "Step-by-step instructions for installing the FarmBot's Arduino firmware"
---

* toc
{:toc}

The [Farmbot Arduino Firmware](https://github.com/FarmBot/farmbot-arduino-firmware) performs the following tasks:

 * Physically controls the FarmBot hardware by sending electrical pulses to the stepper motor drivers, reading voltages from pins, and outputting voltages and data to the Universal Tool Mount
 * Communicates with the Raspberry Pi via a serial connection over a USB cable in order to receive G-code and F-code commands and send back log and collected data.
 * Monitors the rotary encoders as a closed-loop feedback control system to ensure that the stepper motors have not missed any steps.

Below, we describe the available methods for installing the Arduino Firmware onto the Arduino. Most users will use the first method.

{%
include callout.html
type="success"
title="Help Improve the Arduino Firmware"
content="Found some bugs? Have a feature request or improved code you would like to contribute? Let us know by opening up an issue or submitting a pull request on the [GitHub repository for the FarmBot Arduino Firmware](https://github.com/FarmBot/farmbot-arduino-firmware)."
%}



# Installation

## From FarmBot OS (automatic)

{%
include callout.html
type="success"
title="Installed automatically"
content="If you just [installed](farmbot-os.md) and [configured](configurator.md) FarmBot OS, then the Arduino firmware has already been installed and you can skip ahead to using the [web app](../Web-App/the-farmbot-web-app.md).

Any time FarmBot OS updates, it will install the latest version of the firmware automatically as well."
%}

## From the Web App (easy)
If you chose the wrong electronics board/hardware version during configuration and find yourself with the wrong firmware installed, it is easy to install the correct firmware from the Web App.

Navigate to the [Device page](https://my.farm.bot/app/device). Under the Device widget, select the correct electronics board/hardware version from the dropdown menu labelled **FIRMWARE**. This will instruct FarmBot to install the chosen version of the firmware.

## From the Arduino IDE (hard)

{%
include callout.html
type="info"
title="Want to Hack?"
content="There is more technical documentation about the FarmBot Arduino Firmware in the [README file](https://github.com/FarmBot/farmbot-arduino-firmware/blob/master/README.md)."
%}



{%
include callout.html
type="warning"
title="Advanced Users Only"
content="This method is not recommended because you have to manually download and install the firmware through the Arduino IDE instead of installing the Arduino firmware with one click from the FarmBot web application."
%}

If you do not want to use the firmware installed by FarmBot OS, you can still install the FarmBot Arduino Firmware by using the standard Arduino IDE with the steps below.

1. Download and install the [Arduino IDE](https://www.arduino.cc/en/Main/Software) onto your computer.
2. Download and unzip the latest [FarmBot Arduino Firmware](https://github.com/FarmBot/farmbot-arduino-firmware).
3. In the firmware folder you just unzipped, go to the **src** sub-folder and open up **src** with the Arduino IDE. Note: this file is blank, but there are many other file tabs that should be automatically opened as well.
4. Connect your Arduino to your computer with a USB cable.
5. From the IDE, click **Tools** > **Board**, and then select `Arduino Mega 2560`.
6. Now click **File** > **Upload**. This will flash the firmware onto your Arduino.
