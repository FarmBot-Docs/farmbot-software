---
title: "Regimens"
slug: "regimens"
description: "Plant care recipes for your FarmBot to follow [my.farmbot.io/app/regimens](http://my.farmbot.io/app/regimens)"
---

* toc
{:toc}


# Regimen Building

To explain the utility of the Regimen Builder, let's go through a practical example. Imagine you create three sequences for growing Cherry Tomatoes:
1. Seed Injection
2. Light Watering
3. Medium Watering

You decide to grow 10 tomato plants with these sequences starting on **March 1st**. To do this using the Event Scheduler, you create three Event Schedules:
1. Seed Injection will run on **March 1st**
2. Light Watering will run everyday from **March 2nd to March 21st**
3. Medium Watering will run everyday from **March 22nd to May 22nd**

Now imagine you want to grow 10 more tomato plants starting March 9th, and 10 more plants starting March 25th, and 10 more on April 19th. Using the Event Scheduler, you would need to tediously schedule your three sequences three more times each. In total, you will have to make 12 Event Schedules. This is what the Regimen Builder aims to streamline.

While the Event Scheduler works by scheduling an event on a *specific calendar day* such as **March 1st**, the Regimen Builder works by scheduling events on a *relative day* such as **Day 22** from when the regimen is started. Regimens are therefore a way to bulk re-schedule a set of events starting at any time.

![regimens.png](_images/regimens.png)

Let's look at our tomatoes example again, this time using the Regimen Builder to reach the same outcome. First, we'll make a Regimen:
1. Seed Injection will run on **Day 1**
2. Light Watering will run everyday from **Day 2 to 21**
3. Medium Watering will run everyday from **Day 22 to 82**

We can then Schedule this Regimen to start on March 1st, March 9th, March 25th, and April 19th.

Using this method, we created one Regimen and four Event Schedules instead of the 12 Event Schedules from before. Plus, we can continue to re-use our Regimen and we'll save even more time. We can also change one Regimen to update all four scheduled instances of the Regimen at once. We alleviate the risk of forgetting one of our sequences or messing up a date calculation when we want to plant tomatoes again using the same method next season.


# Creating a Regimen



![no regimens.png](_images/no_regimens.png)



![new regimen.png](_images/new_regimen.png)



![seed.png](_images/seed.png)



![light.png](_images/light.png)



![light_added.png](_images/light_added.png)



![medium.png](_images/medium.png)



![medium added.png](_images/medium_added.png)


# What's next?

 * [Farm Designer](../Web-App/farm-designer.md)
 * [Farm Events](../Web-App/farm-events.md)
