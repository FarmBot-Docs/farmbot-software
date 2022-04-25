---
title: "Regimens"
slug: "regimens"
description: "Plant care recipes for your FarmBot to follow [my.farm.bot/app/regimens](https://my.farm.bot/app/regimens)"
---


<iframe class="embedly-embed" src="//cdn.embedly.com/widgets/media.html?url=http%3A%2F%2Fwww.youtube.com%2Fwatch%3Fv%3DLMUPc8XfxI0&src=http%3A%2F%2Fwww.youtube.com%2Fembed%2FLMUPc8XfxI0&type=text%2Fhtml&key=f2aa6fc3595946d0afc3d76cbbd25dc3&schema=youtube" width="854" height="480" scrolling="no" frameborder="0" allow="autoplay; fullscreen" allowfullscreen="true"></iframe>

**Regimens** allow you to easily take care of a plant throughout its entire life and re-use each "recipe" season after season. To explain the utility of regimens, let's go through a practical example. Imagine you create three sequences for growing Cherry Tomatoes:
1. `Seed Injection`
2. `Light Watering`
3. `Medium Watering`

You decide to grow 10 tomato plants with these sequences starting on **March 1st**. To do this using the [event scheduler](farm-designer/events.md), you might create three events:
1. `Seed Injection` to run on **March 1st**
2. `Light Watering` to run every other day from **March 1st to March 13th**
3. `Medium Watering` to run every other day from **March 15th to April 22nd**

Now imagine you want to grow 10 more tomato plants starting March 9th, and 10 more plants starting March 25th, and 10 more on April 19th. Using the event scheduler, you would need to tediously calculate the timings for each sequence and schedule them three more times each. In total, you will have to make 12 events. **This is what regimens can streamline.**

While the event scheduler works by scheduling an event on a *specific calendar day* such as **March 1st**, regimens work by scheduling events on a *relative day* such as **Day 22** from when the regimen is started. Regimens are therefore a way to bulk re-schedule a set of events starting at any time. Usually the start time coincides with when a plant is started (either sown or transplanted into your garden) though this is not required.

Let's look at our tomatoes example again, this time using a regimen to reach the same outcome. First, we'll make a regimen:
1. `Seed Injection` will run on **Day 1**
2. `Light Watering` will run every other day from **Day 2 to 13**
3. `Medium Watering` will run every other day from **Day 15 to 49**

![Screen Shot 2019-07-15 at 2.22.03 PM.png](_images/Screen_Shot_2019-07-15_at_2.22.03_PM.png)

We can then use events to schedule this regimen to start on March 1st, March 9th, March 25th, and April 19th. Using this method, we created one regimen and four events, instead of the 12 events from before. Plus, we can continue to re-use the regimen each time we want to re-plant tomatoes to save even more time. We can also make changes to the regimen and all of the scheduled instances will be updated automatically.

# Creating a regimen

In the left panel of the **Regimens** page, press the <span class="fb-button fb-green"><i class='fa fa-plus'></i></span> button to create a new regimen. The new regimen will be loaded into the middle **Regimen Editor** panel, and the **Scheduler** will appear in the column on the right. Give your regimen a descriptive name and optionally assign it a color.

![Screen Shot 2019-07-15 at 2.13.04 PM.png](_images/Screen_Shot_2019-07-15_at_2.13.04_PM.png)

In the scheduler panel, select the **SEQUENCE** you wish to add to the regimen. Pick a **TIME** and the **DAYS** for it to run. For this example, we will run the `Seed Injection` sequence at `10am` on `Day 1`. Press the <span class="fb-button fb-green"><i class='fa fa-plus'></i></span> button in the scheduler panel to add the sequence to the regimen.

If you make a mistake, remove items from the regimen by clicking the <i class='fa fa-trash'></i> icon.

![Screen Shot 2019-07-15 at 2.11.27 PM.png](_images/Screen_Shot_2019-07-15_at_2.11.27_PM.png)

Next we'll add a `Light Watering` sequence to the regimen to run at `8PM` every other day for the first two weeks.

![Screen Shot 2019-07-15 at 2.17.38 PM.png](_images/Screen_Shot_2019-07-15_at_2.17.38_PM.png)

Last we'll add a `Medium Watering` sequence to run at `8PM` every other day for weeks 3 through 7, and then press <span class="fb-button fb-green">SAVE</span> to save the regimen.

![Screen Shot 2019-07-15 at 2.22.03 PM.png](_images/Screen_Shot_2019-07-15_at_2.22.03_02.png)

# Running a regimen
A regimen on its own will not execute because the regimen only has enough information to run sequences at a day and time _relative_ from a start date. Thus, to run a regimen, you will have to schedule it using an [event](farm-designer/events.md).

# What's next?

 * [Events](farm-designer/events.md)
