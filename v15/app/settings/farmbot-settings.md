---
title: "FarmBot Settings"
slug: "farmbot-settings"
description: ":robot: Device name and software updates.\n[Open these settings in the app](https://my.farm.bot/app/designer/settings?highlight=farmbot)"
---


# Name

Give your FarmBot a fun name. For example: `Broccoli Overlord` 🥦 🤖

# Order number

By registering your original FarmBot **ORDER NUMBER** with your web app account you will receive prioritized help should you run into any issues.

{%
include callout.html
type="warning"
title=""
content="We have limited capacity to help users of the app that did not purchase hardware from [farm.bot](https://farm.bot)."
%}

# Timezone

Set the device's timezone.

{%
include callout.html
type="clock-o"
title="Automatically set"
content="When you create your FarmBot web app account and login for the first time, we will automatically set your device's timezone to match your computer or phone's timezone (whichever was used to login to the account). If your FarmBot is located somewhere else, you can change the timezone setting here."
%}

# Location

Specify where FarmBot is located in the world with latitude and longitude coordinates. This information may be used by advanced sequence commands to provide smarter FarmBot operation, such as a watering command that uses local weather data.

To set the location, press the <span class="fb-button fb-blue"><i class='fa fa-crosshairs'></i></span> button and grant your web browser permission to provide location information to the web app. This will automatically set the coordinates using two decimal precision (neighborhood level). If you would like to provide more or less precision, you may edit the coordinates manually. Clicking the <i class='fa fa-map'></i> icon will open [openstreetmap.org](https://www.openstreetmap.org) to the current coordinates so that you may double check accuracy.

# Indoor

Specify whether or not your FarmBot is located indoors. This information may be used by advanced sequence commands to provide smarter FarmBot operation based on an indoor vs outdoor environment.

# Update time

With this dropdown you can choose the hour of the day when FarmBot will apply software updates so that updates occur at a convenient time (such as the middle of the night) when you do not have any events scheduled and do not plan to be working with your FarmBot.

You may also choose the `As soon as possible` option, in which case FarmBot will install updates immediately as they become available. Note that selecting this option may cause unexpected disruptions and event execution failures.

# Auto update

{%
include callout.html
type="info"
content="This [advanced setting](../settings.md#show-advanced-settings) is not shown by default."
%}

By default, FarmBot OS will automatically download and install software updates at **3AM**. The update process may take up to 1 hour to complete. If you need your FarmBot to perform updates at a different time, you can choose the desired time with this setting, or disable auto updates entirely.

{%
include callout.html
type="warning"
content="If you decide to disable auto updates, please make sure you regularly manually update your device so that it stays within our [support policy](../../docs/troubleshooting/support-policy.md)."
%}

# FarmBot OS

{%
include callout.html
type="info"
content="This [advanced setting](../settings.md#show-advanced-settings) is not shown by default."
%}

View the version of FarmBot OS that you have installed on your device, that version's release notes, and install updates if they are available using the <span class="fb-button fb-green">UPDATE</span> button. Note that the update button will display as <span class="fb-button fb-gray">UP TO DATE</span> when there are no updates available.

# Boot sequence

The **BOOT SEQUENCE** is a customizable sequence that FarmBot will execute as the final step of the boot up process. This can be especially useful for recovering from a power outage, or to just simply prepare your FarmBot automatically for it's scheduled tasks after every power cycle.

We recommend getting started with a boot sequence that finds home and sends a message via email so you stay informed about when FarmBot has rebooted. More advanced users may wish to perform additional actions such as operating external peripherals or reading sensors, turning on the lights, mounting a tool, etc.

# Firmware

Select the firmware to be used with your electronics board and then press <span class="fb-button fb-yellow">FLASH FIRMWARE</span> to manually flash the firmware to the microcontroller. This may be required when installing a new electronics board.

{%
include callout.html
type="info"
title="Just upgraded?"
content="If you are upgrading your FarmBot's electronics board, you may need to manually add any new peripherals, sensors, and tools that your new electronics board supports."
%}

# Firmware path

{%
include callout.html
type="info"
content="This [advanced setting](../settings.md#show-advanced-settings) is not shown by default."
%}

View and change the firmware device path. Select `ttyACM0` for Genesis, `ttyAMA0` for Express, or choose `Manual input` to select a custom device path. This value is automatically set based on FarmBot model for most users, but can be configured for custom setups with multiple serial devices connected.

# What's next?

 * [Auto Updates](../../farmbot-os/intro/auto-updates.md)
