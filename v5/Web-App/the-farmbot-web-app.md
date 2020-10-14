---
title: "The FarmBot Web App"
slug: "the-farmbot-web-app"
description: "Step-by-step instructions for setting up and using the FarmBot web app"
---

* toc
{:toc}

The Farmbot Web App is a cloud based web service that performs the following functions:
 * [Farm Designer](farm-designer.md) - Drag and drop interface for farm/garden design
 * [Farm Events](farm-events.md) - Scheduling of recurring sequences of events (irrigation, seeding, etc...)
 * [Controls](controls.md) - Real time manual control of a FarmBot from a web browser
 * [Device](device.md)  - Storage of device info and calibration settings
 * [Sequences](sequences.md) - Creation of sequences of events
 * [Regimens](regimens.md) - Creation of regimens (plant-age-based scheduling of sequences of events)
 * [Tools](tools.md) - Management of the Universal Tool Mount's tools
 * [Farmware](farmware.md) - Photos and Weed Detection
 * Coming soon: crop and sensor data storage and management

{%
include callout.html
type="success"
title="At your service"
content="We offer a hosted service of the web app at [my.farmbot.io](http://my.farmbot.io). We recommend that most people use this because it is convenient, affordable, and always up-to-date with the latest features and security.

In case you want to run the application on your own servers, we show you how to do that as well near the bottom of this page."
%}



{%
include callout.html
type="info"
title="Help improve the web app"
content="Submit feature requests, bugs, and code for the web app [on GitHub](https://github.com/FarmBot/farmbot-web-app)."
%}



# Using the Web App

## Registration
1. Go to [my.farmbot.io](http://my.farmbot.io)
2. Enter an email, name, and password in the **Create an Account** section
3. Agree to the terms of use and click **Create Account**
4. Check your email and follow the link to confirm your account

## Add your FarmBot device
1. Follow the FarmBot Raspberry Pi Software installation instructions: [Raspberry Pi Software](../Device/farmbot-os.md)
2. Follow the WiFi Configurator instructions: [WiFi Configurator](../Device/configurator.md)
3. Go to [my.farmbot.io](http://my.farmbot.io) and log in.


{%
include callout.html
type="success"
title="Can you hear me now?"
content="If all has gone well, the web application should now be able to communicate with your FarmBot. You should see some logs stream into the **Logs** widget, and the device status button in the main navigation change from **Offline** to **Sync Now**."
%}

### Troubleshooting
There are three likely reasons of why your device might not connect to the web application:
1. WiFi configuration has not been completed yet or was not completed successfully.
2. Your FarmBot is not connected to the Internet. Double check that your device can connect to the Internet either over WiFi or Ethernet.

{%
include callout.html
type="success"
title="We're here to help"
content="Still having trouble? Ask a question and find answers in our [forum](http://forum.farmbot.org/)."
%}



# Web App workflow

The recommended workflow for using the web app is:
1. **Add [Tools](tools.md)**: [my.farmbot.io/app/tools](http://my.farmbot.io/app/tools)
2. **Create [Sequences](sequences.md)** for using those tools: [my.farmbot.io/app/sequences](http://my.farmbot.io/app/sequences)
3. **Create [Regimens](regimens.md)** for scheduling sequences to run at specific times: [my.farmbot.io/app/regimens](http://my.farmbot.io/app/regimens)
4. **Add plants** in the [Farm Designer](farm-designer.md): [my.farmbot.io/app/designer/plants](http://my.farmbot.io/app/designer/plants)
5. **Schedule [Farm Events](farm-events.md)**: [my.farmbot.io/app/designer/farm_events](http://my.farmbot.io/app/designer/farm_events)
6. **[Watch](controls.md#webcam-feeds) your FarmBot work!** [my.farmbot.io/app/controls](http://my.farmbot.io/app/controls)

# Provisioning the Web App



{%
include callout.html
type="warning"
title="For advanced users only"
content="The instructions below are intended for expert users and software developers who wish to run the FarmBot Web App on their own servers. This may be useful for enterprise or off-grid intranet solutions. Nontechnical users are encouraged to use the hosted service at [my.farmbot.io](http://my.farmbot.io)."
%}

Please see the official README for the web app source code [here](https://github.com/FarmBot/farmbot-web-app/blob/master/README.md).

# What's next?

 * [Tools](tools.md)
