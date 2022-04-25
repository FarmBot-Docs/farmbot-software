---
title: "Device Settings"
slug: "device-settings"
---


![device_widget.png](_images/device_widget.png)

# Device
## Name
Give your FarmBot a fun name. For example: `Broccoli Overlord` 🥦🤖

## Time Zone
Set the device's timezone.

{%
include callout.html
type="info"
title="Automatically set"
content="When you create your FarmBot web app account and login for the first time, we will automatically set your device's timezone to match your computer or phone's timezone (whichever was used to login to the account). If your FarmBot is located somewhere else, you can change the timezone setting here."
%}

## FarmBot OS
View the version of FarmBot OS that you have installed on your device, that version's release notes, and install updates if they are available using the <span class="fb-button fb-green">UPDATE</span> button. Note that the update button will display as <span class="fb-button fb-gray">UP TO DATE</span> when there are no updates available.

## FarmBot OS auto update
When enabled, FarmBot OS will periodically check for, download, and install updates automatically.

{%
include callout.html
type="success"
title="Enabled by default"
content="This setting is enabled by default so that your FarmBot will stay updated automatically with the latest features and security patches. If you decide to disable auto updates, please make sure you regularly manually update your device so that it stays within our [support policy](../../FarmBot-Software/troubleshooting/support-policy.md)."
%}

## Apply software updates
With this dropdown you can choose the hour of the day when FarmBot will apply software updates so that updates occur at a convenient time (such as the middle of the night) when you do not have any events scheduled and do not plan to be working with your FarmBot.

You may also choose the `as soon as possible` option, in which case FarmBot will install updates immediately as they become available. Note that selecting this option may cause unexpected disruptions and event execution failures.

## Auto sync
When enabled, resources such as sequences, regimens, events, plant locations, and more will be synced with FarmBot automatically as soon as they are created, changed, or deleted. This setting is enabled by default to help make your FarmBot experience streamlined and efficient.

Disabling this setting may be useful when making many changes to your resources that are not ready to be executed by FarmBot immediately.

## Camera
Select the type of camera you are using in the camera selection dropdown. Choices are `USB Camera` and `Raspberry Pi Camera`. Defaults to `USB camera`. Test by using the <span class="fb-button fb-green">take photo</span> button in the [take photo](../farmware/take-photo.md) farmware.

## Firmware
Select the firmware to be used with your electronics board.

# Power and reset
## Restart FarmBot
This will restart FarmBot's Raspberry Pi and FarmBot OS.

## Shutdown FarmBot
This will shutdown FarmBot's Raspberry Pi. To turn it back on, unplug FarmBot and plug it back in.

## Factory reset
Factory resetting your FarmBot will destroy all data on the device, revoking your FarmBot's ability to connect to your web app account and your home WiFi network. Upon factory resetting, your device will restart [Configurator](../../Device/farmbot-os/configurator.md).

Factory resetting your FarmBot will not affect any data or settings from your web app account, allowing you to do a complete restore to your device once it is back online and paired with your web app account.

## Automatic factory reset
Automatically factory reset when the WiFi network cannot be detected. Useful for network changes. Disable this setting to allow FarmBot to wait indefinitely for the configured WiFi network to come back online if it disconnects.

## Connection attempt period
For use with automatic factory reset: set the time in minutes to attempt connecting to WiFi before a factory reset.

# Diagnostic reports
Please refer to the [diagnostic reports document](diagnostic-reports.md) for more details.

# What's next?

 * [Hardware Settings](hardware-settings.md)
