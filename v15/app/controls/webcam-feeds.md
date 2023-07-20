---
title: "Webcam Feeds"
slug: "webcam-feeds"
description: "Monitor your FarmBot from a distance <i class='fa fa-video-camera'></i>\n[Open this popup in the app](https://my.farm.bot/app/designer/controls)"
---

The **WEBCAM FEEDS** tab of the controls popup allows you to monitor your FarmBot from a distance with the use of an external camera system such as a Nest brand home security camera. Using a single camera, you could monitor the entire FarmBot bed while controlling it remotely, or, you could set up multiple webcams at different angles for viewing plants, etc.

![webcam feeds](_images/webcam_feeds.png)

# Adding a webcam feed
To add a webcam feed, press <span class="fb-button fb-gray">EDIT</span>, and then the <span class="fb-button fb-green"><i class='fa fa-plus'></i></span> button. Provide a <span class="fb-input">Name</span> and a publicly accessible <span class="fb-input">URL</span> (with `http://`) or IP address for your webcam stream. Multiple webcam feeds can be added by pressing <span class="fb-button fb-green"><i class='fa fa-plus'></i></span> for each camera. When finished editing, press <span class="fb-button fb-green">SAVE</span>.

![edit webcam feeds](_images/edit_webcam_feeds.png)

{%
include callout.html
type="warning"
title="Not all webcam feeds will work"
content="Some webcam services do not allow webcam feeds to be embedded in other websites or apps. If you see a web browser error after adding a webcam feed, there is unfortunately nothing FarmBot can do to fix the problem. Please contact your webcam's customer support to see if the security policy for embedding feeds into other sites can be changed."
%}

# Viewing webcam feeds
The webcam feed area will display one webcam feed at a time. If you have added multiple webcam feeds, you can cycle through them using the `PREV` and `NEXT` buttons on the left and right sides of the viewer.

![view multiple webcam feeds](_images/view_multiple_webcam_feeds.png)

# Deleting webcam feeds
To delete a webcam feed, press <span class="fb-button fb-gray">edit</span> and then the feed's <span class="fb-button fb-red"><i class='fa fa-times'></i></span> button. Finish editing by pressing <span class="fb-button fb-gray">back</span>.

# What's next?

 * [Sensors](../sensors.md)
