---
title: "FarmBot OS"
slug: "farmbot-os"
description: "Step-by-step instructions for installing FarmBot OS :movie_camera: [Video tutorial](https://youtu.be/AOsF17Yxoi4?t=9)\nDownload the latest FarmBot OS `.img` file [here](http://os.farm.bot)."
---

* toc
{:toc}

The Raspberry Pi runs a custom operating system named **FarmBot OS**, allowing FarmBot to:

* Communicate with the web application over WiFi or ethernet so that it can synchronize (download) sequences, regimens, farm designs, events, and more; upload logs and sensor data; and accept real-time commands.
* Communicate with the Farmduino to send G and F commands and receive sensor and encoder data.
* Take photos with a USB or Raspberry Pi camera, and upload the photos to the web application.
* Get configured over WiFi, mitigating the need to plug in a mouse, keyboard, or screen.

# Installing FarmBot OS



{%
include callout.html
type="success"
title="Pre-installed"
content="FarmBot OS comes pre-installed with all Genesis v1.5+ and Express v1.0+ FarmBots. If you have an older FarmBot model or need to manually install FarmBot OS for another reason, continue reading!"
%}



{%
include callout.html
type="info"
title="Another computer is required"
content="You will need another computer with a microSD card reader to install FarmBot OS."
%}

## Step 1: Download FarmBot OS
Download the latest FarmBot OS `.img` file [here](http://os.farm.bot).

## Step 2. Write FarmBot OS onto the microSD card
You must use a `.img` writing tool to write FarmBot OS onto the microSD card. We recommend downloading and installing [Etcher](https://etcher.io/) for this purpose. Once you have Etcher installed, open it up and select the FarmBot OS `.img` file and write it to the microSD card.

{%
include callout.html
type="warning"
title="Drag and drop will not work"
content="Using your typical file browser (Finder on Mac or File Explorer on Windows) to drag and drop or copy and paste the FarmBot OS `.img` file onto the microSD card **will not work**. You *must* use a tool such as Etcher as described above."
%}

## Step 3. Insert the microSD card into the Raspberry Pi
Insert the microSD card into the back side of the Raspberry Pi.

{%
include callout.html
type="success"
title="No need to remove the Raspberry Pi"
content="You do not need to remove the Raspberry Pi from the electronics box for v1.4 kits; we have left enough room to the right of the Pi for you to insert the card."
%}



![Screen Shot 2018-10-04 at 5.10.01 PM.png](_images/Screen_Shot_2018-10-04_at_5.10.01_PM.png)

## Step 4. Turn on the Raspberry Pi
Plug in the power source to the Raspberry Pi. Depending on your setup, power will be coming from either a standard microUSB cable plugged into the Farmduino (or a standalone power supply), from a DC/DC buck converter coming from your RAMPS shield, or from a DC/DC buck converter coming straight from your FarmBot's power supply.

You should now see a solid red <span class="fa fa-circle" style="color: red;opacity: 1"></span> LED and a steadily flashing green <span class="fa fa-circle" style="color: green;opacity: 1"></span> LED on the Raspberry Pi, indicating that the Pi has adequate power and is busy booting up. Refer to the [status LEDs](farmbot-os/status-leds.md) page for more information, especially if your LEDs are not lit up as described above.

# What's next?

 * [Configurator](farmbot-os/configurator.md)
 * [Status LEDs](farmbot-os/status-leds.md)
 * [Data Usage](farmbot-os/data-usage.md)
 * [OTA Updates](farmbot-os/ota-updates.md)
