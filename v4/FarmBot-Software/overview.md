---
title: "High Level Overview"
slug: "overview"
excerpt: "Description of the FarmBot software toolchain"
---

* toc
{:toc}

There are many software systems contributing to FarmBot's functionality. The diagram below shows the different components and how data flows between them. Read the brief descriptions of each component in the following sections to understand the system as a whole, and then dive into setting up the needed components for your FarmBot.

<div class="software-overview-image">
  <a href="https://cloud.githubusercontent.com/assets/12681652/19332443/e0345a90-90a0-11e6-85ce-0a9aa03a7ea9.png">
  <img src="https://cloud.githubusercontent.com/assets/12681652/19332287/59a73138-909f-11e6-956a-6b3836779c54.png" />
  </a>

  <p style="top:3%;left:0%;font-size:20px;width:100%">FarmBot Software High Level Overview</p>

  <p style="top:10%;left:62%;font-size:10px;">User</p>
  <p style="top:25%;left:63%;">Farm Design, Commands</p>
  <p style="top:28%;left:67%;">Logs, Sensor Data, Photos, Video</p>

  <p style="top:10%;left:0%;font-size:10px;">Web</p>
  
  <p style="top:15%;left:3%;font-size:10px;">External Resources</p>
  <p style="top:22.5%;left:2%;font-size:12px;color:white">OpenFarm.cc</p>
  <p style="top:25%;left:2%;color:white">(crop database)</p>
  <p style="top:31%;left:2%;font-size:10px;">Local Weather</p>
  <p style="top:33%;left:2%;">(any source)</p>
  <p style="top:36%;left:4.5%;">Rain, temperature, humidity</p>

  <p style="top:18%;left:20%;font-size:10px;width:30%">FarmBot Cloud Services</p>
  <p style="top:21%;left:20%;width:30%">Crop Information, growing regimens</p>
  <p style="top:24%;left:46%;font-size:10px;">Farmbot Web App</p>
  <p style="top:26%;left:46%;">(hosted service at my.farmbot.io)</p>
  <p style="top:28%;left:30%;">Events, Sensor Data</p>
  <p style="top:36%;left:21%;font-size:10px;width:30%;color:white">Decision Support System</p>
  <p style="top:38%;left:21%;width:30%;color:white">(hosted service at dss.farmbot.io)</p>
  <p style="top:42%;left:40%;">Commands</p>
  <p style="top:38%;left:59%;max-width:50px;">Logs, Sensor Data, Video, Photos</p>
  <p style="top:49%;left:30%;">Optimized Events</p>
  <p style="top:46.5%;left:46%;font-size:10px;color:white">MQTT Gateway</p>
  <p style="top:48.5%;left:41%;width:30%;color:white">(hosted service at mqtt.farmbot.io)</p>
  <p style="top:54%;left:34%;">Optimized Events, Commands</p>
  <p style="top:54%;left:52%;width:30%">Logs, Sensor Data, Video, Photos</p>

  <p style="top:58%;left:14%;font-size:10px;">FarmBot Device</p>
  <p style="top:59%;left:30%;font-size:10px;">Raspberry Pi</p>
  <p style="top:61%;left:30%;">(FarmBot OS)</p>
  <p style="top:64%;left:41%;font-size:10px;width:30%;color:white">Raspberry Pi Controller</p>
  <p style="top:63.5%;left:20%;">Video, Photos</p>
  <p style="top:68%;left:14.5%;font-size:10px;">Webcam</p>
  <p style="top:69.5%;left:56%;font-size:10px;width:30%;color:black">FarmBot Configurator</p>
  <p style="top:71%;left:78%;">WiFi and web app credentials</p>
  <p style="top:63.5%;left:61%;">Credentials</p>
  <p style="top:74%;left:37%;">G and F codes</p>
  <p style="top:74%;left:58%;">Logs, Sensor (Pin,Encoder) Data</p>

  <p style="top:79%;left:28%;font-size:10px;">Arduino/RAMPS</p>
  <p style="top:78.5%;left:46%;font-size:10px;color:white">Arduino Firmware</p>
  <p style="top:86%;left:37%;">Step and Direction Pulses</p>
  <p style="top:90%;left:37%;">Rotary Encoder Data</p>
  <p style="top:93%;left:10%;font-size:10px;width:50%">Stepper Motors and Rotary Encoders</p>
  <p style="top:78%;left:65%;">Read Pins</p>
  <p style="top:86%;left:52%;">Write Pins</p>
  <p style="top:93%;left:60%;font-size:10px;">Tools</p>
  <p style="top:93%;left:72%;font-size:10px;">Sensors</p>
  <p style="top:87.25%;left:57%;color:white">Seeds</p>
  <p style="top:87.25%;left:62.25%;color:white">Water</p>
  <p style="top:87.25%;left:71%;color:white">pH</p>
