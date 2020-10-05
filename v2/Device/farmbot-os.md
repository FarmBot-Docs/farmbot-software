---
title: "FarmBot OS"
slug: "farmbot-os"
description: "Step-by-step instructions for installing FarmBot OS onto the Raspberry Pi"
---

* toc
{:toc}

The Raspberry Pi is the brain of your FarmBot and has software installed on it that allows it to:

* Communicate with the web application via MQTT over WiFi or ethernet in order to synchronize (download) the latest schedules and sequences, and upload the latest logs and sensor data.
* Communicate with the Arduino over USB to send G and F commands and receive sensor data
* Take photos with a USB web cam, and stream video back to the web application

The Raspberry Pi will need to have FarmBot OS installed in order for FarmBot to work:

FarmBot OS is all the software FarmBot needs already bundled together: [farmbot_os](https://github.com/FarmBot/farmbot_os)

It includes a WiFi configurator component that allows the Pi to create its own WiFi network whenever it cannot connect to the Internet. This allows you to enter WiFi and web app credentials from your laptop, phone, or tablet, which means you never need to hook up a keyboard or monitor to the Raspberry Pi.

{%
include callout.html
type="info"
title="Another computer is required"
content="You will need another computer with a microSD card reader to install the Raspberry Pi OS."
%}



{%
include callout.html
type="success"
title="Help improve the FarmBot Raspberry Pi software"
content="Submit feature requests, bugs, and code on GitHub for the [FarmBot OS](https://github.com/FarmBot/farmbot_os)"
%}



# Installing FarmBot OS

In this method, we will install FarmBot OS - an operating system with all the software FarmBot needs bundled together in one package. Once you install FarmBot OS onto your Raspberry Pi, everything should be good to go.

## Step 1: Download FarmBot OS
Download the latest FarmBot OS image file [here](https://github.com/FarmBot/farmbot_os/releases).

## Step 2. Write FarmBot OS to the microSD card
You need to use an image writing tool to install FarmBot OS onto your microSD card. Follow the instructions provided by RaspberryPi.org for your operating system:

* [Linux](https://www.raspberrypi.org/documentation/installation/installing-images/linux.md)
* [Mac OS](https://www.raspberrypi.org/documentation/installation/installing-images/mac.md)
* [Windows](https://www.raspberrypi.org/documentation/installation/installing-images/windows.md)

## Step 3. Prepare the Raspberry Pi
* Plug your microSD card into the Raspberry Pi
* Plug your Arduino into the Raspberry Pi with a USB cable
* Optional: plug in a USB camera to the Raspberry Pi

## Step 4. Turn on the Raspberry Pi
Plug in the power source to the Raspberry Pi. Depending on your setup, power will be coming from either a standard microUSB cable plugged into a standalone power supply, from a DC/DC buck converter coming from your RAMPS shield, or from a DC/DC buck converter coming straight from your FarmBot's power supply. Note: The power supplied must be rated to 5V and at least 1A, though 2A is recommended.

## Step 5. Configure your FarmBot
Use the FarmBot Configurator (for details, see [FarmBot Configurator](configurator.md)):
* Using a phone, tablet or laptop, search for the WiFi network 'farmbot-xxxx'.
* Connect to that and open a web browser to http://192.168.24.1/
* Follow the on screen instructions to configure your FarmBot. Once you save your configuration FarmBot will connect to your home WiFi network and to the FarmBot web application.

{%
include callout.html
type="warning"
title=""
content="If you are using a smartphone you may need to disable cellular data to allow your phone's browser to connect to the configurator."
%}



{%
include callout.html
type="success"
title="Check the web app"
content="If all has gone well during your setup, you should now see your FarmBot 'Online' in the web application interface."
%}


# What's next?

 * [Configurator](configurator.md)
