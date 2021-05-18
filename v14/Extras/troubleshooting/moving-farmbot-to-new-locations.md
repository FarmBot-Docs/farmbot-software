---
title: "Moving FarmBot to New Locations"
slug: "moving-farmbot-to-new-locations"
---

* toc
{:toc}

FarmBot is a fun platform to share with others and offers a great deal of crowd appeal at events such as fairs and trade shows. Many FarmBot users, particularly those in STEM education, will move their devices to new locations using [mobile garden beds](https://genesis.farm.bot/docs/mobile-raised-bed) or removable trays. This document outlines considerations to account for when moving FarmBot to a new location.

# Check network conditions before moving the device

WiFi problems are the most common issue at trade shows and exhibitions. FarmBot has network requirements that differ from traditional desktop computers. This means that FarmBot might not work on the WiFi at your new location, even though your laptop can connect to the internet. This can be especially stressful if you are operating on tight event deadlines. **To prevent delays and unforeseen technical difficulties, ALWAYS test WiFi at the remote site before proceeding with installation.**

## Testing the WiFi with a detached device

Public WiFi networks, particularly those used in large exhibition halls and open spaces may have security software to prevent "suspicious activity". This has historically been a problem for FarmBot, as it requires access to ports that are rarely used by desktop computers. It also operates with an antenna that may have lower reception than a laptop.

Before moving equipment to the new location, it is best to do a test run of the FarmBot hardware. To run this test you will need:

 * A Raspberry Pi computer, temporarily detached from the FarmBot electronics box with no peripherals connected.
 * A USB power supply and cable that is compatible with the Raspberry Pi.
 * An SD Card with the [latest version of FarmBot OS](https://my.farm.bot/os) installed.
 * A Windows or Mac laptop for running configurator.

Once you have the required materials, you are ready to perform a network test. Power on the RasperryPi with the SD card inserted and [follow the configurator instructions](../../FarmBot-OS/farmbot-os/configurator.md) as usual.

Once you have finished configuration, you should be able to log in to your FarmBot account and see the device listed as being connected. **The Arduino (device Firmware) will be listed as offline, since the RaspberryPi has no peripherals attached.** All other systems should show as green in the [connectivity panel](connectivity-codes.md).

## Identifying network problems

If your device does not come online after configuration, this may be a sign that the WiFi is not suitable for use with FarmBot. There are two means of rectifying the situation:

 * Contact IT staff and ask about security software that blocks outbound access to internet protocols such as HTTP, DNS, NTP, MQTT and AMQP. FarmBot has prepared a document to assist IT professionals [here](for-it-security-professionals.md).
 * Purchase a commercial wireless hotspot that exposes a WiFi network which FarmBot can reliably use. Please note that FarmBot does not currently support USB tethering - the hotspot must expose a WiFi network.
 * Use a phone to create a wireless hotspot using your cellular data connection. Note that you may want to disable automatic software updates during the event to avoid increased data usage.
