---
title: "Farmware"
slug: "farmware"
excerpt: "Photos and Weed Detection [my.farmbot.io/app/farmware](http://my.farmbot.io/app/farmware)"
---

* toc
{:toc}

Widgets on this page:
 * [Farmware](#farmware)
 * [Take Photo](#take-photo)
 * [Weed Detector](#weed-detector)
 * [Camera Calibration](#camera-calibration)

<div class="nav-image">
  <img class="nav-image" src="farmware_page.png" alt="Device" />
  <a href="https://software.farmbot.io/docs/farmware#farmware" style="top: 5.11%; left: 63.43%; width: 34.63%; height: 11.12%;"></a>
  <a href="https://software.farmbot.io/docs/farmware#take-photo" style="top: 5.36%; left: 0.50%; width: 61.93%; height: 41.38%;"></a>
  <a href="https://software.farmbot.io/docs/farmware#weed-detector" style="top: 48.35%; left: 54.05%; width: 45.62%; height: 51.15%;"></a>
  <a href="https://software.farmbot.io/docs/farmware#camera-calibration" style="top: 48.35%; left: 0%; width: 44.84%; height: 51.10%;"></a>
</div>
<figcaption class="caption">Click a widget in the image to learn more!</figcaption>



# Farmware



![farmware.png](farmware.png)

Run a Farmware by selecting it from the list and pressing <span class="fb-button fb-green">run</span>. For more information, see [Farmware](../Additional-Information/farmware-dev.md).

# Take Photo



![photo_widget.png](photo_widget.png)

Take photos using FarmBot's camera and view them.

Press <span class="fb-button fb-gray">take photo</span> to take a photo.

Use the `PREV` and `NEXT` buttons to navigate through previously taken images.

{%
include callout.html
type="info"
title=""
content="The default camera is a USB camera. If you would like to use a Raspberry Pi camera, use the camera selection dropdown menu in the **Device** widget on the [Device](../Web-App/device.md#device-widget) page."
%}



# Camera Calibration



{%
include callout.html
type="warning"
title="Work in Progress"
content="Camera calibration functionality will be available in alpha soon."
%}

Calibrate your FarmBot's camera. See also: [Weed Detector](#weed-detector)

![camera_calibration.png](camera_calibration.png)

Camera calibration works by using the distance between and orientation of calibration objects placed in the garden bed. Calibration only needs to be performed once.

![config.png](config.png)

## Instructions:

Place two red objects ([these red markers](https://genesis.farmbot.io/docs/miscellaneous#red-markers) are included in kits) on the surface of the soil in your garden bed. The objects should be bright red, and preferably round.

They can be placed anywhere in the bed, but they need to be placed square with FarmBot's tracks and in a location where FarmBot's camera can be moved directly overhead.

Measure the distance from the center of one object to the center of the next. The objects can be separated as far apart as they can while still remaining within the field of view of the camera. 100-200mm is a good starting point. Input the value in millimeters into the `calibration object separation` input box in the **Camera Calibration** widget settings menu (opened by pressing the white gear icon next to <span class="fb-button fb-green">calibrate</span>).

Select the axis along which the calibration objects are placed. If you placed them in the direction of the tracks, select `X` in the `calibration object separation along axis` drop down menu. If you placed them in the direction of the gantry, select `Y`.

For the `origin location in image` setting, look at a photo you have taken with FarmBot's camera (take one using the [take photo](#take-photo) widget if you haven't already). Determine which direction home is in the image, and select the corner of the image that corresponds to that direction. It can help to view a photo taken when FarmBot was at home (0, 0, 0). If a corner of the image does not correspond to the origin, try rotating the camera until one does.

The **hue** color range slider should be set to approximately 20-160, with the `invert hue range selection` checkbox marked. This will select a hue range that includes various shades of red.

Move FarmBot directly over the calibration objects you have placed, and move the z-axis as high as it will go. Press the <span class="fb-button fb-green">calibrate</span> button. Once calibration is finished, press refresh to view the result image. `pixel coordinate scale` and `camera rotation` results will appear as well.

{%
include callout.html
type="info"
title="Note"
content="Once camera calibration is run, you must always detect weeds with the camera at that height (z-axis coordinate). Running calibration with the z-axis all the way up is recommended to maximize the camera's field of view."
%}



# Weed Detector



{%
include callout.html
type="warning"
title="Work in Progress"
content="Weed detection functionality will be available in alpha soon."
%}



{%
include callout.html
type="info"
title="Calibration Required"
content="To use the Weed Detector widget, you must first calibrate the camera using the [Camera Calibration](#camera-calibration) widget."
%}



![weed_detector.png](weed_detector.png)

Select hue, saturation, and value ranges to cover the colors you want to detect using the sliders. The color boxes will give an indication of the range selected. For the hue slider, a green color range is approximately 30-90.

*Blur, morph and iteration processing parameters*: It is recommended to use the defaults, run a test, and then experiment with the values to test the results.

Move the FarmBot over a section of soil. Press <span class="fb-button fb-yellow">test</span> to detect weeds in FarmBot camera's current view. The weeds will appear in the [Farm Designer](../Web-App/farm-designer.md). Press <span class="fb-button fb-red">clear weeds</span> to delete them from the map.

Detect weeds across FarmBot's entire bed by creating a sequence of movements in a grid pattern with a <span class="fb-step fb-take-photo">run farmware</span> step at each grid point.

Weed removal can be performed by creating a weed removal sequence that uses the weeding tool on weeds (points) in the Farm Designer. For more information on the weed detection process, see [Weed Detection](../Additional-Information/weed-detection.md). For more information on creating sequences, see [Sequences](../Web-App/sequences.md).

![both.png](both.png)

_Left: Camera Calibration widget, Right: Weed Detector widget_

