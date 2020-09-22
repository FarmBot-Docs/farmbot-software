---
title: "Farmware"
slug: "farmware"
excerpt: "Photos and Weed Detection [my.farmbot.io/app/farmware](http://my.farmbot.io/app/farmware)"
---

* toc
{:toc}

Widgets on this page:
 * [Farmware](#section-farmware)
 * [Take Photo](#section-take-photo)
 * [Weed Detector](#section-weed-detector)
 * [Camera Calibration](#section-camera-calibration)

<div class="nav-image">
  <img class="nav-image" src="farmware_page.png" alt="Device" />
  <a href="https://software.farmbot.io/docs/farmware#section-farmware" style="top: 80.07%; left: 1.84%; width: 22.73%; height: 17.63%;"></a>
  <a href="https://software.farmbot.io/docs/farmware#section-take-photo" style="top: 7.38%; left: 34.59%; width: 30.97%; height: 36.63%;"></a>
  <a href="https://software.farmbot.io/docs/farmware#section-weed-detector" style="top: 7.31%; left: 0.94%; width: 32.81%; height: 68.39%;"></a>
  <a href="https://software.farmbot.io/docs/farmware#section-camera-calibration" style="top: 7.31%; left: 66.35%; width: 32.97%; height: 68.39%;"></a>
</div>
<figcaption class="caption">Click a widget in the image to learn more!</figcaption>


# Farmware

![farmware.png](farmware.png)

Run a Farmware by selecting it from the list and pressing <span class="fb-button fb-green">run</span>. For more information, see [Farmware](../Extras/farmware-dev.md).

# Take Photo

![photo_widget.png](photo_widget.png)

Take photos using FarmBot's camera and view them.

Press <span class="fb-button fb-gray">take photo</span> to take a photo.

Use the `PREV` and `NEXT` buttons to navigate through previously taken images.

{%
include callout.html
type="info"
title=""
content="The default camera is a USB camera. If you would like to use a Raspberry Pi camera, use the camera selection dropdown menu in the **Device** widget on the [Device](doc:device#section-device) page."
%}

# Weed Detector

{%
include callout.html
type="warning"
title="Work in Progress"
content="Weed detection functionality will be available in alpha soon."
%}



![weed_detection.png](weed_detection.png)

Select hue, saturation, and value ranges to cover the colors you want to detect using the sliders. The color boxes will give an indication of the range selected.

Change the blur, morph and iteration processing parameters if desired.

Press <span class="fb-button fb-yellow">test</span> to detect weeds in FarmBot camera's current view. The weeds will appear in the [Farm Designer](../The FarmBot Web App/farm-designer.md). Press <span class="fb-button fb-red">clear weeds</span> to delete them from the map.

Weed removal is performed by creating a weed removal sequence using the weeding tool and applying it to the weeds in the Farm Designer. For more information on the weed detection process, see [Weed Detection](../The FarmBot Web App/farmware/weed-detection.md).

# Camera Calibration

Coming soon.
