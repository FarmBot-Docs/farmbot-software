---
title: "FarmBot OS"
slug: "farmbot-os"
description: "Step-by-step instructions for installing FarmBot OS :movie_camera: [Video tutorial](https://youtu.be/AOsF17Yxoi4?t=9)\nDownload the latest FarmBot OS `.img` file at [os.farm.bot](http://os.farm.bot)."
---

The Raspberry Pi runs a custom operating system named **FarmBot OS**, allowing FarmBot to:

  * Communicate with the web application over WiFi or ethernet so that it can synchronize (download) sequences, regimens, farm designs, events, and more; upload logs and sensor data; and accept real-time commands.
  * Communicate with the Farmduino to send G and F commands and receive sensor and encoder data.
  * Take photos with a USB or Raspberry Pi camera, and upload the photos to the web application.
  * Get configured over WiFi, mitigating the need to plug in a mouse, keyboard, or screen.

# Installation

{%
include callout.html
type="info"
title=""
content="You will need another computer with a microSD card reader to install FarmBot OS."
%}

## Step 1: Download FarmBot OS
Go to [os.farm.bot](http://os.farm.bot) to download the latest FarmBot OS `.img` file according to your **FarmBot kit** and it's **internal computer**.

<!-- <iframe src="https://my.farm.bot/os" width="100%" height="500px" style="border: none; border-radius: 3px;"></iframe> -->

## Step 2. Write FarmBot OS onto the microSD card
You must use a **`.img` writing tool** to write **FarmBot OS** onto the **microSD card**. We recommend downloading and installing **[balenaEtcher](https://www.balena.io/etcher/)** for this purpose.

Once you have Etcher installed, connect the microSD card to your computer using a **card reader**. You may need to use the **microSD card to SD card adapter** included with your kit. Select the FarmBot OS `.img` file you downloaded in Step 1, the microSD card drive as the **target** (it should show up as a `7.9 GB partition`) and then press **Flash!**  to write the file to the card.

![Screen Shot 2020-01-30 at 1.55.04 PM.png](_images/Screen_Shot_2020-01-30_at_1.55.04_PM.png)



{%
include callout.html
type="danger"
title="Etcher (balenaEtcher) may have issues on MacOS devices."
content="Some users have experienced difficulty flashing SD cards on MacOS devices. A common error experienced is \"Attention: The writer process has ended unexpectedly.\"   Other users on MacOS computers report Etcher freeze ups and crashes during the SD card flashing process.

If you encounter this error, or other problems please re-flash your SD card using a PC or Linux computer."
%}



![Etcher_Error_MacOS.jpg](_images/Etcher_Error_MacOS.jpg)

_Etcher: Common MacOS Error_



{%
include callout.html
type="warning"
title="Drag and drop will not work"
content="Using your typical file browser (Finder on Mac or File Explorer on Windows) to drag and drop or copy and paste the FarmBot OS `.img` file onto the microSD card **will not work**. You *must* use a tool such as Etcher as described above."
%}

## Step 3. Insert the microSD card into the Raspberry Pi
Insert the **microSD card** into the **Raspberry Pi**. The card slot location will differ depending on the FarmBot kit you have.

### Genesis kits

For Genesis kits, the card slot is located on the back side of the Pi 3, on the right-hand edge. You do not need to remove the Raspberry Pi from the electronics box to insert the card; we have left enough access room.

![MicroSD card slot on the Raspberry Pi 3](_images/Screen_Shot_2018-10-04_at_5.10.01_PM.png)

### Express kits

For Express kits, the card slot is located on the front side of the Pi Zero, on the left-hand edge.

![MicroSD card slot on the Raspberry Pi Zero W](_images/Card.jpeg)

## Step 4. Plug in the power source
Plug your FarmBot's power supply into a wall outlet. You should now see a solid red <span class="fa fa-circle red"></span> LED and a steadily flashing green <span class="fa fa-circle led green"></span> LED on the Raspberry Pi, indicating that the Pi has adequate power and is busy booting up. Refer to the [status LEDs](farmbot-os/status-leds.md) page for more information, especially if your LEDs are not lit up as described above.

# What's next?

 * [Configurator](farmbot-os/configurator.md)
 * [Status LEDs](farmbot-os/status-leds.md)
 * [Data Usage](farmbot-os/data-usage.md)
 * [Auto Updates](farmbot-os/auto-updates.md)
