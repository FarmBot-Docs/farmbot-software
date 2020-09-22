---
title: "Arduino Firmware"
slug: "arduino-firmware"
excerpt: "Step-by-step instructions for installing the FarmBot's Arduino firmware"
---

* toc
{:toc}

The FarmBot Arduino Firmware performs the following tasks:

 * Physically controls the FarmBot hardware by sending electrical pulses to the stepper motor drivers, reading voltages from pins, and outputting voltages and data to the Universal Tool Mount
 * Communicates with the Raspberry Pi via a serial connection over a USB cable in order to receive G-code and F-code commands and send back log and collected data.
 * Monitors the rotary encoders as a closed-loop feedback control system to ensure that the stepper motors have not missed any steps.

Below, we describe the available methods for installing the Arduino Firmware onto the Arduino. Most users will use the first method.

# Installation

## From FarmBot OS (automatic)

{%
include callout.html
type="success"
title="Installed automatically"
content="If you just [installed](../FarmBot OS/farmbot-os.md) and [configured](../FarmBot OS/farmbot-os/configurator.md) FarmBot OS, then the Arduino firmware has already been installed and you can skip ahead to using the [web app](../The FarmBot Web App/the-farmbot-web-app.md).

Any time FarmBot OS updates, it will install the latest version of the firmware automatically as well."
%}

## From the Web App (easy)
If you chose the wrong electronics board/hardware version during configuration and find yourself with the wrong firmware installed, it is easy to install the correct firmware from the Web App.

Navigate to the [Device page](https://my.farm.bot/app/device). Under the Device widget, select the correct electronics board/hardware version from the dropdown menu labelled **FIRMWARE**. This will instruct FarmBot to install the chosen version of the firmware.

## From the Arduino IDE (hard)

{%
include callout.html
type="warning"
title="For developers only"
content="This method is only recommended for software developers working with custom firmware. For more information, see the [developer docs](https://developer.farm.bot/docs/firmware#section-installing-custom-firmware)."
%}

