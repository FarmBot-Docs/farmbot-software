---
title: "Connectivity Diagnosis Codes"
slug: "connectivity-codes"
description: "These are the codes that will tell you how to get communication to your FarmBot"
---

The connectivity tool is used to diagnose the status of communications between the nodes within the FarmBot. Communication must be established between the Browser, the Web App, Message Broker and the FarmBot. This tool will tell you where the communications are breaking down within the FarmBot system. In order for the FarmBot to operate properly all the points of communication need to be functioning.

![Connectivity diagnosis code](_images/connectivity_diagnosis_code.jpg)



|Color                                            |Meaning                       |
|-------------------------------------------------|------------------------------|
|<span class="fa fa-circle green"></span> Green   |Status OK
|<span class="fa fa-circle yellow"></span> Yellow |The status is unknown. There is no data available about the status of communication.
|<span class="fa fa-circle red"></span> Red       |Status NOT OK. Take corrective action to resolve this communication disconnect

This is the list of the 32 possible diagnosis codes that will help you to troubleshoot the communications of your FarmBot:

# Code 0
```
There is no access to FarmBot or the message broker. This is usually caused by outdated browsers (Internet Explorer) or firewalls that block WebSockets on port 3002.
```

**Corrective Action**:

1. Update your internet browser to the most current version. Google Chrome is the preferred FarmBot Web App browser.
2. Check for blocked WebSockets in your firewall on port 3002.
3. Test your WebSockets using this website: https://www.websocket.org/echo.html

_Note 1:_ Please note that we have experienced several difficulties with School firewalls.
In one particular school firewall, the IT department opened port 3002 for FarmBot operation but the port was automatically blocked again after a set timeout.

_Note 2:_ This code will not show up on the blue communications LED. Blocked access to port 3002 will affect the browser rather than the device, so in this case, the "browser <=> broker" leg of the connectivity pop-up will be RED.

The tricky part is identifying root cause. A red "browser <=> broker" leg is almost always caused by blocked websocket access, but it is also possible that our broker is down.

So to summarize: A red "browser <=> broker" leg almost always means a port is blocked (if you discount the possibility of a broker outage, which is extremely rare), but different school networks block the port in different ways.

# Code 1
```
You are either offline, using a web browser that does not support WebSockets, or are behind a firewall that blocks port 3002. Do not attempt to debug FarmBot hardware until you solve this issue first. You will not be able to troubleshoot hardware issues without a reliable browser and internet connection.
```

**Corrective Action**:

1. Check to make sure that your device has an active internet connection.
2. Check to make sure that your internet browser supports WebSockets. FarmBot only supports Google Chrome and Firefox and these browsers both support WebSockets. FarmBot Inc. prefers the users choose chrome for the FarmBot Web App.
3. Check for blocked WebSockets in your firewall on port 3002.
Test your websockets using this website: https://www.websocket.org/echo.html

_Note:_ Please note that we have experienced several difficulties with School firewalls.
In one particular school firewall, the IT department opened port 3002 for FarmBot operation but the port was automatically blocked again after a set timeout.

# Code 2
```
You are either offline, using a web browser that does not support WebSockets, or are behind a firewall that blocks port 3002. Do not attempt to debug FarmBot hardware until you solve this issue first. You will not be able to troubleshoot hardware issues without a reliable browser and internet connection.
```

