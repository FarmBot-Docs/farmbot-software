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
content="If you just [installed](intro.md#installation) and [configured](intro/configurator.md) FarmBot OS, then the Arduino firmware has already been flashed to the microcontroller and you can skip ahead to using the [web app](../app/intro.md).

Any time FarmBot OS updates, it will flash the latest version of the firmware automatically as well."
%}

# Changing firmware

If you need to change your firmware because you chose the wrong one during setup, or you just upgraded your electronics, you can manually change it. Navigate to the [firmware section of the settings panel](https://my.farm.bot/app/designer/settings?highlight=firmware) and select the correct electronics board/hardware version from the dropdown menu labelled **FIRMWARE**. This will instruct FarmBot to flash the new firmware. After flashing is complete, you will need to <span class="fb-button fb-yellow">UNLOCK</span> FarmBot to complete the initialization.

![firmware selection menu genesis v1.4](_images/firmware_selection_menu_genesis_v1.4.png)

# Reflashing firmware

If you are experiencing issues with your firmware, or just installed replacement electronics without firmware installed, you may manually reflash the firmware. Navigate to the [firmware section of the settings panel](https://my.farm.bot/app/designer/settings?highlight=firmware) and click <span class="fb-button fb-yellow">FLASH FIRMWARE</span>. After flashing is complete, you will need to <span class="fb-button fb-yellow">UNLOCK</span> FarmBot to complete the initialization.

![flash firmware button](_images/flash_firmware_button.png)

# Using custom firmware

Using custom firmware is only recommended for software developers. For more information, see the [developer docs](https://developer.farm.bot/docs/custom-firmware).

# What's next?

 * [Stall Detection Hardware](arduino-firmware/stall-detection-hardware.md)
 * [Kinematic Equations](arduino-firmware/kinematic-equations.md)
 * [Microstepping](arduino-firmware/microstepping.md)
