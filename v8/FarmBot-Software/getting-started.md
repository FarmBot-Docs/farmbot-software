---
title: "Getting Started"
slug: "getting-started"
excerpt: "Suggested steps for getting started with FarmBot"
---

* toc
{:toc}

If you just finished your FarmBot hardware assembly, you should be ready to set up FarmBot's software. We suggest proceeding in the following order:

# Step 1: Create a web app account
1. Follow our instructions to [create a web app account](../Web-App/the-farmbot-web-app/creating-an-account.md) at [my.farm.bot](https://my.farm.bot). Make sure you verify your account by clicking the verification link emailed to you upon sign up.
2. Once logged in, read the cards in the [message center](../Web-App/the-farmbot-web-app/message-center.md) to become acquainted with the app.
3. Finish setting up your account by [choosing your FarmBot](../Web-App/the-farmbot-web-app/creating-an-account.md#choose-your-farmbot). This will add a set of starter resources (sequences, tools, etc) and apply settings appropriate to your FarmBot model.

# Step 2: Connect your FarmBot
1. [Install FarmBot OS](../Device/farmbot-os.md#installing-farmbot-os) onto the microSD card and power on the device.

{%
include callout.html
type="success"
title=""
content="Genesis v1.5+ and Express v1.0+ kits come with FarmBot OS pre-installed, so you can skip this step."
%}

2. [Configure FarmBot](../Device/farmbot-os/configurator.md) to connect to your home WiFi network and your web app account.
3. Log in to the web app and verify that FarmBot has connected.

# Step 3: Match the virtual FarmBot to real-life
1. Using the [manual controls](../Web-App/controls.md), try moving FarmBot along each axis in both directions. If needed, use the **INVERT JOG BUTTONS** and **SWAP JOG BUTTONS** settings (in the move widget's <i class="fa fa-cog"></i> menu) so that the <span class="fb-button fb-gray"><i class="fa fa-arrow-left"></i></span> <span class="fb-button fb-gray"><i class="fa fa-arrow-right"></i></span> <span class="fb-button fb-gray"><i class="fa fa-arrow-up"></i></span> <span class="fb-button fb-gray"><i class="fa fa-arrow-down"></i></span> buttons send FarmBot moving in the direction that the arrow indicates, according to your real-life perspective.
2. If needed, use the **MAP ORIGIN** and **ROTATE MAP** settings so that the farm designer matches your real-life perspective.

# Step 4: Calibrate FarmBot
1. Send FarmBot to all corners of your raised bed to ensure it can successfully move throughout the entire working area. Make adjustments to belt tension, eccentric spacers, and track alignment as needed, as well as [hardware settings](../Web-App/device/hardware-settings.md) such as **MAX SPEED**.
2. Once you're sure everything operates as expected, [calibrate](../FarmBot-Software/how-do-i/calibrate-and-home-farmbot.md) the device. This will automatically set the exact **AXIS LENGTHS** of your FarmBot.

# Step 5: Add tools, seed containers, slots, peripherals, and sensors

{%
include callout.html
type="info"
title=""
content="If you chose your FarmBot model in the message center, then all of these resources will have already been added for you. However, you will still want to test the peripherals and sensors."
%}

1. Add [tools and seed containers](../Web-App/tools.md) and then load them into [slots](../Web-App/tools/tool-slots.md) so that FarmBot knows where everything is located in the garden bed. Remember: the virtual configuration must always match the real-life configuration.
2. Add [peripherals](../Web-App/controls/peripherals.md) and [sensors](../Web-App/controls/sensors.md), and then use the manual controls to test them.

# Step 6: Design your garden
[Add plants](../Web-App/farm-designer/plants.md) to the [farm designer](../Web-App/farm-designer.md). Remember to choose crops that will grow well in your area at this time of year, and that will be [compatible with FarmBot](http://seeds.farm.bot). Large, indeterminate crops such as Squash or Runner Beans should be placed at the front and back edges of the bed and trained outward so they do not interfere with FarmBot's movements along the x-axis.

{%
include callout.html
type="info"
title=""
content="If you chose your FarmBot model in the message center, then there will be some starter plants already in your garden. You'll likely just want to delete these once you're ready to plan your own layout."
%}

# Step 7: Build and test sequences
Create [sequences](../Web-App/sequences.md) and try them out with the <span class="fb-button fb-orange">TEST</span> button. Start with short, simple sequences and combine them later with the <span class="fb-step fb-execute">EXECUTE SEQUENCE</span> command to do longer, more complex routines. You might first try mounting or dismounting a tool, picking up seeds, or watering. This is where things get really fun!

{%
include callout.html
type="success"
title=""
content="If you chose your FarmBot model in the message center, then there will be some starter sequences already available for you to try. Feel free to use them as-is, copy them, or modify them."
%}

# Step 8: Create regimens
Create [regimens](../Web-App/regimens.md) to take care of your plants throughout their entire life. This will make it easy to re-plant the same crops season after season.

# Step 9: Schedule events
Use [events](../Web-App/farm-designer/events.md) to schedule your sequences and regimens run automatically. Your garden is now on auto-pilot :100:

# Step 10: Monitor your garden
Add a [webcam feed](../Web-App/controls/webcam-feeds.md) to monitor your garden remotely.