**Corrective Action**: See [Code 1](#code-1)

# Code 3
```
You are either offline, using a web browser that does not support WebSockets, or are behind a firewall that blocks port 3002. Do not attempt to debug FarmBot hardware until you solve this issue first. You will not be able to troubleshoot hardware issues without a reliable browser and internet connection.
```

**Corrective Action**: See [Code 1](#code-1)

# Code 4
```
You are either offline, using a web browser that does not support WebSockets, or are behind a firewall that blocks port 3002. Do not attempt to debug FarmBot hardware until you solve this issue first. You will not be able to troubleshoot hardware issues without a reliable browser and internet connection.
```

**Corrective Action**: See [Code 1](#code-1)

# Code 5
```
You are either offline, using a web browser that does not support WebSockets, or are behind a firewall that blocks port 3002. Do not attempt to debug FarmBot hardware until you solve this issue first. You will not be able to troubleshoot hardware issues without a reliable browser and internet connection.
```

**Corrective Action**: See [Code 1](#code-1)

# Code 6
```
You are either offline, using a web browser that does not support WebSockets, or are behind a firewall that blocks port 3002. Do not attempt to debug FarmBot hardware until you solve this issue first. You will not be able to troubleshoot hardware issues without a reliable browser and internet connection.
```

**Corrective Action**: See [Code 1](#code-1)

# Code 7
```
You are either offline, using a web browser that does not support WebSockets, or are behind a firewall that blocks port 3002. Do not attempt to debug FarmBot hardware until you solve this issue first. You will not be able to troubleshoot hardware issues without a reliable browser and internet connection.
```

**Corrective Action**: See [Code 1](#code-1)

# Code 8
```
Your browser is connected correctly, but we have no recent record of FarmBot connecting to the internet. This usually happens because of a bad WiFi signal in the garden, a bad password during configuration, or a very long power outage.
```

**Corrective Action**:
1. Check the WiFi signal to the FarmBot. If you are having trouble with your internet connection please connect using an Ethernet cable or see our troubleshooting document for more information: https://software.farm.bot/docs/connecting-farmbot-to-the-internet
2. Judging by your network error code you entered a bad email or password while configuring and the device cannot connect to the server. Check to make sure that you have not entered a bad password during configuration.

   In this step of the configurator we expect that there was likely an error with the E-mail and/or Password. Please see the graphic below.

   ![CODE 24 CONFIGURATOR](_images/code_24_configurator.png)

   _CODE 8 AND CODE 24 BAD E-MAIL AND/OR PASSWORD IN CONFIGURATOR_

   If you entered a wrong E-mail and/or Password in this step you will need to re-flash your SD card and start the configurator process again.

   Also there is a chance that your local network does not allow access to AMQP, MQTT, NTP and/or https://my.farm.bot.

   1. AMQP (PORT: 5672) or MQTT (PORT: 8883) is a blocked port. Unblock this port to resolve this issue. This may require help from your IT professionals.

   2. For NTP issues the FarmBot users will see log entries that say "expired certificate" and the logs coming from the device will not have the correct time. If you have this issue contact FarmBot technical support.

   3. For A user being able to access my.farm.bot from a desktop computer is not the same thing as a FarmBot being able to access my.farm.bot (this is a common error). Also, the WiFi could cut out after the Web App loads. Since it's a single page Web App, it is possible to navigate the site during network outages.

3. Check to make sure that your FarmBot has not been powered off due to a long power outage.
_Note:_ Some older FBOS versions and specific FBOS config settings may result in a soft reset that the user did not anticipate.

# Code 9
```
Your browser is connected correctly, but we have no recent record of FarmBot connecting to the internet. This usually happens because of a bad WiFi signal in the garden, a bad password during configuration, or a very long power outage.
```

**Corrective Action**: See [Code 8](#code-8)

# Code 10
```
FarmBot and the browser are both connected to the internet (or have been recently). Try rebooting FarmBot and refreshing the browser. If the issue persists, something may be preventing FarmBot from accessing the message broker (used to communicate with your web browser in real-time). If you are on a company or school network, a firewall may be blocking port 5672 or 8883.
```

**Corrective Action**:
1. Try rebooting FarmBot and refreshing the browser.
2. A firewall may be blocking port 5672 or 8883. Check these ports to see if they are blocked. If you are a company or a school please have your IT professional review [this document](for-it-security-professionals.md).
3. On FarmBot Genesis 1.4+ or FarmBot Express check the blue LED communication light. You have blocked ports if the blue LED is OFF <span class="fa fa-circle-thin led blue"></span> and the green LED is on <span class="fa fa-circle led green"></span>. (Only FarmBot Genesis v1.4+ and FarmBot Express models have this diagnostic green and blue LEDs.)

Please review our [troubleshooting document](connecting-farmbot-to-the-internet.md).

# Code 11
```
FarmBot and the browser are both connected to the internet (or have been recently). Try rebooting FarmBot and refreshing the browser. If the issue persists, something may be preventing FarmBot from accessing the message broker (used to communicate with your web browser in real-time). If you are on a company or school network, a firewall may be blocking port 5672 or 8883.
```

**Corrective Action**: See [Code 10](#code-10)

# Code 12

```
Farmduino firmware is missing or is possibly unplugged. Verify FIRMWARE selection matches FarmBot kit version or check the USB cable between the Raspberry Pi and the Farmduino. Reboot FarmBot after a reconnection. If the issue persists, reconfiguration of FarmBot OS may be necessary.
```

**Corrective Action**:
1. For Genesis models, ensure the square USB cable between the Raspberry Pi and the Arduino is properly connected by unplugging and re-plugging the cable. It may have come loose during operation.
2. Next, ensure your firmware setting matches the FarmBot model you purchased. For example, if you purchased a FarmBot Express v1.0, ensure that the firmware selection dropdown says `Farmduino (Express v1.0)` on the [firmware selection dropdown](https://my.farm.bot/app/designer/settings?highlight=firmware). Selecting the wrong firmware version is one of the most common causes of code 12 / code 30 errors.

   ![firmware selection dropdown](_images/firmware_selection_dropdown.png)

3. Re-apply the firmware by hitting the <span class="fb-button fb-yellow">FLASH FIRMWARE</span> button located [here](https://my.farm.bot/app/designer/settings?highlight=firmware). Wait until the device says the firmware was successfully flash before proceeding (will appear in the logs menu area).
4. Perform a "hard reboot" of the device by unplugging the power, waiting for 10 seconds and re-applying power to the device.
5. If you still get this code reconfiguration of FarmBot OS may be necessary. This would mean the user needs to hit the <span class="fb-button fb-red">SOFT RESET</span> button located [here](https://my.farm.bot/app/designer/settings?highlight=soft_reset).
6. If the firmware is still not connected to the device after a power cycle and re-configuration, contact customer support for further remediation steps.

# Code 13
```
FarmBot and the browser both have internet connectivity, but we haven't seen any activity from FarmBot on the Web App in a while. This could mean that FarmBot has not synced in a while, which might not be a problem. If you are experiencing usability issues, however, it could be a sign of HTTP blockage on FarmBot's local internet connection.
```

**Corrective Action**:
1. Check for HTTP blockage on port 80 HTTP(S) and port 443 HTTP(S).
2. On FarmBot Genesis 1.4+ or FarmBot Express check the blue LED communication light. You have blocked ports if the blue LED is OFF <span class="fa fa-circle-thin led blue"></span> and the green LED is on <span class="fa fa-circle led green"></span>. (Only FarmBot Genesis v1.4+ and FarmBot Express models have this diagnostic green and blue LEDs.)

# Code 14
```
Farmduino firmware is missing or is possibly unplugged. Verify FIRMWARE selection matches FarmBot kit version or check the USB cable between the Raspberry Pi and the Farmduino. Reboot FarmBot after a reconnection. If the issue persists, reconfiguration of FarmBot OS may be necessary.
```

**Corrective Action**: See [Code 12](#code-12)

# Code 15
```
You are either offline, using a web browser that does not support WebSockets, or are behind a firewall that blocks port 3002. Do not attempt to debug FarmBot hardware until you solve this issue first. You will not be able to troubleshoot hardware issues without a reliable browser and internet connection.
```

**Corrective Action**: See [Code 1](#code-1)

# Code 16
```
You are either offline, using a web browser that does not support WebSockets, or are behind a firewall that blocks port 3002. Do not attempt to debug FarmBot hardware until you solve this issue first. You will not be able to troubleshoot hardware issues without a reliable browser and internet connection.
```

**Corrective Action**: See [Code 1](#code-1)

# Code 17
```
You are either offline, using a web browser that does not support WebSockets, or are behind a firewall that blocks port 3002. Do not attempt to debug FarmBot hardware until you solve this issue first. You will not be able to troubleshoot hardware issues without a reliable browser and internet connection.
```

**Corrective Action**: See [Code 1](#code-1)

# Code 18
```
You are either offline, using a web browser that does not support WebSockets, or are behind a firewall that blocks port 3002. Do not attempt to debug FarmBot hardware until you solve this issue first. You will not be able to troubleshoot hardware issues without a reliable browser and internet connection.
```

**Corrective Action**: See [Code 1](#code-1)

# Code 19
```
You are either offline, using a web browser that does not support WebSockets, or are behind a firewall that blocks port 3002. Do not attempt to debug FarmBot hardware until you solve this issue first. You will not be able to troubleshoot hardware issues without a reliable browser and internet connection.
```

**Corrective Action**: See [Code 1](#code-1)

# Code 20
```
You are either offline, using a web browser that does not support WebSockets, or are behind a firewall that blocks port 3002. Do not attempt to debug FarmBot hardware until you solve this issue first. You will not be able to troubleshoot hardware issues without a reliable browser and internet connection.
```

**Corrective Action**: See [Code 1](#code-1)

# Code 21
```
You are either offline, using a web browser that does not support WebSockets, or are behind a firewall that blocks port 3002. Do not attempt to debug FarmBot hardware until you solve this issue first. You will not be able to troubleshoot hardware issues without a reliable browser and internet connection.
```

**Corrective Action**: See [Code 1](#code-1)

# Code 22
```
You are either offline, using a web browser that does not support WebSockets, or are behind a firewall that blocks port 3002. Do not attempt to debug FarmBot hardware until you solve this issue first. You will not be able to troubleshoot hardware issues without a reliable browser and internet connection.
```

**Corrective Action**: See [Code 1](#code-1)

# Code 23
```
You are either offline, using a web browser that does not support WebSockets, or are behind a firewall that blocks port 3002. Do not attempt to debug FarmBot hardware until you solve this issue first. You will not be able to troubleshoot hardware issues without a reliable browser and internet connection.
```

**Corrective Action**: See [Code 1](#code-1)

# Code 24
```
Your browser is connected correctly, but we have no recent record of FarmBot connecting to the internet. This usually happens because of a bad WiFi signal in the garden, a bad password during configuration, or a very long power outage.
```

**Corrective Action**: See [Code 8](#code-8)

# Code 25
```
Your browser is connected correctly, but we have no recent record of FarmBot connecting to the internet. This usually happens because of a bad WiFi signal in the garden, a bad password during configuration, or a very long power outage.
```

**Corrective Action**: See [Code 8](#code-8)

# Code 26
```
FarmBot and the browser are both connected to the internet (or have been recently). Try rebooting FarmBot and refreshing the browser. If the issue persists, something may be preventing FarmBot from accessing the message broker (used to communicate with your web browser in real-time). If you are on a company or school network, a firewall may be blocking port 5672 or 8883.
```

**Corrective Action**: See [Code 10](#code-10)

# Code 27
```
FarmBot and the browser are both connected to the internet (or have been recently). Try rebooting FarmBot and refreshing the browser. If the issue persists, something may be preventing FarmBot from accessing the message broker (used to communicate with your web browser in real-time). If you are on a company or school network, a firewall may be blocking port 5672 or 8883.
```

**Corrective Action**: See [Code 10](#code-10)

# Code 28
```
Farmduino firmware is missing or is possibly unplugged. Verify FIRMWARE selection matches FarmBot kit version or check the USB cable between the Raspberry Pi and the Farmduino. Reboot FarmBot after a reconnection. If the issue persists, reconfiguration of FarmBot OS may be necessary.
```

**Corrective Action**: See [Code 12](#code-12)

# Code 29
```
FarmBot and the browser both have internet connectivity, but we haven't seen any activity from FarmBot on the Web App in a while. This could mean that FarmBot has not synced in a while, which might not be a problem. If you are experiencing usability issues, however, it could be a sign of HTTP blockage on FarmBot's local internet connection.
```

**Corrective Action**:
1. Press the refresh button on your browser

   ![Refresh button in Google Chrome](_images/Refresh_button_in_Google_Chrome.bmp)
   _Refresh button in Google Chrome_

2. Try Syncing the FarmBot
3. Check for HTTP blockage on FarmBot's local internet connection
4. On FarmBot Genesis 1.4+ or FarmBot Express check the blue LED communication light. You have blocked ports if the blue LED is OFF <span class="fa fa-circle-thin led blue"></span> and the green LED is on <span class="fa fa-circle led green"></span>. (Only FarmBot Genesis v1.4+ and FarmBot Express models have this diagnostic green and blue LEDs.)

# Code 30

```
Farmduino firmware is missing or is possibly unplugged. Verify FIRMWARE selection matches FarmBot kit version or check the USB cable between the Raspberry Pi and the Farmduino. Reboot FarmBot after a reconnection. If the issue persists, reconfiguration of FarmBot OS may be necessary.
```

**Corrective Action**: See [Code 12](#code-12)

# Code 31
```
All systems nominal.
```

**No corrective action required.** All the points of communication are functioning.

![Connectivity diagnosis code31](_images/connectivity_diagnosis_code31.jpg)
