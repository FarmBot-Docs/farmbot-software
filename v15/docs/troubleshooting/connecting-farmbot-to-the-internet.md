---
title: "Connecting FarmBot to the Internet"
slug: "connecting-farmbot-to-the-internet"
description: "**Problem description:** FarmBot is having trouble connecting to the Internet or staying connected consistently."
---

Your FarmBot needs to be connected to the internet and the Web App. When everything is connected and functioning, the **connectivity popup** should show a `code 31` diagnosis code and the points on the graphic should show green. Follow this troubleshooting guide if you are having trouble getting full connectivity to your FarmBot.

![Connectivity pop-up](_images/connectivity_pop-up.png)

|Suggested steps               |Applies to                    |
|------------------------------|------------------------------|
|Step 1: [Check the connectivity popup](#step-1-check-the-connectivity-popup)|All FarmBots
|Step 2: [Check your internet connection](#step-2-check-your-internet-connection)|All FarmBots
|Step 3: [Try a Wi-Fi hotspot with a cellular network](#step-3-try-a-wi-fi-hotspot-with-a-cellular-network)|All FarmBots
|Step 4: [Check for blocked ports](#step-4-check-for-blocked-ports)|All FarmBots connecting to school or corporate networks
|Step 5: [Try a wired Ethernet connection](#step-5-try-a-wired-ethernet-connection)|All FarmBot
|Step 6: [Improve Wi-Fi signal strength](#step-6-improve-wi-fi-signal-strength)|All FarmBots

# Step 1: Check the connectivity popup

The **connectivity popup** is used to diagnose communications between the various FarmBot systems. To learn more about the connectivity popup and to get access to the full list of connectivity codes check out this page: [Connectivity Diagnosis Codes](connectivity-codes.md).

![Connectivity diagnosis code](_images/connectivity_diagnosis_code.png)

# Step 2: Check your internet connection

The first step in troubleshooting connectivity issues is to ensure that the internet connection you plan to use with FarmBot is working properly.

With cellular data (4G LTE, 5G, etc) turned **OFF**, try loading [my.farm.bot](https://my.farm.bot) on your phone or computer when connected to the internet connection you plan to use with your FarmBot. If you are not able to load webpages, then you will need to troubleshoot your internet connection before proceeding.

# Step 3: Try a Wi-Fi hotspot with a cellular network

Use your smartphone or a dedicated hotspot device from a provider like Verizon or AT&T to create a **Wi-Fi hotspot** in very close proximity to your FarmBot (within 3m or 10 feet). Ensure the hotspot device has a working cellular connection by connecting to it with a laptop or other device and loading [my.farm.bot](https://my.farm.bot). Once you are certain the hotspot is up and functional, configure FarmBot to connect to the hotspot.

If you are able to complete configuration and get your FarmBot online using the hotspot, then you can either continue to use the hotspot with your FarmBot or further troubleshoot your normal Wi-Fi network. Most likely the issue with your normal network is a [blocked port](#step-4-check-for-blocked-ports) or a [weak Wi-Fi signal](#step-6-improve-wi-fi-signal-strength).

If your FarmBot does not connect with the hotspot, there may be an issue with your hardware. However, this is an extremely rare circumstance (less than 1/1,000 FarmBots have hardware issues of this type). Almost certainly there is usually another issue at play.

# Step 4: Check for blocked ports

{%
include callout.html
type="info"
title=""
content="This solution usually only applies to FarmBots being connected to school and/or corporate networks."
%}

It is very common for the IT department of schools and corporate networks to **block ports** that are not commonly used. Just because the FarmBot is connected to the internet doesn't mean the FarmBot will be able to connect to the Web App because of these blocked ports. We have [specific instructions for your IT department](for-it-security-professionals.md) to help you connect your FarmBot to the internet if you suspect any ports are blocked.

FarmBot requires the following ports to be open on your network:

  * Port 8883 - MQTT
  * Port 80 - HTTP(S)
  * Port 443 - HTTP(S)
  * Port 3002 - WebSockets

On FarmBot Genesis v1.4+ check the Blue LED communication light. You have blocked ports if the Blue LED is OFF and the Green LED is ON. On Express v1.0+, the blue and green LEDs are located in the top right of the electronics board itself. See the [status LEDs page](../../farmbot-os/intro/status-leds.md) for more information.

![FarmBot Lights](_images/farmbot_lights.png)

# Step 5: Try a wired Ethernet connection

The most reliable way to connect FarmBot to the internet is with a **wired Ethernet connection**. This will eliminate any possibility of wireless signal interference, or weak signals causing the connection to be intermittent.

## Genesis

For Genesis kits, simply connect an Ethernet cable between the Raspberry Pi and your router. Then proceed through the configuration process and select the **Ethernet** option when prompted.

{%
include gallery.html images='
![pi 3B+ with ethernet port labeled](_images/raspberry_pi_3_b_plus_ethernet.jpeg)
![pi 4B with ethernet port labeled](_images/raspberry_pi_4_b_ethernet.jpeg)
' %}

<center><i>The Ethernet port location on the Raspberry Pi can vary.</i></center>

## Express v1.1+

For Express v1.1+ kits, simply connect an Ethernet cable between the Ethenet port on the Farmduino Express and your router. Then proceed through the configuration process and select the **Ethernet** option when prompted.

![farmduino express v1.1 with ethernet port labeled](_images/farmduino_express_ethernet.jpeg)

## Express v1.0

For Express v1.0 kits, you will need to purchase and install a **USB Ethernet hub** from a third party vendor. We recommend USB Ethernet hubs based on the `AX88179` chipset such as [this one from Adafruit](https://www.adafruit.com/product/2992). Note that depending on the hub you purchase, you may also need a [USB to microUSB adapter](https://www.amazon.com/dp/B07SDB7XY1/) to be able to plug the camera into the hub, as there is only one available microUSB port on the Raspberry Pi Zero which will be occupied by the Ethernet hub.

Please keep the following points in mind if you decide to use Ethernet on an Express device:

 * FarmBot Inc can only provide support for official, first-party hardware and we cannot guarantee that your USB Ethernet hub will operate correctly.
 * We have not tested other chipsets and do not officially support USB Ethernet installations.

Once you have connected the additional hardware, proceed through the configuration process and select the **Ethernet** option when prompted.

# Step 6: Improve Wi-Fi signal strength

The most common enemies of the Raspberry Pi Wi-Fi are other Wi-Fi networks and other electronic devices. If you are in an area with lots of other heavy duty electrical equipment such as power lines, transformers, microwaves, fridges, other appliances, radio equipment like baby monitors, or mobile phone towers, it may disrupt the Raspberry Pi Wi-Fi radio.

Here is a link with [more information on how you can improve the Wi-Fi signal](https://www.netspotapp.com/wifi-interference.html).

## Try a Wi-Fi range extender

There are multiple ways users can use a **Wi-Fi range extender** and these are a few ideas that we have:

1) Use the Wi-Fi extender to extend the Wi-Fi network coverage so that the FarmBot can connect over Wi-Fi with a stronger signal. Sometimes the Wi-Fi signal needs some help and the Wi-Fi range extender will lend a hand to boost your Wi-Fi.

2) Use both the range extender and an Ethernet cord to plug into the Raspberry Pi on the FarmBot. This will work in case it is infeasible to run an Ethernet cord from the primary router all the way to the FarmBot.

{%
include callout.html
type="warning"
title="Test the Wi-Fi range extender"
content="If you decide to try a Wi-Fi range extender, make sure you test it first to ensure it works with your network and provides adequate signal where your FarmBot is located. Test the Wi-Fi range extender by connecting to it with a laptop or other device and loading [my.farm.bot](https://my.farm.bot)."
%}

There are many range extenders and repeaters on the market and this one is just an example:

![Dell Range Extender](_images/dell_range_extender.bmp)

<center><i>Netgear Universal Wi-Fi Range Extender (WN3000RP)</i></center>

There are other resources, documentation and diagnostic Wi-Fi Apps available online to help with poor Wi-Fi signal. Check out this page by Netgear on [Wi-Fi range extenders](https://www.netgear.co.uk/home/discover/wifi-range-extender/).
