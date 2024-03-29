---
title: "Error Handling"
slug: "error-handling"
description: "Let FarmBot know what to do when something goes wrong\n[Open these settings in the app](https://my.farm.bot/app/device?highlight=error_handling)"
---


![Screen Shot 2020-04-22 at 4.57.22 PM.png](_images/Screen_Shot_2020-04-22_at_4.57.22_PM.png)

# Timeout after
This is the amount of time in seconds that the firmware will wait until a movement command times out, or stops executing. The default value for each axis is 120 seconds.

{%
include callout.html
type="warning"
title="Use reasonable timeout values"
content="Do not set the timeout times to extremely high values (such as 20,000 seconds). Under certain circumstances, such as when endstops and encoders are disabled and you send an extremely long movement command, this could cause your FarmBot to stall at the end of an axis for a very long time, requiring an e-stop or system reboot."
%}

# Max retries
The number of times that FarmBot will try to move to a position before stopping and reporting that the movement has failed.

# E-stop on movement error
Emergency stop if movement is not complete after the maximum number of retries. If enabled and the retries are exhausted, you will need to unlock the device by pressing the <span class="fb-button fb-yellow">UNLOCK</span> button in the main navbar.
