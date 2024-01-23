---
title: "Accessing Configurator"
slug: "accessing-configurator"
description: "**Problem description:** I'm trying to configure my FarmBot but I do not see the `farmbot-xxxx` WiFi network."
---

# 1. Reflash FarmBot OS

[Reflash the latest version of FarmBot OS](../../farmbot-os/intro.md) onto the microSD card and then insert the microSD card into the Raspberry Pi. **Take special care to ensure that you have downloaded the correct version of FarmBot OS for the FarmBot kit you have.**

{%
include callout.html
type="warning"
content="Configurator will **not** start if you do not flash the microSD card using the special **Etcher** program. Always follow the [installation instructions](../../farmbot-os/intro.md) and do not skip steps."
%}

# 2. Try a different microSD card

It is possible for the microSD card to become corrupted and unusable. If you have tried the step above and did not ever find the `farmbot-xxxx` WiFi network, try flashing FarmBot OS onto a different microSD card and attempting to connect again.

{%
include callout.html
type="warning"
title="Do not use large capacity microSD cards"
content="FarmBot OS will not work with microSD cards larger than 32GB in capacity. Please use a microSD card 32GB or smaller. We recommend 8GB."
%}

If this does not work or you do not have an extra microSD card to try with, please contact us at [contact@farm.bot](mailto:contact@farm.bot).

# 3. Check the Raspberry Pi's power

Make sure that your FarmBot's power supply is plugged into grid power and that the outlet and optional extension cord you are using are working properly. If you are plugged into a GFCI protected outlet, ensure it has not been tripped. Then check all connections between the power supply and the Raspberry Pi ensuring that polarity is correct, connections are solid, and plugs are fully inserted into receptacles. Once everything is plugged in, refer to the [Raspberry Pi status LEDs](../../farmbot-os/intro/status-leds.md) to verify that the Raspberry Pi is receiving adequate power. If the Pi is not receiving adequate power, then some parts may need replacement. Please contact us at [contact@farm.bot](mailto:contact@farm.bot).

{%
include callout.html
type="bolt"
title="Using an off-grid power system?"
content="At this time we cannot provide support for off-grid power systems. If you are using an off-grid system and the Raspberry Pi is not receiving adequate power, please consult an electrician for additional help."
%}

# 4. Search for the farmbot-xxxx network with a WiFi enabled device

If you've installed FarmBot OS and ensured the Raspberry Pi is receiving adequate power, then FarmBot should now be in configuration mode and broadcasting a WiFi network named `farmbot-xxxx`.

{%
include callout.html
type="clock-o"
title="Be patient"
content="It can take up to 2 minutes from turning on the power until when the FarmBot is broadcasting the network."
%}

Use a smartphone, tablet, or laptop to look for the `farmbot-xxxx` WiFi network. Ensure that WiFi is enabled on your smartphone, tablet, or laptop (no airplane mode). If you don't see the `farmbot-xxxx` network immediately, allow up to 2 minutes for your smartphone, tablet, or laptop to complete its search. Also, ensure that you are physically close enough to connect to the FarmBot (5-10 meters without any walls in the way is a good distance).

Once you find the `farmbot-xxxx` WiFi network, connect to it and follow the detailed configuration instructions [here](../../farmbot-os/intro/configurator.md).

If you do not see the `farmbot-xxxx` WiFi network, try again with a different smartphone, tablet, or laptopx.

# 5. I'm connected to farmbot-xxxx but can't load the configurator

If you are using a smartphone you may need to disable cellular data to allow your phone's browser to connect to the configurator instead of the Internet.

If you experience a site connection error in the browser, try navigating to [192.168.24.1](http://192.168.24.1) instead of [setup.farm.bot](http://setup.farm.bot).

Please use a modern, updated web browser. We recommend Google Chrome.
