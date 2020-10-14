---
title: "Account"
slug: "account"
description: "Manage your account and app settings [my.farm.bot/app/account](https://my.farm.bot/app/account)"
---

* toc
{:toc}


<div class="nav-image">
  <img class="nav-image" src="_images/account.png" alt="Account" />
  <a href="#account-settings" style="top: 6.66%; left: 26.34%; width: 47.39%; height: 11.98%;"></a>
  <a href="#change-password" style="top: 21.76%; left: 26.27%; width: 47.32%; height: 15.71%;"></a>
  <a href="#app-settings" style="top: 40.56%; left: 26.34%; width: 47.46%; height: 31.23%;"></a>
  <a href="#delete-account" style="top: 74.94%; left: 26.27%; width: 47.53%; height: 24.33%;"></a>
</div>
<figcaption class="caption">Click a widget in the image to learn more!</figcaption>



# Account Settings

Change your name (displayed in the top right of the app) and email (used for login, emailed log messages).

# Change Password

Select a new password.

# App Settings

Customize your web app experience.

## Internationalize web app
Disable use of language files to translate web app text.

{%
include callout.html
type="info"
title="Web App translations may be incomplete"
content="Interested in helping out? See the [instructions for submitting corrections or new languages](https://github.com/FarmBot/Farmbot-Web-App#translating-the-web-app-into-your-language)."
%}

## Confirm sequence step deletion
Show a confirmation dialog when the sequence delete step icon is pressed.

## Hide webcam widget
If not using a webcam, use this setting to remove the widget from the Controls page.

## Dynamic map size
Change the [Farm Designer](farm-designer.md)  map size based on axis length. A value must be input in `AXIS LENGTH` and `STOP AT MAX` must be enabled in the [Hardware](device.md#hardware-widget) widget.

## Double default map dimensions
Double the default dimensions of the [Farm Designer](farm-designer.md) map for a map with four times the area. ([FarmBot Genesis XL](https://farm.bot/))

## Display plant animations
Enable plant animations in the [Farm Designer](farm-designer.md).

{%
include callout.html
type="warning"
title="Experiencing plant icon oddities?"
content="Use or upgrade to the latest Chrome browser, disable animations using this setting, or [submit a bug report](https://github.com/FarmBot/Farmbot-Web-App/issues/new)."
%}



# Delete Account

Permanently delete your account and all of its data.

# Export Data

Download all of your Web App account data. Exported data is delivered in JSON format to your email address as a file attachment.

# What's next?

 * [Logs](account/logs.md)
 * [Account Limitations](account/account-limitations.md)
