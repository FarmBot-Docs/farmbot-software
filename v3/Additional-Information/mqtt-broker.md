---
title: "MQTT Gateway"
slug: "mqtt-broker"
description: "The intermediary for all messages between FarmBot devices and the web app"
---

The **MQTT Gateway** is a cloud application that acts as an intermediary for all messages between the FarmBot web app and FarmBot devices. It handles socket connections, device identification, and authentication.

{%
include callout.html
type="success"
title="At your service"
content="We offer a hosted MQTT Gateway service at [mqtt.farmbot.io](http://mqtt.farmbot.io). We recommend that most people use this because it is convenient, free, and always up-to-date with the latest features and security."
%}



{%
include callout.html
type="info"
title="Help improve this software"
content="Submit feature requests, bugs, and code for [on GitHub](https://github.com/FarmBot/mqtt-gateway)."
%}



# Using the MQTT Gateway

## Use the Hosted MQTT Gateway with the Hosted Web App (Easy)
The hosted web app at my.farmbot.io is already configured to to use the hosted MQTT Gateway service at mqtt.farmbot.io. All you have to do is enter in your web app credentials using the FarmBot OS WiFi Configurator, and then your FarmBot will be able to talk to the web app over MQTT. All of the configuration needed for your FarmBot will be stored in the authentication token that the web app gives to your FarmBot during setup.

## Self Provision an MQTT Gateway to be used with a Self-Provisioned Web App (Difficult)

{%
include callout.html
type="info"
title="See GitHub for details"
content="To configure your web app installation, see the GitHub README: [https://github.com/FarmBot/Farmbot-Web-API](https://github.com/FarmBot/Farmbot-Web-API)

If you have any troubles, please raise an issue on GitHub so we can address the problem and help you out!"
%}