</div>

<style>
img {
  width: 100%;
}
.software-overview-image { 
  position: relative; 
  width: 100%;
  border: 1px solid #d0d0d0;
}
.software-overview-image p {
  position: absolute; 
  font-size: 7px;
  font-weight: bold;
  text-align: center;
  width: 20%;
  color: black;
}
</style>



{%
include callout.html
type="info"
title="Everything is open-source"
content="All of our software is licensed permissively with the [MIT license](https://opensource.org/licenses/MIT), allowing you to contribute to, copy, modify, redistribute, and even sell FarmBot software. Want to help build new features or have a bug to report? [Get involved on GitHub!](https://github.com/FarmBot)"
%}



{%
include callout.html
type="success"
title="We're here to help"
content="Have a question or need help setting up some of the software? You can ask a question and find answers in our [forum](http://forum.farmbot.org/)!"
%}



# FarmBot Cloud Services

## The FarmBot Web Application
The web app allows you to easily configure and control your FarmBot from a web browser on your laptop, tablet, or smartphone. The application features real-time manual controls and logging, a sequence builder for creating custom routines for FarmBot to execute, and a drag-and-drop farm designer so you can graphically design and manage your farm.

![Farm Designer V7.png](1Yj70fCFTGyPQYbg68jj_Farm_Designer_V7.png)

## MQTT Gateway
The MQTT Gateway is a cloud application that acts as an intermediary for all messages between the FarmBot web app and FarmBot devices. It handles socket connections, device identification, and authentication.

## Coming soon: Decision Support System
The decision support system (DSS) is a cloud service that employs fine tuned algorithms to optimize scheduled events based on relevant data. For example, the DSS may optimize a watering sequence to use more or less water based on the weather forecast.

# Device Software

## FarmBot Raspberry Pi Controller
FarmBot's Raspberry Pi uses this software to maintain a connection and synchronize with the web application via FarmBot Mesh. This allows FarmBot to download and execute scheduled events, be controlled in real-time, and upload logs and sensor data. The controller communicates with the Arduino over USB to send G and F code commands and also receive collected data.

## Farmbot Arduino Firmware
This software is flashed onto FarmBot's Arduino MEGA 2560 microcontroller and is responsible for physically operating FarmBot's hardware, tools, sensors, and other electronics. It receives G and F codes from FarmBot Raspberry Pi Controller via the USB serial connection, and then moves the motors and reads and writes pins accordingly. It also sends collected data from the rotary encoders and pin reads back to the Raspberry Pi.

## WiFi Configurator
FarmBot OS has a WiFi Configurator utility built in allowing you to easily enter WiFi and web app credentials from a WiFi enabled device (such as a laptop or smartphone). This is useful for initial setup in order to get your FarmBot connected to your home WiFi.

# External Resources

