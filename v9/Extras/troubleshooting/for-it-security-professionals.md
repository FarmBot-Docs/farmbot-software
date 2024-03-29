---
title: "For IT Security Professionals"
slug: "for-it-security-professionals"
---

FarmBot requires access to various servers to operate properly.

The first server is the web server (HTTPS). The servers are operated in the United States by Heroku, a Salesforce subsidiary. Heroku subcontracts their infrastructure services to Amazon Web Services (AWS). The servers reside in Amazon's `us-east-1` region, which is located in Virginia. The server uses the domains `my.farm.bot` and `my.farmbot.io`. Both domains point to the same server. Services are provided on TCP port 443 (HTTPS and WSS). Heroku does not provide lists of IP ranges, but they should mirror Amazon's us-east-1 IP ranges. We do not have control over IP allocation, but the most up-to-date list can be found [here](https://docs.aws.amazon.com/general/latest/gr/aws-ip-ranges.html). Our DNS server is `herokudns.com`.

The second server is the real-time message broker, which runs the RabbitMQ software package. It is also hosted on Amazon Web Services United States region by CloudAMQP, a hosting provider specializing in RabbitMQ message brokers. Like our web servers, the message broker is hosted within Amazon's `us-east-1` data center. The server's public domain name is `clever-octopus.rmq.cloudamqp.com`. Web browsers require *long-running access* to this server on TCP port 443. FarmBot devices require long-running access to this domain on TCP port 5672.

{%
include callout.html
type="info"
title="Long-running connections are required"
content="Connections to this server will be kept open for long periods of time via the WebSocket protocol. This is critical to the smooth operation of the device. From the perspective of your security software, it will appear as a long-running HTTPS connection. It is important that your security software does not prematurely close this socket. Disallowing the use of WebSockets or attempting to close sockets after a timeout is a common obstacle to smooth device operation in an enterprise setting."
%}

The FarmBot device also requires outbound access to two redundant NTP servers for setting the system clock: `0.pool.ntp.org` and `1.pool.ntp.org`. The servers are based in the United States. The services are provided on UDP port 123. **Obstructed NTP access is an extremely common source of FarmBot failures in an enterprise setting**.

Web content is delivered by the following third parties. All content is transferred over HTTPS (TCP port 443):

* `farmbot-production.storage.googleapis.com` - FarmBot photograph storage.
* `openfarm.cc` - Crop knowledge database
* `maxcdn.bootstrapcdn.com` - Visual stylesheet assets for UI.
* `fonts.googleapis.com` and `fonts.gstatic.com` - UI font files.
* `device.nerveshub.org` - FarmBotOS software release information.
* `api.github.com` - FarmBot OS software release information.
* `raw.githubusercontent.com` - Hosting of device plugins, such as the weed detector

The servers in the list above do not require long-running access. They simply open a connection and close it upon completion, which should not take more than a few seconds.

# Security practices

Data in transit is encrypted via SSL and HTTPS (WSS:// in the case of WebSockets). AMQP traffic uses TLS managed by CloudAMQP. The web application implements an HTTP content security policy (CSP) to avoid exfiltration of data by malicious scripts on the end user's machine. Software updates are run at least once a month. Our source control hosting vendor (Github) provides us with real-time security alerts when vulnerabilities are found in libraries used by the application. Staff is on-call 24 hours a day to apply security patches. The authenticity of the server's HTTPS certificate is managed by Let's Encrypt, our certificate authority. Passwords are hashed using [Devise](https://github.com/plataformatec/devise), the most common user authentication library for Ruby on Rails applications.

# IP addressing

FarmBot does not require a fixed IP address. DHCP is the preferred method of assigning an IP to a device. Due to internal network configuration variation, some organizations may need to assign a static IP to a device, although this is less common.

# Proxy Servers

As of November 2019, **FarmBot does not support the use of proxy servers**, although we do plan to support the use of proxies in a future version of FarmBot OS. Please see this [discussion on Github](https://github.com/FarmBot/farmbot_os/issues/909) for more information.

# "Rogue" Access Points

Some users, particularly schools and larger organizations, have reported their devices as being blacklisted by their security software because the security software categorizes it as a ["rogue access point"](https://en.wikipedia.org/wiki/Rogue_access_point). Please ensure that your security software does not identify FarmBot's WiFi configurator as a rogue access point.

# Enterprise WiFi Support

FarmBot does not support enterprise WiFi at this time.

# Other security concerns

Please let us know if you have any other security concerns by emailing contact@farm.bot, or opening an issue on GitHub.
