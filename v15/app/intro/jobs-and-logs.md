---
title: "Jobs and Logs"
slug: "jobs-and-logs"
description: "Keep track of what FarmBot is doing :clipboard: :construction_worker:\n[Open this popup in the app](https://my.farm.bot/app/logs)"
---

The **jobs and logs popup** in the main nav bar of the app features two tabs allowing you to keep track of FarmBot's progress while it is performing long-running jobs as well as audit the detailed logs of each individual operation.

![jobs and logs popup](_images/jobs_and_logs_popup.png)

# Jobs tab

When FarmBot is executing long-running sequences or tasks such as watering the whole garden or taking photos, you can keep track of the high-level progress from the **jobs tab** of the popup.

The jobs table shows the **JOB** name, **%** completion, current **STATUS**, and the **DURATION** of time <i class='fa fa-clock-o'></i> that the job has been executing for. Completed jobs are shown at the bottom of the table and may be cleared after 5 minutes upon refreshing the browser tab.

![jobs tab](_images/jobs_tab.gif)

{%
include callout.html
type="info"
title="Use job progress tracking"
content="To implement job progress tracking in your own sequences, see the [Lua developer documentation](http://lua.farm.bot) for `set_job()` and `get_job()`."
%}

# Logs tab

The **logs tab** shows a low-level view of each individual operation that FarmBot has performed. Logs can be useful for debugging sequences and diagnosing issues with FarmBot, but are generally not needed during normal operation.

![logs tab](_images/logs_tab.png)

## Log types

There are several **log types**, each with their own color, that indicate the type of message being sent.

|<span class="gray fa fa-circle suacer"></span>|Type|Meaning|
|:--------------------------------------------:|----|-------|
|<span class="green fa fa-circle suacer"></span>|**SUCCESS**|FarmBot has successfully completed a task.<br>**Example:** *Synced*
|<span class="yellow fa fa-circle suacer"></span>|**BUSY**|FarmBot is busy working on a task.<br>**Example:** *Syncing*
|<span class="orange fa fa-circle suacer"></span>|**WARN**|A situation may require your attention or make FarmBot unresponsive.<br>**Example:** *Emergency locking and powering down*
|<span class="red fa fa-circle suacer"></span>|**ERROR**|An error or emergency stop has occurred.<br>**Example:** *Movement failed*
|<span class="light-blue fa fa-circle suacer"></span>|**INFO**|General information about what FarmBot is doing.<br>**Example:** *Starting Water All Plants Sequence*
|<span class="blue fa fa-circle suacer"></span>|**FUN**|Logs that are just for fun :rabbit:
|<span class="gray fa fa-circle suacer"></span>|**DEBUG**|Verbose information relevant to software development and troubleshooting.<br>**Example:** *Network interface needs configuration: wlan0*
|<span class="gray fa fa-circle suacer"></span>|**ASSERTION**|Results of <span class="fb-step fb-assertion">ASSERTION</span> commands. (advanced)

## Verbosity and filtering

FarmBot sends logs for nearly every action it takes. Sometimes seeing all of the logs can be helpful, for example when trying out new features or when debugging your system. Other times seeing only logs of a certain type or detail level is desirable, such as when you leave your FarmBot to work for a few weeks and you just periodically check in.

Every log that FarmBot sends has a **verbosity** of `1`, `2`, or `3`, which can be loosely associated with how important the log is and the level of detail that it reveals about how your FarmBot is operating. A more verbose log (verbosity `3`) is usually "lower level" and less important. A less verbose log (verbosity `1`) is usually "higher level" and more important.

You can filter logs by using the search bar or by clicking the filter <i class='fa fa-filter'></i> icon. The verbosity sliders allow you to choose to see more verbose or less verbose logs of each type, or turn them off completely.

![log filters](_images/log_filters.png)

## Logs settings menu

You can customize whether or not FarmBot sends some types of logs or not by using the options in the (cog) menu. Each option is described in the tooltip shown when the (?) icon is clicked.

![log settings menu](_images/log_settings_menu.png)

## Log limits

In order to provide the best possible web application experience to all users, we have implemented the following limitations to the number of logs a FarmBot can store to the web app within a given time period.

Time Period | Max Number of Logs
--- | ---
1 minute | 250
1 hour | 5,000
1 day | 25,000

If a log limit is reached, a **cooldown period** will begin where log storage and display is suspended until the next time period. For example, if the 1 minute limit is reached, logs will be suspended until the next minute. A warning log and toast notification will be displayed, indicating the suspension:

![device sending too many logs warning log message](_images/device_sending_too_many_logs_warning_log_message.png)

{%
include callout.html
type="success"
title="You still have control"
content="Even when log storage and display is suspended, you can still control the FarmBot from the web application (manual movements, <span class=\"fb-button fb-red\">E-STOP</span>, etc). FarmBot will also continue to execute scheduled events, take photos, etc while logs are suspended."
%}

Once the cooldown period has ended, logs will resume being stored and displayed in the web application. An informational log and toast notification will indicate this:

![cooldown period ended log message](_images/cooldown_period_ended_log_message.png)

{%
include callout.html
type="info"
title="Don't fret"
content="We do not expect average users to ever experience these limits. Instead, they are designed to minimize the disruption that an incorrectly configured FarmBot or a malicious attacker can have on our systems."
%}

# What's next?

 * [Message Center](message-center.md)