## OpenFarm.cc
[OpenFarm](https://openfarm.cc) is a free and open database for farming and gardening knowledge. This service provides crop and growing information to the web app for a streamlined user experienced.

{%
include callout.html
type="success"
title="OpenFarm is built by us too!"
content="[OpenFarm.cc](https://openfarm.cc) was originally conceived as a small component of the FarmBot project. As progress was made, it became clear that OpenFarm had no reason to be tied to FarmBot, but could rather live on its own. In September of 2014, 1,605 people [backed OpenFarm on Kickstarter](https://www.kickstarter.com/projects/roryaronson/openfarm-learn-to-grow-anything/). Today, OpenFarm is a standalone application, non-profit, and community. You can get involved with OpenFarm by joining the [Slack channel](http://slack.openfarm.cc), contributing on [GitHub](https://github.com/openfarmcc), or going to [OpenFarm.cc](https://openfarm.cc) and creating content!"
%}



# Syncronization and Data Exchange

Data is exchanged across the web application, Raspberry Pi controller, and the user's web browser session in three ways.

## Automatic and manual synchronization
FarmBot's Raspberry Pi controller automatically synchronizes with the web application every hour and with manual initiation from the user via the browser. The data that is transferred during synchronization includes logs, configuration settings, sensor data, sequences, schedules, and events. The diagram below explains how this works.

<div class="translatable-image-flow">
  <!--<a href="FarmBot_Syncing_Flows.png">-->
  <img src="https://cloud.githubusercontent.com/assets/12681652/15723358/e4639daa-27f6-11e6-9db9-ed35f7a69d25.png" />
  <!--</a>-->
  
  <p style="top:3%;left:21%;font-size:12px;font-weight:bold;">Regular, Autonomous Syncing</p>
  <p style="top:7%;left:21%;">
    1. Device polls the Web App and says: <i>Let's Sync! Here is my new Sensor Data and Logs</i>
    <br />
    2. Web App sends back: <i>Got it, and here's some new Events for you</i>
    <br />
    3. Device sends back: <i>Got it, thanks. See you again in 15</i></p>
  
  <p style="top:21%;left:2%;font-size:12px;font-weight:bold;text-align: center;width:30%">FarmBot Device</p>
  <p style="top:26%;left:2%;text-align: center;width:30%">Stores: Sensor Data, Events, and Logs</p>
  
  <p style="top:19%;left:38%;">Sensor Data, Logs<br /><br />Confirmation, Events<br /><br />Confirmation</p>
  
  <p style="top:21%;left:60%;font-size:12px;font-weight:bold;text-align: center;width:30%">Web App (The Cloud)</p>
  <p style="top:25%;left:55%;width:40%;text-align: center;">Stores: Users, FarmBots, Sensor Data, Zones, Plant Groups, Plants, Events, Sequences, Operations, and Logs</p>

  <p style="top:40%;left:23%;font-size:12px;font-weight:bold;">Manual Syncing by the User</p>
  <p style="top:43%;left:23%;">
    1. User presses the Sync button
    <br />
    2. Browser sends Web App: <i>Here are some updated Sequences, Plants, Plant Groups, Zones, and Events</i>
    <br />
    3. Web App says back: <i>Got it, thanks</i>
    <br />
    4. Browser sends Device: <i>Hey, I updated the Web App, go sync!</i>
    <br />
    5. Device does the three step syncing flow (above)
    <br />
    6. Device sends Browser: <i>I'm done syncing</i>
    <br />
    7. Browser asks Web App: <i>Yo, give me the latest Sensor Data and Logs</i>
    <br />
    8. Web App says: <i>Okay, here ya go</i>
    <br />
    9. Browser says: <i>Thanks!</i></p>
  
  <p style="top:68%;left:32%;font-size:12px;font-weight:bold;text-align: center;width:30%">Web App (The Cloud)</p>
  <p style="top:73%;left:28%;width:40%;text-align: center;">Stores: Users, FarmBots, Sensor Data, Zones, Plant Groups, Plants, Events, Sequences, Operations, and Logs</p>
  
  <p style="top:72.5%;left:10%">Sensor Data, Logs</p>
  
  <p style="top:88%;left:6%;font-size:12px;font-weight:bold;text-align: center;width:30%">FarmBot Device</p>
  <p style="top:93%;left:6%;text-align: center;width:30%">Stores: Sensor Data, Events, and Logs</p>
  
  <p style="top:87.5%;left:38%;">Events</p>
  <p style="top:87.5%;left:49%;">Sensor Data, Logs</p>
  <p style="top:91%;left:45%;">Go sync!<br /><br />I'm done syncing</p>

  
  <p style="top:88%;left:65%;font-size:12px;font-weight:bold;text-align: center;width:30%">Browser UI</p>
  <p style="top:93%;left:65%;width:28%;text-align: center;">Modifies: all data of the Web App except Sensor Data and Logs</p>
  
  <p style="top:70%;left:76%;width:20%">Sequences, Plants, Plant Groups, Zones, Events</p>
  
</div>

<style>
img {
  width: 100%;
}
.translatable-image-flow { 
    position: relative; 
  width: 100%;
  border: 1px solid #d0d0d0;
}
.translatable-image-flow p {
  position: absolute; 
  font-size: 10px;
  width: 50%;
  color: black;
}
</style>

## Real-time data exchange
In addition to synchronization, data is also exchanged in real-time between the user's web browser and the FarmBot device. This is used for emergency stop and real-time control commands, as well as real-time log and video streaming.
