---
title: "Error Handling"
slug: "error-handling"
description: ":stop_sign: Let FarmBot know what to do when something goes wrong.\n[Open these settings in the app](https://my.farm.bot/app/designer/settings?highlight=error_handling)"
---

* toc
{:toc}


![error handling](_images/error_handling.png)

# Max retries

The number of times that FarmBot will try to move to a position before stopping and reporting that the movement has failed.

# Calibration retries

Number of times to retry calibration.

# E-stop on movement error

Emergency stop if movement is not complete after the maximum number of retries. If enabled and the retries are exhausted, you will need to unlock the device by pressing the <span class="fb-button fb-yellow">UNLOCK</span> button in the main navbar.

# Advanced settings

{%
include callout.html
type="info"
content="These [advanced settings](../settings/parameter-management.md#show-advanced-settings) are not shown by default."
%}

## Timeout after

This is the amount of time in seconds that the firmware will wait until a movement command times out, or stops executing. The default value for each axis is 120 seconds.

{%
include callout.html
type="warning"
title="Use reasonable timeout values"
content="Do not set the timeout times to extremely high values (such as 20,000 seconds). Under certain circumstances, such as when endstops and encoders are disabled and you send an extremely long movement command, this could cause your FarmBot to stall at the end of an axis for a very long time, requiring an e-stop or system reboot."
%}

## Calibration retry reset distance

Distance in millimeters to group calibration retries. If the distance travelled while detecting the axis end location exceeds this value, the calibration retry counter is reset.
