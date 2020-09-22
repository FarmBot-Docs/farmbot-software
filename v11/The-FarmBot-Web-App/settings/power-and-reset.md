---
title: "Power and Reset"
slug: "power-and-reset"
excerpt: "[Open these settings in the app](https://my.farm.bot/app/designer/settings?highlight=power_and_reset)"
---

* toc
{:toc}


![Screen Shot 2020-08-25 at 10.38.08 AM.png](Screen_Shot_2020-08-25_at_10.38.08_AM.png)

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
content="If you are experiencing problems with your setup, we do not recommend performing a soft reset. Instead, perform a [hard reset](#section-hard-reset)."
%}

# Hard reset

Hard resetting your FarmBot will erase all data from the device, allowing you to start from a clean slate. **This is recommended if you are experiencing problems with your setup.**

Perform a hard reset by [reflashing the latest version of FarmBot OS onto the microSD card](doc:farmbot-os#section-installation). Upon hard resetting, you will need to [reconfigure FarmBot](http://configure.farm.bot) to connect it to internet and your web app account.

{%
include callout.html
type="success"
title="Your web app data is safe"
content="Hard resetting your FarmBot will not affect any of your data or settings from your web app account, allowing you to do a complete restore to your device once it is back online and paired with your web app account."
%}

# Automatic soft reset
Automatically soft reset when the WiFi network cannot be detected. Useful for network changes. Keep this setting disabled to allow FarmBot to wait indefinitely for the configured WiFi network to come back online if it disconnects.

# Connection attempt period
For use with automatic soft reset: set the time in minutes to attempt connecting to WiFi before a soft reset.
