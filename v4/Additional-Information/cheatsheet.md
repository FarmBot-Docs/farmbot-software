---
title: "Cheatsheet"
slug: "cheatsheet"
description: "The shortlist of commands, nomenclature, and locations to get all the FarmBot software up and running"
---

* toc
{:toc}

## For People Using Hosted Services

|Component                     |Location                      |Setup                         |Start Command                 |
|------------------------------|------------------------------|------------------------------|------------------------------|
|Web app frontend              |[my.farmbot.io](http://my.farmbot.io)|Open in browser, create an account|Open in browser, login
|Web app API/backend           |[my.farmbot.io](http://my.farmbot.io)|None                          |None
|MQTT gateway                  |[mqtt.farmbot.io](http://mqtt.farmbot.io)|None                          |None
|Controller                    |Raspberry Pi                  |None                          |None
|Firmware                      |Arduino                       |None                          |None - its always running when powered

## For Developers Running Everything Locally

|Component                     |Location                      |Git Repo                      |Final Setup Step              |Start Command                 |
|------------------------------|------------------------------|------------------------------|------------------------------|------------------------------|
|Web app frontend              |[localhost:8080](localhost:8080)|[farmbot-web-frontend](https://github.com/FarmBot/farmbot-web-frontend)|`npm install`                 |`npm start`
|Web app API/backend           |[localhost:3000](localhost:3000)|[farmbot-web-API](https://github.com/FarmBot/Farmbot-Web-API)|`bundle install`              |`MQTT_HOST=mqtt.farmbot.io rails s`
|MQTT gateway                  |[localhost:1883](localhost:1883) for MQTT direct clients (FarmBots)<br>[localhost:3002](localhost:3002) for WebSockets (web frontend/API)|[mqtt-gateway](https://github.com/FarmBot/mqtt-gateway)|?                             |?
|Controller                    |Raspberry Pi                  |[farmbot_os](https://github.com/FarmBot/farmbot_os)|WiFi Configurator             |None
|Firmware                      |Arduino                       |[farmbot-arduino-firmware](https://github.com/FarmBot/farmbot-arduino-firmware)|`ino build`<br>`ino upload`   |None - its always running when powered

