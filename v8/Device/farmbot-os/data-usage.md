---
title: "Data Usage"
slug: "data-usage"
---

Depending on how you setup your FarmBot, the device will send and receive different amounts of data. For users who are connecting the device to the internet with a cellular or other metered data connection plan, the amount of data transmitted may be of concern.

{%
include callout.html
type="warning"
title="For reference only"
content="The numbers in this document are for reference only, and meant to serve as a starting point for estimating the amount of data your FarmBot will use. These numbers are not meant to show the exact amount of data your device will use, as that will depend on your exact configuration and other variables. FarmBot Inc cannot be held liable for unexpected data usage charges."
%}

# Average data required by task
The table below shows the average amounts of data transmitted and received by the FarmBot to complete various tasks. Again, these are average amounts; actual data required may be more or less depending on your configuration.

|Task                          |Transmitted                   |Received                      |Total                         |
|------------------------------|------------------------------|------------------------------|------------------------------|
|Log sent from FarmBot         |200 bytes                     |200 bytes                     |400 bytes
|Command sent to FarmBot       |200 bytes                     |200 bytes                     |400 bytes
|Partial sync                  |200 bytes                     |200 bytes                     |400 bytes
|Full sync                     |30KB - 150KB                  |30KB - 150KB                  |60KB - 300KB
|Image upload                  |100KB - 500KB                 |200 bytes                     |100KB - 500KB
|Over-the-air update           |1MB                           |60MB                          |61MB

# Practical examples
## Manually controlling FarmBot for an hour
Let's say you are demonstrating FarmBot to a group of people for one hour. In this time period, you send the FarmBot 300 manual control commands (movements, toggling peripherals, reading sensors, testing sequences, etc), perform 10 full syncs, and upload 30 photos. This would result in approximately 120KB in manual control commands, 0.6MB - 30MB for the syncing, and 3MB - 15MB for the photos. Thus, you may expect the FarmBot to use between 4MB and 45MB of total data for the hour long demo.

## FarmBot on auto-pilot
Let's say you have configured your FarmBot to run 20 farm events each day, take 50 photos a day, you've enabled auto-sync, and turned on automatic updates. We'll estimate that the average farm event executes 100 sequence steps and generates 500 logs; the average image size will be 200KB; the bot will perform a 100KB full auto-sync every 30 minutes; and the OS will be updated once per week. Thus, over one month you might expect FarmBot to require 120MB for logs, 150MB for syncing, 300MB for photos, and 250MB for updates (820MB total).
