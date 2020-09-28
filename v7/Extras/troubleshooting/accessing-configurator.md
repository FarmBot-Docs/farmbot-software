---
title: "Accessing Configurator"
slug: "accessing-configurator"
excerpt: "Problem description: I'm trying to configure my FarmBot but I do not see the `farmbot-xxxx` WiFi network."
---

* toc
{:toc}

# 1. Install FarmBot OS
[Flash the latest version of FarmBot OS](../../Device/farmbot-os.md#installing-farmbot-os) onto the microSD card and then insert the microSD card into the Raspberry Pi. *Note that FarmBot kits do not come with an OS pre-installed.*

# 2. Check the Raspberry Pi's power
Make sure that your FarmBot's power supply is plugged into grid power and that the outlet and optional extension cord you are using are working properly. If you are plugged into a GFCI protected outlet, ensure it has not been tripped. Then check all connections between the power supply and the Raspberry Pi ensuring that polarity is correct, connections are solid, and plugs are fully inserted into receptacles. Once everything is plugged in, refer to the [Raspberry Pi status LEDs](https://software.farm.bot/docs/farmbot-os#raspberry-pi-status-leds) to verify that the Raspberry Pi is receiving adequate power. If the Pi is not receiving adequate power, then some parts may need replacement. Please contact us at [support@farm.bot](mailto:support@farm.bot).

{%
include callout.html
type="info"
title="Using an off-grid power system?"
content="At this time we cannot provide support for off-grid power systems. If you are using an off-grid system and the Raspberry Pi is not receiving adequate power, please consult an electrician for additional help."
%}

# 3. Search for the `farmbot-xxxx` network with a WiFi enabled device
If you've installed FarmBot OS and ensured the Raspberry Pi is receiving adequate power, then FarmBot should now be in configuration mode and broadcasting a WiFi network named `farmbot-xxxx`. Please note: it can take up to 2 minutes from turning on the power until when the FarmBot is broadcasting the network.

Use a smartphone, tablet, or laptop to look for the `farmbot-xxxx` WiFi network. Ensure that WiFi is enabled on your smartphone, tablet, or laptop (no airplane mode). If you don't see the `farmbot-xxxx` network immediately, allow up to 2 minutes for your smartphone, tablet, or laptop to complete its search. Also, ensure that you are physically close enough to connect to the FarmBot (5-10 meters without any walls in the way is a good distance).

Once you find the `farmbot-xxxx` WiFi network, connect to it and follow the detailed configuration instructions [here](../../Device/farmbot-os/configurator.md#configure-farmbot).

If you do not see the `farmbot-xxxx` WiFi network, try again with a different smartphone, tablet, or laptop. If you still cannot find the network, move on to the next troubleshooting step.

# 4. Try a different microSD card
It is possible for the microSD card to become corrupted and unusable. If you have tried the steps above and did not ever find the `farmbot-xxxx` WiFi network, try installing FarmBot OS onto a different microSD card and attempting to connect again.

If this does not work or you do not have an extra microSD card to try with, please contact us at [support@farm.bot](mailto:support@farm.bot).

# 5. I'm connected to `farmbot-xxxx` but can't load the configurator
If you are using a smartphone you may need to disable cellular data to allow your phone's browser to connect to the configurator instead of the Internet.

If you experience a site connection error in the browser, try navigating to [192.168.24.1](http://192.168.24.1) instead of [setup.farm.bot](http://setup.farm.bot).

Please use a modern, updated web browser. We recommend Google Chrome.
