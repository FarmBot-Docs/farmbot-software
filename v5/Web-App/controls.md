---
title: "Controls"
slug: "controls"
description: "Manually control your FarmBot from anywhere! [my.farmbot.io/app/controls](http://my.farmbot.io/app/controls)"
---

* toc
{:toc}

You generally will not need to manually control FarmBot, since it acts automatically from instructions provided by Farm Events. But in case you want to show off to your friends, you can do that from this page!

## Widgets on this page:
 * [Move](#move)
 * [Peripherals](#peripherals)
 * [Webcam Feeds](#webcam-feeds)

<div class="nav-image">
  <img class="nav-image" src="_images/controls.png" alt="Controls" />
  <a href="https://software.farmbot.io/docs/controls#move" style="top: 14.1%; left: 10.2%; width: 30.51%; height: 47.6%;"></a>
  <a href="https://software.farmbot.io/docs/controls#peripherals" style="top: 66.5%; left: 10.2%; width: 30.56%; height: 19.5%;"></a>
  <a href="https://software.farmbot.io/docs/controls#webcam-feeds" style="top: 14%; left: 42.99%; width: 46.8%; height: 73%;"></a>
</div>
<figcaption class="caption">Click a widget in the image to learn more!</figcaption>



<iframe class="embedly-embed" src="//cdn.embedly.com/widgets/media.html?src=https%3A%2F%2Fwww.youtube.com%2Fembed%2Fvideoseries%3Flist%3DPLMhsMRlKjcNIYlDKDdKvPQuHqBjjS1ZGc&url=http%3A%2F%2Fwww.youtube.com%2Fwatch%3Fv%3D5spRMMoocDU&image=https%3A%2F%2Fi.ytimg.com%2Fvi%2F5spRMMoocDU%2Fhqdefault.jpg&key=f2aa6fc3595946d0afc3d76cbbd25dc3&type=text%2Fhtml&schema=youtube" width="854" height="480" scrolling="no" frameborder="0" allowfullscreen></iframe>

# Move

![move.png](_images/move.png)

  * The current position of your FarmBot (Motor Coordinates (mm)) is shown in the grey fields directly below the X-AXIS, Y-AXIS, and Z-AXIS labels. This information is updated in real-time.
  * You can move the device a *relative distance* in any direction by using the arrow buttons. The default move amount is 100mm, though you can also select 1, 10, and 1000mm amounts. Depending on your settings in the **Hardware** configuration widget on the [Device](device.md)  page, you may not be able to move to negative coordinates or past the specified axis maximums.
  * The home button will move FarmBot to zero for all axes by first moving the Z axis to zero, then the other axes to zero.
  * You can move the device to an *absolute position* by typing in new coordinates to the input fields labeled X-AXIS, Y-AXIS, and Z-AXIS and pressing <span class="fb-button fb-green">GO</span>.
  * If you ever need to immediately halt your FarmBot, press the <span class="fb-button fb-red">E-STOP</span> button.
  * You can switch the directions that the jog buttons move by toggling the axis inversion in the settings menu (gear icon next to the e-stop button). Encoder data can be displayed in the settings menu as well.

# Peripherals
You can manually operate FarmBot's peripherals using the toggle switches in the **Peripherals** widget.

The pins can be changed to the pins used when plugging in the peripherals in [this step](https://genesis.farmbot.io/docs/plug-everything-in#step-3-connect-the-peripherals) of the hardware documentation.

![peripherals_unknown.png](_images/peripherals_unknown.png)

Press the toggle switch to turn a peripheral ON or OFF.

## Edit
To change the peripherals, press <span class="fb-button fb-gray">EDIT</span>.

![Peripherals Edit.JPG](_images/Peripherals_Edit.JPG)

Add a new peripheral by pressing the <span class="fb-button fb-green">+</span> button and filling out <span class="fb-input">Label</span> and <span class="fb-input">Pin #</span>. To delete a peripheral, press it's <span class="fb-button fb-red">-</span> button. When finished editing, press <span class="fb-button fb-green">SAVE</span>.

{%
include callout.html
type="warning"
title=""
content="Note that pin numbers are required and must be unique."
%}

# Webcam Feeds

![webcam.png](_images/webcam.png)

The __Webcam Feeds__ widget can be used for a network stream setup using a webcam. You could use the video stream for a view of the entire bot to view movements while controlling it remotely, or you could set up a webcam at a different angle for viewing plants, etc..

You will need to set up a network webcam, and provide the network stream's IP address to the widget.

## Edit
To set the webcam URL, press <span class="fb-button fb-gray">EDIT</span>, enter a URL (with `http://`) and press <span class="fb-button fb-green">SAVE</span>.

![webcam_inputs.png](_images/webcam_inputs.png)

