---
title: "Firmware Settings"
slug: "firmware-settings"
description: ":floppy_disk: FarmBot model and firmware management.\n[Open these settings in the app](https://my.farm.bot/app/designer/settings?highlight=firmware)"
---


# Firmware

Select the firmware to be used with your electronics board. This will flash the selected firmware to the microcontroller. Pressing <span class="fb-button fb-yellow">FLASH FIRMWARE</span> will manually flash the firmware, which may be required when installing a new electronics board.

# Firmware path

{%
include callout.html
type="info"
content="This [advanced setting](../settings/parameter-management.md#show-advanced-settings) is not shown by default."
%}

View and change the firmware device path. Select `ttyACM0` for Genesis, `ttyAMA0` for Express, or choose `Manual input` to select a custom device path. This value is automatically set based on FarmBot model for most users, but can be configured for custom setups with multiple serial devices connected.

# Restart firmware

This will restart the firmware. This may be useful for developers.
