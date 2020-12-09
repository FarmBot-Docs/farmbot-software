---
title: "Measure soil height"
slug: "measure-soil-height"
description: "Map your garden's soil surface using FarmBot's camera."
---

* toc
{:toc}

FarmBot uses computer vision software to detect the average z-axis coordinate of the soil in an image.

{%
include callout.html
type="info"
content="While the **Measure Soil Height** feature provides an automated method for mapping the soil surface, you may also manually add soil surface points through the [Points panel](https://my.farm.bot/app/designer/points). It is recommended to add at least several points manually (even if using the automatic method) for comparison."
%}

# Install

{%
include callout.html
type="info"
title="Only required while in alpha"
content="Once the feature moves out of alpha, **Measure Soil Height** will be preinstalled."
%}

Navigate to the [Farmware panel](https://my.farm.bot/app/designer/farmware) and press the <span class="fb-button fb-gray"><i class='fa fa-plus'></i></span> button. Paste the following URL into the input box:

```
https://raw.githubusercontent.com/FarmBot-Labs/farmware_manifests/main/packages/measure-soil-height/manifest.json
```

and press <span class="fb-button fb-green">INSTALL</span>.

# Calibrate
1. Move FarmBot to a location where the camera has a clear view of a wide area of soil.
Ensure the Y and Z axes have room to move away from home/zero.
3. Measure the distance from the camera lens to the soil with a tape measure.
4. Open the **Measure Soil Height** section of the [Photos panel](https://my.farm.bot/app/designer/photos).
5. Enter the measured distance in millimeters in the _Measured distance from camera to soil_ input.
6. Press **CALIBRATE**. FarmBot will:
    * take a photo
    * move the y-axis a small amount
    * take another photo
    * move the z-axis
    * take another photo
    * move the y-axis back
    * take another photo
    * move the z-axis back

# Measure
Once calibration is complete, soil height can be measured and recorded by pressing **MEASURE** in the **Measure Soil Height** section of the [Photos panel](https://my.farm.bot/app/designer/photos) or by using a **Measure Soil Height** sequence command and running the sequence.

For full garden soil mapping, follow [Scan the Garden for Weeds](../../FarmBot-Software/how-to-guides/scan-the-garden-for-weeds.md) and use the **Measure Soil Height** sequence command.

# Check results
The measured soil z coordinate will be shown in a toast message and saved to a soil height point in the [Points panel](https://my.farm.bot/app/designer/points). An image will be saved to the [Photos panel](https://my.farm.bot/app/designer/photos) which will also be shown in the map if the [camera has been calibrated](camera-calibration.md).

Before using the detected soil height values, compare the results to your garden bed:
 * Spot check individual values by moving FarmBot above the soil height point and measuring the distance to the soil with a tape measure or slowly moving FarmBot down to the detected soil height.
 * Remove or adjust outliers at the top and bottom of the [soil height points list](../points.md#soil-height-points).
 * Open the [profile viewer](../farm-designer.md#profile-viewer) and check the detected soil cross-section.

If the detected values are consistently offset from the actual soil surface, try adjusting the _Measured distance from camera to soil_ input in the **Measure Soil Height** section of the [Photos panel](https://my.farm.bot/app/designer/photos) or re-calibrate by pressing the <span class="fb-button fb-red">RESET CALIBRATION VALUES</span> button and following the [calibration steps](#calibrate).

# Use soil height

After checking the detected soil points and removing or adjusting any outliers, open the [soil height points list](../points.md#soil-height-points) and press the <span class="fb-button fb-blue">USE AVERAGE Z</span> button to apply the average detected soil height to the [soil height](../settings/axes.md#soil-height) value used by <span class="fb-step fb-move">Move</span> sequence commands.

# Troubleshooting

## Capture
_Error message:_ `Problem getting image`:
_Troubleshooting steps:_ Verify camera is working by taking a photo.

## Calibration
_Error message:_ `Calibration measured distance input required`:
_Solution:_ Provide a distance measurement (see the [calibration steps](#calibrate)).

_Error message:_ `Image size must match calibration`:
_Solution:_ Recalibrate or revert change to image capture size or rotation.

## Detection
All other error messages:
_Troubleshooting steps:_ Verify the soil is clearly visible in photos or try recalibrating at a different location..
