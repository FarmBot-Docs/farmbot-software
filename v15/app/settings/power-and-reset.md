---
title: "Power and Reset"
slug: "power-and-reset"
description: ":electric_plug: Reboot, reconfigure, and shutdown FarmBot.\n[Open these settings in the app](https://my.farm.bot/app/designer/settings?highlight=power_and_reset)"
---


# Restart FarmBot

This will restart FarmBot's Raspberry Pi and FarmBot OS.

# Shutdown FarmBot

This will shutdown FarmBot's Raspberry Pi. To turn it back on, unplug FarmBot and plug it back in.

# Soft reset

Soft resetting your FarmBot will revoke your FarmBot's ability to connect to your web app account and your home WiFi network. **This is useful before moving FarmBot to a new location with a different WiFi network, or when switching FarmBot from one web app account to another.**

Upon soft resetting, you will need to [reconfigure FarmBot](http://configure.farm.bot) to connect it to internet and your web app account.

{%
include callout.html
type="success"
title="Your web app data is safe"
content="Soft resetting your FarmBot will not affect any of your data or settings from your web app account, allowing you to do a complete restore to your device once it is back online and paired with your web app account."
%}

{%
include callout.html
type="info"
title=""
content="If you are experiencing problems with your setup, we do not recommend performing a soft reset. Instead, perform a [hard reset](#hard-reset)."
%}

# Hard reset

Hard resetting your FarmBot will erase all data from the device, allowing you to start from a clean slate. **This is recommended if you are experiencing problems with your setup.**

Perform a hard reset by [reflashing the latest version of FarmBot OS onto the microSD card](../../farmbot-os/intro.md). Upon hard resetting, you will need to [reconfigure FarmBot](http://configure.farm.bot) to connect it to internet and your web app account.

{%
include callout.html
type="success"
title="Your web app data is safe"
content="Hard resetting your FarmBot will not affect any of your data or settings from your web app account, allowing you to do a complete restore to your device once it is back online and paired with your web app account."
%}
