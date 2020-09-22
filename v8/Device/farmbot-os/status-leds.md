---
title: "Status LEDs"
slug: "status-leds"
excerpt: "The meaning behind the blinking"
---

* toc
{:toc}

The Raspberry Pi has two LED lights that convey information about its status.

![RASPBERRY_PI_LIGHTS.jpg](RASPBERRY_PI_LIGHTS.jpg)

# Red (power) LED

|Red (power)                   |Status                        |Tips                          |
|------------------------------|------------------------------|------------------------------|
|<span class="fa fa-circle" style="color: red; opacity: 1"></span> (solid red)|OK                            |Good to go!
|<span class="fa fa-sun-o" style="color: red; opacity: 1"></span> (blinking red)|Low power                     |Try a more powerful power supply or a different cable.
|<span class="fa fa-circle-thin" style="color: red; opacity: 1"></span>  (off)|No power / low power          |Plug in to a 5V, 3A power supply.

# Green (activity) LED

|Green (activity)              |Status                        |Tips                          |
|------------------------------|------------------------------|------------------------------|
|<span class="fa fa-circle" style="color: green; opacity: 1"></span> (solid green)|Busy                          |Working/booting
|<span class="fa fa-sun-o" style="color: green; opacity: 1"></span> (blinking randomly)|Busy                          |Working/booting
|<span class="fa fa-sun-o" style="color: green; opacity: 1"></span> (blinking consistently)|Network disconnected or emergency stopped|[Configure FarmBot](../farmbot-os/configurator.md), press <span class="fb-button fb-yellow">UNLOCK</span> in the Web App, or check that the network FarmBot is connected to is online.
|<span class="fa fa-circle-thin" style="color: green; opacity: 1"></span> (off)|Ready                         |Waiting for the next task



# Electronics Box LEDs

In addition to the LEDs located on the Raspberry Pi, Genesis v1.4+ kits feature LEDs mounted on top of the electronics box.

![LEDs.png](LEDs.png)

## LED 1
This green LED indicates the **sync status** between FarmBot and the web app. It is connected to Raspberry Pi GPIO BCM pin 24.

|Green (sync)                  |Status                        |Tips                          |
|------------------------------|------------------------------|------------------------------|
|<span class="fa fa-circle" style="color: green;opacity: 1"></span> (solid green)|Synced                        |Ready
|<span class="fa fa-sun-o" style="color: green;opacity: 1"></span> (blinking slowly)|Needs sync                    |Will not execute any unsynced events or sequences
|<span class="fa fa-sun-o" style="color: green;opacity: 1"></span> (blinking quickly)|Syncing                       |
|<span class="fa fa-circle-thin" style="color: green;opacity: 1"></span> (off)|Offline                       |Check the connection status LED

## LED 2
This blue LED indicates the **connection status** between FarmBot and the internet and web app. It is connected to Raspberry Pi GPIO BCM pin 25.

|Blue (connection)             |Status                        |Tips                          |
|------------------------------|------------------------------|------------------------------|
|<span class="fa fa-circle" style="color: blue;opacity: 1"></span> (solid blue)|Connected                     |Working
|<span class="fa fa-sun-o" style="color: blue;opacity: 1"></span> (blinking slowly)|Needs configuration           |[Configure FarmBot](../farmbot-os/configurator.md), press <span class="fb-button fb-yellow">UNLOCK</span> in the Web App, or check that the network FarmBot is connected to is online.
|<span class="fa fa-circle-thin" style="color: blue;opacity: 1"></span> (off)|Offline                       |Check your internet connection.<br><br>If you are connected to the internet but the Blue LED is off, one or more of your ports may be blocked. Get your network administrator to check the ports listed in the [Firewall is blocking network traffic](https://software.farm.bot/docs/connecting-farmbot-to-the-web-app#section-6-firewall-is-blocking-network-traffic) troubleshooting section.

## LED 3
This white LED is user controllable via the <span class="fb-step fb-write-pin">Control Peripheral</span> sequence command. It is connected to Raspberry Pi GPIO BCM pin 12.

## LED 4
This white LED is user controllable via the <span class="fb-step fb-write-pin">Control Peripheral</span> sequence command. It is connected to Raspberry Pi GPIO BCM pin 13.

## Button 1 LED
This red LED indicates if FarmBot is **E-STOPPED** or not. It is connected to Raspberry Pi GPIO BCM pin 17.

|Red (E-stop)                  |Status                        |Tips                          |
|------------------------------|------------------------------|------------------------------|
|<span class="fa fa-circle" style="color: red;opacity: 1"></span> (solid red)|Unlocked                      |Ready
|<span class="fa fa-circle-thin" style="color: red;opacity: 1"></span> (off)|Locked                        |Check the Button 2 LED status

## Button 2 LED
This yellow LED indicates if FarmBot is **UNLOCKED** or not. It is connected to Raspberry Pi GPIO BCM pin 23.

|Yellow (unlock)               |Status                        |Tips                          |
|------------------------------|------------------------------|------------------------------|
|<span class="fa fa-sun-o" style="color: orange;opacity: 1"></span> (blinking)|Locked                        |When safe to do so, press this button to unlock FarmBot.
|<span class="fa fa-circle-thin" style="color: orange;opacity: 1"></span> (off)|Unlocked                      |Ready

