---
title: "OTA Updates"
slug: "ota-updates"
---

* toc
{:toc}

FarmBot OS is regularly improved to include new features, security enhancements, and bug fixes. It is recommended that you keep your FarmBot updated with the latest version of FarmBot OS at all times so that you can enjoy the best that FarmBot has to offer.

By default, all FarmBots are configured to update automatically, meaning you don't have to worry about manually staying up-to-date. You do have the option to [disable automatic updates](../../Web-App/device/device-settings.md#farmbot-os-auto-update) from the device settings, though this is not recommended.

# The update process
Updates will happen **over-the-air** (OTA), meaning FarmBot will download the latest version of the software when it becomes available, apply it, and reboot as necessary. Under normal circumstances there will be no need for reconfiguration or any manual effort required by the user; FarmBot should come back online, re-sync, and resume any scheduled events automatically.

An OTA update will usually take between 15 seconds and 2 minutes to download, depending on network quality and connection speed. The update process will then take 1 to 5 minutes before FarmBot is back online and ready to start work again.

If you're experiencing OTA update issues, you can remove the microSD card from your FarmBot and [manually flash](../farmbot-os.md#installing-farmbot-os) the latest `.img` file.
