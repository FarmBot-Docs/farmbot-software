---
title: "Cheatsheet"
slug: "cheatsheet"
excerpt: "The shortlist of commands, nomenclature, and locations to get all the FarmBot software up and running"
---

* toc
{:toc}

## For People Using Hosted Services

|Component                     |Location                      |Setup                         |Start Command                 |
|------------------------------|------------------------------|------------------------------|------------------------------|
|Web app frontend              |[my.farmbot.io](http://my.farmbot.io)|Open in browser, create an account|Open in browser, login
|Web app API/backend           |[my.farmbot.io](http://my.farmbot.io)|None                          |None
|Message broker                |                              |None                          |None
|Controller (FarmBot OS)       |Raspberry Pi                  |[Configurator](../FarmBot OS/farmbot-os/configurator.md)|None
|Firmware                      |Arduino                       |None                          |None - its always running when powered

## For Developers Running Everything Locally

|Component                     |Location                      |Git Repo                      |Final Setup Step              |Start Command                 |
|------------------------------|------------------------------|------------------------------|------------------------------|------------------------------|
|Web app frontend              |[localhost:3000](localhost:3000)|[Farmbot-Web-App](https://github.com/FarmBot/Farmbot-Web-App)|`yarn install`                |`rails api:start`
|Web app API/backend           |[localhost:3000](localhost:3000)|[Farmbot-Web-App](https://github.com/FarmBot/Farmbot-Web-App)|`bundle install`              |None
|Message broker                |[localhost:3002](localhost:3002)|[Farmbot-Web-App](https://github.com/FarmBot/Farmbot-Web-App)|None                          |`rails mqtt:start`
|Controller                    |Raspberry Pi                  |[farmbot_os](https://github.com/FarmBot/farmbot_os)|[Configurator](../FarmBot OS/farmbot-os/configurator.md)|None
|Firmware                      |Arduino                       |[farmbot-arduino-firmware](https://github.com/FarmBot/farmbot-arduino-firmware)|None                          |None - its always running when powered

