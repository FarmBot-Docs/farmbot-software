---
title: "Arduino Firmware"
slug: "arduino-firmware"
---

* toc
{:toc}

The **FarmBot Arduino Firmware** performs the following tasks:

 * Physically controls the FarmBot hardware by sending electrical pulses to the stepper motor drivers, reading voltages from pins, and outputting voltages and data to the Universal Tool Mount and peripherals.
 * Communicates with the Raspberry Pi to receive G-code and F-code commands and send back logs and collected data.
 * Monitors the rotary encoders as a closed-loop feedback control system to ensure that the stepper motors have not missed any steps. (Genesis kits only)

{%
include callout.html
type="success"
title="Installed automatically"
content="If you just [installed](../FarmBot-OS/farmbot-os.md) and [configured](../FarmBot-OS/farmbot-os/configurator.md) FarmBot OS, then the Arduino firmware has already been flashed to the microcontroller and you can skip ahead to using the [web app](../The-FarmBot-Web-App/the-farmbot-web-app.md).

Any time FarmBot OS updates, it will flash the latest version of the firmware automatically as well."
%}

# Changing firmware

If you need to change your firmware because you chose the wrong one during setup, or you just upgraded your electronics, you can manually change it. Navigate to the [Device page](https://my.farm.bot/app/device). Under the Device widget, select the correct electronics board/hardware version from the dropdown menu labelled **FIRMWARE**. This will instruct FarmBot to flash the new firmware. After flashing is complete, you will need to <span class="fb-button fb-yellow">UNLOCK</span> FarmBot to complete the initialization.

![Screen Shot 2020-04-21 at 4.36.03 PM.png](Screen_Shot_2020-04-21_at_4.36.03_PM.png)

# Reflashing firmware

If you are experiencing issues with your firmware, or just installed replacement electronics without firmware installed, you may manually reflash the firmware. Navigate to the [Device page](https://my.farm.bot/app/device). Under the Device widget, find the **FLASH FIRMWARE** setting and click <span class="fb-button fb-yellow">FLASH FIRMWARE</span>. After flashing is complete, you will need to <span class="fb-button fb-yellow">UNLOCK</span> FarmBot to complete the initialization.

![Screen Shot 2020-04-21 at 4.38.03 PM.png](Screen_Shot_2020-04-21_at_4.38.03_PM.png)

# Using custom firmware

Using custom firmware is only recommended for software developers. For more information, see the [developer docs](https://developer.farm.bot/Documentation/firmware/custom-firmware).
