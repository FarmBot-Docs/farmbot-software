---
title: "Creating an Account"
slug: "creating-an-account"
description: ":movie_camera: [Video tutorial](https://youtu.be/0EAcUbO6tqo?t=35)"
---

1. Go to [my.farm.bot](https://my.farm.bot)
2. Enter an <span class="fb-input">Email</span>, <span class="fb-input">Name</span>, and <span class="fb-input">Password</span> in the **CREATE AN ACCOUNT** widget
3. Check that you agree to our [privacy policy](http://privacy.farm.bot) and [terms of use](http://tos.farm.bot)
4. Click <span class="fb-button fb-green">Create account</span>
5. Check your email and click the link to confirm your account

# Choose your FarmBot
Clicking the email verification link will log you into the app and take you to the [message center](message-center.md). Here, you'll see a few messages to help you become familiar with the app, as well as one to **Choose your FarmBot**.

Once you let the app know which FarmBot model you have, it will add a set of resources (peripherals, sequences, etc) and apply a set of settings (map size, firmware version, etc) appropriate to your FarmBot model. This will allow you to get started working with your FarmBot more quickly. If you want to start completely from scratch, you can do so by selecting `Custom bot` in the dropdown, or simply dismissing the message center card.

![Choose your FarmBot.png](_images/Choose_your_FarmBot.png)

# Connect FarmBot to your account
1. [Install FarmBot OS](../../Device/farmbot-os.md)
2. [Configure FarmBot](../../Device/farmbot-os/configurator.md) with the same email and password you used to create your web app account
3. Go to [my.farm.bot](https://my.farm.bot) and log in

{%
include callout.html
type="success"
title="Can you hear me now?"
content="The web application should now be in communication with your FarmBot. You should see some bootup logs streaming into the status ticker, and FarmBot should respond to any commands you send it. If there are any problems, see the [troubleshooting guide](../../FarmBot-Software/troubleshooting.md)."
%}

# Using a demo account
If you're thinking about getting a FarmBot but want to try the app first, you can use our **demo account** feature. Simply go to [demo.farm.bot](http://demo.farm.bot) and click <span class="fb-button fb-blue">DEMO THE APP</span> at the bottom of the screen. The demo can be tried on desktop computers, laptops, tablets, and phones.

<div class="laptop" style="perspective: 1000px;">
  <div class="laptop-screen">
    <video muted="" autoplay="" loop="" style="opacity: 0.99;">
      <source src="https://cdn.shopify.com/s/files/1/2040/0289/files/Farm_Designer_Loop.mp4?9552037556691879018" type="video/mp4">
    </video>
  </div>
  <div class="laptop-keyboard">
    <div class="laptop-keys">
    </div>
    <div class="laptop-trackpad">
    </div>
  </div>
</div>

<style>
.laptop {
  margin-bottom: -100px;
}
  
  .laptop-screen {
    padding: 13px 10px 20px;
    margin: auto;
    width: 80%;
    border-radius: 15px;
    background: #111;
    box-shadow: inset 0 -5px 20px rgba(173,186,204,.25), 0 2px 6px rgba(0,21,64,.14), -16px 20px 40px 0px rgba(0,0,0,.15);
    border: 2px solid #bbbaba;
  }
  
  .laptop-screen video {
    width: 100%;
    border-radius: 5px;
  }
  
  .laptop-keyboard {
    border-bottom: 12px solid #434343;
    padding-left: 10px;
    padding-top: 15px;
    border-radius: 30px;
    margin: auto;
    margin-top: -12px;
    width: 80%;
    height: 220px;
    background: #c6ccd0;
    transform: rotateX(75deg);
    transform-origin: 50% 0;
    box-shadow: -20px 30px 40px 0px rgba(0,0,0,.1);
  }
  .laptop-keys {
    background: linear-gradient(45deg,#51565a,#6a7177);
    width: 85%;
    height: 105px;
    margin-left: auto;
    margin-right: auto;
    opacity: 0.7;
  }
  .laptop-trackpad {
    background: linear-gradient(45deg,#51565a,#6a7177);
    width: 30%;
    height: 60px;
    margin-top: 10px;
    margin-left: auto;
    margin-right: auto;
    opacity: 0.7;
  }
</style>



{%
include callout.html
type="info"
title=""
content="Not all features of the app will work in demo mode because there will not be a real FarmBot connected to the account. Additionally, keep in mind that demo accounts and their data are automatically deleted after 1 hour."
%}


# What's next?

 * [Message Center](message-center.md)
