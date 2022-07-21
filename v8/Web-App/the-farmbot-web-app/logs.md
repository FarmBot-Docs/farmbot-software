---
title: "Logs"
slug: "logs"
description: "View and filter FarmBot OS log messages [my.farm.bot/app/logs](https://my.farm.bot/app/logs)"
---


<iframe class="embedly-embed" src="//cdn.embedly.com/widgets/media.html?url=http%3A%2F%2Fwww.youtube.com%2Fwatch%3Fv%3D46VgOoTvx4o&src=http%3A%2F%2Fwww.youtube.com%2Fembed%2F46VgOoTvx4o&type=text%2Fhtml&key=f2aa6fc3595946d0afc3d76cbbd25dc3&schema=youtube" width="854" height="480" scrolling="no" frameborder="0" allow="autoplay; fullscreen" allowfullscreen="true"></iframe>



# Verbosity and filtering

FarmBot sends logs for nearly every action it takes. Sometimes seeing all of the logs can be helpful, for example when trying out new features or when debugging your system. Other times seeing only the most important "high level" logs is desirable, such as when you leave your FarmBot to work for a few weeks and you just periodically check in.

Every log that FarmBot sends has a *verbosity* of `1`, `2`, or `3`, which can be loosely associated with how important the log is and the level of detail that it reveals about how your FarmBot is operating. A more verbose log (verbosity `3`) is usually "lower level" and less important. A less verbose log (verbosity `1`) is usually "higher level" and more important.

You can filter logs by clicking <span class="fb-button fb-gray">FILTER</span> (or, when log filters are currently active, <span class="fb-button fb-green">FILTERS ACTIVE</span>). The verbosity sliders allow you to choose to see more verbose or less verbose logs.

Setting a verbosity slider to `0` means you will not see any logs of that type in the logs table or in the status ticker. Setting a slider to `1` means you will see only the most important "high level" logs of that type. `2` means you will see most logs of that type including the most important "high level" logs as well as semi-important "medium level" logs. A setting of `3` means you will see every log of that type, many of which may be unimportant during normal operation.

The <span class="fb-button fb-gray">NORMAL</span> preset sets all log types to verbosity level `1`, while the <span class="fb-button fb-gray">MAX</span> sets all log types to verbosity level `3`, removing all filters.

![Screen Shot 2019-07-10 at 4.06.29 PM.png](_images/Screen_Shot_2019-07-10_at_4.06.29_PM.png)



# Logs settings menu

You can customize whether or not FarmBot sends some types of logs or not by using the options in the (cog) menu. Each option is described in the tooltip shown when the (?) icon is clicked.

![Screen Shot 2019-07-10 at 4.05.39 PM.png](_images/Screen_Shot_2019-07-10_at_4.05.39_PM.png)



{%
include callout.html
type="warning"
title="Warning"
content="The firmware sends a high volume of messages during normal FarmBot OS communication. Logging these messages may slow down the web app considerably. It is recommended to use this toggle sparingly and disable `Received` logs when you are done."
%}



# Log limits

In order to provide the best possible web application experience to all users, we have implemented the following limitations to the number of logs a FarmBot can store to the web app within a given time period.

|Time Period                   |Max Number of Logs            |
|------------------------------|------------------------------|
|1 minute                      |250
|1 hour                        |5,000
|1 day                         |25,000

If a log limit is reached, a cooldown period will begin where log storage and display is suspended until the next time period. For example, if the 1 minute limit is reached, logs will be suspended until the next minute. A warning log and toast notification will be displayed, indicating the suspension:

![Screen Shot 2018-08-15 at 12.23.33 PM.png](_images/Screen_Shot_2018-08-15_at_12.23.33_PM.png)



{%
include callout.html
type="success"
title="You still have control"
content="Even when log storage and display is suspended, you can still control the FarmBot from the web application (manual movements, E-STOP, etc). FarmBot will also continue to execute scheduled events, take photos, etc while logs are suspended."
%}

Once the cooldown period has ended, logs will resume being stored and displayed in the web application. An informational log and toast notification will indicate this:

![Screen Shot 2018-08-15 at 12.23.42 PM.png](_images/Screen_Shot_2018-08-15_at_12.23.42_PM.png)



{%
include callout.html
type="info"
title="Don't fret"
content="We do not expect average users to ever experience these limits. Instead, they are designed to minimize the disruption that an incorrectly configured FarmBot or a malicious attacker can have on our systems."
%}

