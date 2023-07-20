---
title: "Account Settings"
slug: "account-settings"
description: ":computer: Manage your account and app settings.\n[Open these settings in the app](https://my.farm.bot/app/designer/settings?highlight=account)"
---

In this section you can change your name (displayed in the top right of the app), email (used for login, emailed log messages), and account password. There are also additional app settings, reset controls, and data export tools, as described below.

# Internationalize web app

Disable use of language files to translate web app text.

{%
include callout.html
type="info"
title="Translations may be incomplete"
content="Interested in helping out? See the [instructions for submitting corrections or new languages](https://github.com/FarmBot/Farmbot-Web-App#translating-the-web-app-into-your-language)."
%}

# Use 24-hour time format

Enabling this setting will display times using the 24-hour notation, i.e., `23:00` instead of `11:00pm`.

# Show seconds in time

Enabling this setting will display times with seconds, i.e., `6:22:58pm` instead of `6:22pm`.

# Hide sections

If you're not using an external webcam to monitor your FarmBot, you can remove the **webcams** section from the controls panel to save space. If your FarmBot does not have any sensors (such as FarmBot Express), you can hide the **sensors** panel as well.

# Read speak logs in browser

<span class="fb-step fb-send-message">SEND MESSAGE</span> commands can optionally speak the message aloud. The audio can be heard from the Raspberry Pi's 3.5mm audio jack, and using this setting, output using your computer speakers as well.

{%
include callout.html
type="info"
title=""
content="This feature may not be available in some web browsers. We're sorry for the inconvenience."
%}

# Discard unsaved changes

Enabling this setting will prevent a browser dialog from asking about unsaved work before closing the browser tab. Warning: may cause loss of data.

# Confirm emergency unlock

Enabling this setting will show a browser dialog asking for confirmation when using the <span class="fb-button fb-yellow">UNLOCK</span> button after an emergency stop.

# User interface read-only mode

Enabling this setting will prevent data changes to your account, such as modifying or deleting sequences or garden layouts. This setting does not prevent FarmBot OS from changing settings, or the manual control buttons from working.

This setting may be useful when setting up a demonstration computer for members of the public to control a FarmBot, or in a school setting where an instructor wishes to protect the account from accidental changes from students.

# Landing page

Choose the starting page/panel that loads after logging into the app.

# Language

Your preferred language. Used to write comments in AI generated Lua code.

# Reset your account

Resetting your account will permanently delete all of your sequences, regimens, events, tools, logs, and farm designer data. All app settings and device settings will be reset to default values. This is useful if you want to delete all data to start from scratch while avoiding having to fully delete your account, re-signup, and re-configure your FarmBot.

Note that when FarmBot syncs after resetting your account, your FarmBot will delete all of its stored Sequences, etc, because your account will no longer have any of these resources until you create new ones. Furthermore, upon reset any customized device settings will be immediately overwritten with the default values downloaded from the reset web app account.

{%
include callout.html
type="danger"
title=""
content="Resetting an account is irreversible."
%}

# Delete your account

Permanently delete your account and all of its data. If you have a FarmBot connected to this account, it should be soft reset before the account is deleted. Otherwise you may need to reflash the microSD card to reconnect it to a new account.

{%
include callout.html
type="danger"
title=""
content="Deleting an account is irreversible. If you have a FarmBot connected to this account, it should be soft reset before the account is deleted. Otherwise you may need to reflash the microSD card to reconnect it to a new account."
%}

# Exporting data

Download all of your web app account data. Exported data is delivered in JSON format to your email address as a file attachment.

# Account limitations

All accounts at my.farm.bot have the following limitations:

|Resource                      |Limit                         |Notes                         |
|------------------------------|------------------------------|------------------------------|
|Devices                       |1                             |While you technically *can* pair multiple devices to one account, we do not officially support this and it may result in unexpected behavior.
|Points (Plants, Weeds, Tool Slots)|1,000                         |We expect to offer increased limits with paid plans in the future.
|Logs (storage rate)           |See the [log rate limits section](../intro/jobs-and-logs.md#log-limits)|
|Logs (stored)                 |1,000                         |We expect to offer increased limits with paid plans in the future.
|Logs (viewable)               |250                           |
|Images (viewable)             |450                           |

# Automatic account deletion

As a matter of security, web app accounts that are not being used are subject to **automatic deletion** with the following process:

**1) Checking for eligibility**
* If the account has never had a FarmBot connected to it, the account becomes eligible to be deleted 3 months after the last login.
* If the account has had a FarmBot connected to it at least once, the account becomes eligible to be deleted 11 months after the last login.

**2) Grace period**
Once the account becomes eligible for deletion, an email will be sent with the subject `[ACTION REQUIRED] Your FarmBot account will be deleted due to inactivity unless you login`. To halt the automatic deletion process, the user must login.

**3) Deletion**
If the user does not login to their account within 14 days of the warning email, the account will be automatically deleted and cannot be recovered.

# What's next?

 * [Logs](../intro/jobs-and-logs.md)
