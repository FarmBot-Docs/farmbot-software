---
title: "Device"
slug: "device"
description: "Manage your FarmBot's settings: [my.farmbot.io/app/device](http://my.farmbot.io/app/device)"
---

* toc
{:toc}

Widgets on this page:
 * [Device](#device)
 * [Hardware](#hardware)
 * [Farmware](#farmware)
 * [Weed Detector](#weed-detector)

<style>
.nav-image{
  position: relative;
  max-width: 100%;
}
.nav-image a{
  display: block;      
  position: absolute;
}
.nav-image a:hover{
  background-color: black;
  opacity: 0.5;
}
.caption{
  font-style: italic;
  text-align: center;
}
</style>

<div class="nav-image">
  <img class="nav-image" src="_images/device_2.png" alt="Device" />
  <a href="https://software.farmbot.io/docs/device#device" style="top: 28.50%; left: 1.9%; width: 47.03%; height: 52.82%;"></a>
  <a href="https://software.farmbot.io/docs/device#hardware" style="top: 49.77%; left: 50.97%; width: 47.27%; height: 48.04%;"></a>
  <a href="https://software.farmbot.io/docs/device#farmware" style="top: 8.24%; left: 1.81%; width: 47.17%; height: 17.48%;"></a>
  <a href="https://software.farmbot.io/docs/device#weed-detector" style="top: 8.24%; left: 50.97%; width: 47.08%; height: 39.93%;"></a>
</div>
<figcaption class="caption">Click a widget in the image to learn more!</figcaption>

# Device

![device_widget.png](_images/device_widget.png)

 * Give your device a name
 * View the controller version and update it
 * View the firmware version and update it
 * Restart the controller
 * Factory reset FarmBot OS


# Hardware

![hardware.png](_images/hardware.png)

 * Steps per mm
 * Max speed
 * Acceleration period
 * Timeout
 * Length
 * Calibration
 * Invert endpoints
 * Invert motors
 * Allow negatives
 * Enable encoders

# Farmware

![farmware.png](_images/farmware.png)

Run a Farmware by selecting it from the list and pressing `RUN`. For more information, see [Farmware](../Additional-Information/farmware-dev.md).

# Weed Detector

![weed_detection.png](_images/weed_detection.png)

Select hue, saturation, and value ranges to cover the colors you want to detect using the sliders. The color boxes will give an indication of the range selected.

Change the blur, morph and iteration processing parameters if desired.

Press `TEST` to detect weeds in FarmBot camera's current view. The weeds will appear in the [Farm Designer](farm-designer.md). Press `CLEAR WEEDS` to delete them from the map.

Weed removal is performed by creating a weed removal sequence using the weeding tool and applying it to the weeds in the Farm Designer.
