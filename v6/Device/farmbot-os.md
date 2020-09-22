---
title: "FarmBot OS"
slug: "farmbot-os"
excerpt: "Step-by-step instructions for installing FarmBot OS onto the Raspberry Pi.\nDownload the latest FarmBot OS `.img` file [here](http://os.farm.bot)."
---

* toc
{:toc}

The Raspberry Pi runs a custom operating system named **FarmBot OS**, allowing FarmBot to:

* Communicate with the web application over WiFi or ethernet in order to synchronize (download) sequences, regimens, farm designs, events, and more; upload logs and sensor data; and accept real-time commands.
* Communicate with the Arduino over USB to send G and F commands and receive sensor and encoder data.
* Take photos with a USB or Raspberry Pi camera, and send the photos back to the web application.
* Get configured over WiFi, mitigating the need to plug in a mouse, keyboard, or screen.

{%
include callout.html
type="success"
title="Help improve FarmBot OS"
content="Submit feature requests, bugs, and code on GitHub for [FarmBot OS](https://github.com/FarmBot/farmbot_os)."
%}



# Installing FarmBot OS



{%
include callout.html
type="info"
title="Another computer is required"
content="You will need another computer with a microSD card reader to install FarmBot OS."
%}

## Step 1: Download FarmBot OS
Download the latest FarmBot OS `.img` file [here](http://os.farm.bot).

## Step 2. Write FarmBot OS to the microSD card
You must use a `.img` tool to write FarmBot OS onto the microSD card. We recommend downloading and installing [Etcher](https://etcher.io/) for this purpose. Once you have Etcher installed, open it up and select the FarmBot OS `.img` file and write it to the microSD card.

{%
include callout.html
type="warning"
title="Drag and drop will not work"
content="Using your typical file browser (Finder on Mac or File Explorer on Windows) to drag and drop or copy and paste the FarmBot OS `.img` file onto the microSD card **will not work**. You *must* use a tool such as Etcher as described above."
%}

# Step 3. Insert the microSD card into the Raspberry Pi
Insert the microSD card into the back side of the Raspberry Pi. *Note: you do not need to remove the Raspberry Pi from the electronics box for v1.4 kits - we have left enough room to the right of the Pi for you to insert the card.*

![Screen Shot 2018-10-04 at 5.10.01 PM.png](Screen_Shot_2018-10-04_at_5.10.01_PM.png)

## Step 4. Turn on the Raspberry Pi
Plug in the power source to the Raspberry Pi. Depending on your setup, power will be coming from either a standard microUSB cable plugged into a standalone power supply (or the Farmduino), from a DC/DC buck converter coming from your RAMPS shield, or from a DC/DC buck converter coming straight from your FarmBot's power supply.

# Raspberry Pi Status LEDs



{%
include callout.html
type="success"
title="Raspberry Pi LED status"
content="At this point you should see a solid red <span class=\"fa fa-circle\" style=\"color: red;opacity: 1\"></span>LED and a steadily flashing green <span class=\"fa fa-circle\" style=\"color: green;opacity: 1\"></span>LED on the Raspberry Pi."
%}



{%
include callout.html
type="danger"
title="Low power"
content="If the red <span class=\"fa fa-circle\" style=\"color: red;opacity: 1\"></span>LED on the Raspberry Pi does not light up or blinks, the power supply may not be adequate. **The power supplied must be rated to 5V and at least 2A, though 3A is recommended.**"
%}



|RED (power)                   |STATUS                        |TIPS                          |
|------------------------------|------------------------------|------------------------------|
|<span class="fa fa-circle" style="color: red;opacity: 1"></span> (solid red)|OK                            |Good to go!
|<span class="fa fa-sun-o" style="color: red;opacity: 1"></span> (blinking red)|Low power                     |Try a more powerful power supply or a different cable.
|<span class="fa fa-circle-thin" style="color: red;opacity: 1"></span>  (off)|No power / low power          |Plug in to a 3A power supply.



|GREEN (activity)              |STATUS                        |TIPS                          |
|------------------------------|------------------------------|------------------------------|
|<span class="fa fa-circle" style="color: green;opacity: 1"></span> (solid green)|Busy                          |Working/booting
|<span class="fa fa-sun-o" style="color: green;opacity: 1"></span> (blinking randomly)|Busy                          |Working/booting
|<span class="fa fa-sun-o" style="color: green;opacity: 1"></span> (blinking consistently)|Network disconnected or emergency stopped|[Configure FarmBot](../FarmBot OS/farmbot-os/configurator.md), press <span class="fb-button fb-yellow">UNLOCK</span> in the Web App, or check that the network FarmBot is connected to is online.
|<span class="fa fa-circle-thin" style="color: green;opacity: 1"></span> (off)|Ready                         |Waiting for the next task



# Electronics Box Status LEDs



{%
include callout.html
type="info"
title="FarmBot OS v6.4.4 or greater required"
content=""
%}

The following LEDs are mounted on top of the FarmBot Genesis v1.4 kit electronics box. Alternatively, you can connect an LED to the Raspberry Pi GPIO BCM pin number provided.
See [pinout.xyz](https://pinout.xyz/) for a Raspberry Pi GPIO reference diagram.

## Button 1 LED: E-STOP [red] (Raspberry Pi GPIO BCM pin 17)

|RED (E-STOP)                  |STATUS                        |TIPS                          |
|------------------------------|------------------------------|------------------------------|
|<span class="fa fa-circle" style="color: red;opacity: 1"></span> (solid red)|unlocked                      |Ready
|<span class="fa fa-circle-thin" style="color: red;opacity: 1"></span> (off)|locked                        |check the button 2 LED status

## Button 2 LED: UNLOCK [yellow] (Raspberry Pi GPIO BCM pin 23)


|YELLOW (UNLOCK)               |STATUS                        |TIPS                          |
|------------------------------|------------------------------|------------------------------|
|<span class="fa fa-sun-o" style="color: orange;opacity: 1"></span> (blinking)|locked                        |When safe to do so, press this button to unlock FarmBot.
|<span class="fa fa-circle-thin" style="color: orange;opacity: 1"></span> (off)|unlocked                      |Ready

## LED 1: Sync status [Green] (Raspberry Pi GPIO BCM pin 24)

|GREEN (sync)                  |STATUS                        |TIPS                          |
|------------------------------|------------------------------|------------------------------|
|<span class="fa fa-circle" style="color: green;opacity: 1"></span> (solid green)|Synced                        |Ready
|<span class="fa fa-sun-o" style="color: green;opacity: 1"></span> (blinking slowly)|Needs sync                    |Will not execute any unsynced events or sequences
|<span class="fa fa-sun-o" style="color: green;opacity: 1"></span> (blinking quickly)|Syncing                       |
|<span class="fa fa-circle-thin" style="color: green;opacity: 1"></span> (off)|Offline                       |Check the connection status LED

## LED 2: Connection status [Blue] (Raspberry Pi GPIO BCM pin 25)

|BLUE (connection)             |STATUS                        |TIPS                          |
|------------------------------|------------------------------|------------------------------|
|<span class="fa fa-circle" style="color: blue;opacity: 1"></span> (solid blue)|Connected                     |Working
|<span class="fa fa-sun-o" style="color: blue;opacity: 1"></span> (blinking slowly)|Needs configuration           |[Configure FarmBot](../FarmBot OS/farmbot-os/configurator.md), press <span class="fb-button fb-yellow">UNLOCK</span> in the Web App, or check that the network FarmBot is connected to is online.
|<span class="fa fa-circle-thin" style="color: blue;opacity: 1"></span> (off)|Offline                       |Check your internet connection.

## LED 3: Controllable [white] (Raspberry Pi GPIO BCM pin 12)
Control this LED via the <span class="fb-step fb-write-pin">Write Pin</span> Sequence step command.

## LED 4: Controllable [white] (Raspberry Pi GPIO BCM pin 13)
Control this LED via the <span class="fb-step fb-write-pin">Write Pin</span> Sequence step command.
