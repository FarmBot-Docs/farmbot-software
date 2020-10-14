---
title: "Connecting FarmBot to the Web App"
slug: "connecting-farmbot-to-the-web-app"
description: "Problem description: I completed all steps of the [configuration process](../../Device/farmbot-os/configurator.md) and now I'm waiting for FarmBot to connect to the web application."
---

* toc
{:toc}

# 1. Ensure you have created a web app account
You must create a web app account at [my.farm.bot](http://my.farm.bot) prior to completing the configuration process. Otherwise your FarmBot will try to connect with account credentials that do not yet exist.

{%
include callout.html
type="success"
title="Don't forget to verify your email address"
content="After creating a web app account, you must also verify that you control the email address you used to make the account. Please check your email and click the verification link we sent you."
%}

# 2. Reconnect to the Internet and be patient
Immediately after completing configuration, FarmBot will disable the `farmbot-xxxx` WiFi network. Check to make sure that your smartphone, tablet, or laptop reconnects to your normal WiFi network (with Internet access), as this might not happen automatically or quickly. Then use your web browser to load the web app ([my.farm.bot](https://my.farm.bot)). If you already had the web app loaded in a tab, refresh the tab.

It usually takes about 2 minutes after completing configuration for FarmBot to boot up, connect to the internet (over WiFi or Ethernet), connect to the web application, and finish the initialization process. If you have waited at least 2 minutes since completing configuration and do not see the FarmBot online in the web app, move on to the next step.

# 3. Incorrect web app credentials
If you mistyped your web application credentials (email and/or password) during configuration, then FarmBot will not be able to connect to your web application account to send and receive messages. If this occurred, then FarmBot will automatically restart into configuration mode, allowing you to try again.

# 4. Incorrect WiFi credentials
If you mistyped your WiFi credentials (network name and/or password) during configuration, then FarmBot will not be able to connect to the Internet to send and receive messages. If this occurred, then FarmBot will automatically restart into configuration mode, allowing you to try again.

# 5. WiFi is out of range
If your FarmBot is too far from your WiFi router, then it will not be able to find the network and/or reliably connect to the Internet to send and receive messages. If this occurred, then FarmBot will automatically restart into configuration mode. We recommend installing a WiFi repeater or connecting the FarmBot to your WiFi router directly with an Ethernet cable.

# 6. Firewall is blocking network traffic
If you are installing FarmBot at a school or company with restricted network access (firewall), then FarmBot may not be able to fully connect to the web application to send and receive messages. Tell your network administrator that FarmBot needs access to ports `5672` (AMQP), `1883` (MQTT), `8883` (MQTT over SSL), `80` (HTTP), and `443` (HTTPS) in order to function correctly. Additionally, the FarmBot device also requires outbound access to two redundant NTP servers for setting the system clock: `0.pool.ntp.org` and `1.pool.ntp.org`. The servers are based in the United States. The services are provided on `UDP port 123`. Obstructed access to these servers is another common pitfall when operating a FarmBot behind a firewall. You may also want to send your network admin [this page](for-it-security-professionals.md), which contains additional details for allowing FarmBot to work with a firewall.

{%
include callout.html
type="success"
title="We're here to help"
content="Still having trouble? Ask a question and find answers in the [forum](http://forum.farmbot.org/)."
%}

