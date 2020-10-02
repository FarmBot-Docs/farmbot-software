---
title: "The FarmBot Web App"
slug: "the-farmbot-web-app"
excerpt: "Step-by-step instructions for setting up and using the FarmBot web app"
---

* toc
{:toc}

The Farmbot Web App is a cloud based web service that performs the following functions:
 * [Farm Designer](../Web-App/farm-designer.md) - Drag and drop interface for farm/garden design
 * [Events](../Web-App/events.md) - Scheduling sequences and regimens
 * [Controls](../Web-App/controls.md) - Real time manual control of a FarmBot from a web browser
 * [Device](../Web-App/device.md)  - Storage of device info and calibration settings
 * [Sequences](../Web-App/sequences.md) - Creation of sequences of commands
 * [Regimens](../Web-App/regimens.md) - Creation of regimens (plant-age-based scheduling of sequences)
 * [Tools](../Web-App/tools.md) - Management of FarmBot's Tools and Tool Slots
 * [Farmware](../Web-App/farmware.md) - Photos and Weed Detection
 * [Logs](../Web-App/account/logs.md) - View and filter FarmBot OS log messages
 * Coming soon: crop and sensor data storage and management

<iframe class="embedly-embed" src="//cdn.embedly.com/widgets/media.html?src=https%3A%2F%2Fwww.youtube.com%2Fembed%2Fvideoseries%3Flist%3DPLMhsMRlKjcNIYlDKDdKvPQuHqBjjS1ZGc&url=http%3A%2F%2Fwww.youtube.com%2Fwatch%3Fv%3DUFjDyfRool8&image=https%3A%2F%2Fi.ytimg.com%2Fvi%2FUFjDyfRool8%2Fhqdefault.jpg&key=f2aa6fc3595946d0afc3d76cbbd25dc3&type=text%2Fhtml&schema=youtube" width="854" height="480" scrolling="no" frameborder="0" allowfullscreen></iframe>



# Creating an account

1. Go to [my.farm.bot](https://my.farm.bot)
2. Enter an <span class="fb-input">Email</span>, <span class="fb-input">Name</span>, and <span class="fb-input">Password</span> in the **CREATE AN ACCOUNT** widget
3. Agree to our [privacy policy](http://privacy.farm.bot) and [terms of use](http://tos.farm.bot) and click <span class="fb-button fb-green">Create account</span>
4. Check your email and follow the link to confirm your account

# Connect FarmBot to your account

1. Follow the [FarmBot OS installation instructions](../Device/farmbot-os.md).
2. Follow the [Configurator instructions](../Device/farmbot-os/configurator.md).
3. Go to [my.farm.bot](https://my.farm.bot) and log in.


{%
include callout.html
type="success"
title="Can you hear me now?"
content="The web application should now be in communication with your FarmBot. You should see some bootup logs streaming into the status ticker, and FarmBot should respond to any commands you send it. If there are any problems, see the [Configurator Troubleshooting Tips](../Device/farmbot-os/configurator.md#troubleshooting)."
%}



# Web app workflow

The recommended workflow for using the web app is:
1. **Add plants** in the [Farm Designer](../Web-App/farm-designer.md): [my.farm.bot/app/designer/plants](https://my.farm.bot/app/designer/plants)
2. **Add [Tools](../Web-App/tools.md)**: [my.farm.bot/app/tools](https://my.farm.bot/app/tools)
3. **Create [Sequences](../Web-App/sequences.md)** for using those tools: [my.farm.bot/app/sequences](https://my.farm.bot/app/sequences)
4. **Create [Regimens](../Web-App/regimens.md)** to repeat sequences at specific times in the days of a plant's life: [my.farm.bot/app/regimens](https://my.farm.bot/app/regimens)
5. **Schedule [Events](../Web-App/events.md)** to execute sequences or regimens: [my.farm.bot/app/designer/events](https://my.farm.bot/app/designer/events)
6. **[Watch](../Web-App/controls.md#camera) your FarmBot work!** [my.farm.bot/app/controls](https://my.farm.bot/app/controls) (Also [my.farm.bot/app/designer](https://my.farm.bot/app/designer))

# Provisioning the web app



{%
include callout.html
type="success"
title="At your service"
content="We offer a hosted service of the web app at [my.farm.bot](https://my.farm.bot). We recommend that most people use this because it is convenient, affordable, and always up-to-date with the latest features and security."
%}



{%
include callout.html
type="warning"
title="For advanced users only"
content="Our [instructions for provisioning the web app](https://developer.farm.bot/v11/Documentation/web-app) are intended for expert users and software developers who wish to run the FarmBot Web App on their own servers. This may be useful for enterprise or off-grid intranet solutions. Nontechnical users are encouraged to use the hosted service at [my.farm.bot](https://my.farm.bot)."
%}


# What's next?

 * [Tools](../Web-App/tools.md)
