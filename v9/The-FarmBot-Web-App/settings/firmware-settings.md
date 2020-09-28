---
title: "Firmware Settings"
slug: "firmware-settings"
---

* toc
{:toc}


![Screen Shot 2020-04-22 at 4.58.31 PM.png](Screen_Shot_2020-04-22_at_4.58.31_PM.png)

# Name
Give your FarmBot a fun name. For example: `Broccoli Overlord` 🥦🤖

# Time zone
Set the device's timezone.

> 📘 Automatically set
>
> When you create your FarmBot web app account and login for the first time, we will automatically set your device's timezone to match your computer or phone's timezone (whichever was used to login to the account). If your FarmBot is located somewhere else, you can change the timezone setting here.

# Camera
Select the type of camera you are using in the camera selection dropdown. Choices are `USB Camera` and `Raspberry Pi Camera`. Defaults to `USB camera`. Test by using the <span class="fb-button fb-green">take photo</span> button in the [take photo](../../The-FarmBot-Web-App/farmware/take-photo.md) farmware.

# Firmware
Select the firmware to be used with your electronics board.

# Update time
With this dropdown you can choose the hour of the day when FarmBot will apply software updates so that updates occur at a convenient time (such as the middle of the night) when you do not have any events scheduled and do not plan to be working with your FarmBot.

You may also choose the `As soon as possible` option, in which case FarmBot will install updates immediately as they become available. Note that selecting this option may cause unexpected disruptions and event execution failures.

# Auto update
When enabled, FarmBot OS will automatically download and install software updates at the chosen time.

{%
include callout.html
type="success"
title="Enabled by default"
content="This setting is enabled by default so that your FarmBot will stay updated automatically with the latest features and security patches. If you decide to disable auto updates, please make sure you regularly manually update your device so that it stays within our [support policy](../../Extras/troubleshooting/support-policy.md)."
%}

# FarmBot OS
View the version of FarmBot OS that you have installed on your device, that version's release notes, and install updates if they are available using the <span class="fb-button fb-green">UPDATE</span> button. Note that the update button will display as <span class="fb-button fb-gray">UP TO DATE</span> when there are no updates available.

# Auto sync
When enabled, resources such as sequences, regimens, events, plant locations, and more will be synced with FarmBot automatically as soon as they are created, changed, or deleted. This setting is enabled by default to help make your FarmBot experience streamlined and efficient.

> 📘
>
> Disabling this setting may be useful when making many changes to your resources that are not ready to be executed by FarmBot immediately.
