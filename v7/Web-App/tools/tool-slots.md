---
title: "Tool Slots"
slug: "tool-slots"
description: "Allow FarmBot to find the tools and seed containers [my.farm.bot/app/tools](https://my.farm.bot/app/tools)"
---

* toc
{:toc}

Once you've added all of your tools and seed containers, its time to load some or all of them into **tool slots**. Tool slots are locations within FarmBot's coordinate system that can hold a **tool** or **seed container**.

![toolbay.png](_images/toolbay.png)

# Creating tool slots
To create a new tool slot, press <span class="fb-button fb-gray">edit</span> and then the <span class="fb-button fb-green"><i class='fa fa-plus'></i></span> button.

Next, provide **coordinates** for the tool slot.
  * _If you plan to load an **interchangeable tool** into the slot:_ Use coordinates for when FarmBot's UTM will fully mount the tool while it is still in the slot.
  * _If you plan to load a **seed container** into the slot:_ Use coordinates for when FarmBot's seed injector needle will be positioned to pick up a seed from the container.

To input accurate coordinates, use the manual controls to move FarmBot into the desired position (mounting the tool or picking up a seed). Then click **USE CURRENT LOCATION** <span class="fb-button fb-light-blue"><i class='fa fa-crosshairs'></i></span> in the slot's <i class='fa fa-gear'></i> menu to copy FarmBot's current coordinates into the **X**, **Y**, and **Z** input fields.

![Screen Shot 2019-05-05 at 10.58.35 PM.png](_images/Screen_Shot_2019-05-05_at_10.58.35_PM.png)

## Changing the slot direction
Most tool slots have a **slot direction**, which is the direction that the tool or seed container must be loaded and unloaded from. To specify a tool slot's direction, use the **CHANGE SLOT DIRECTION** dropdown located in the slot's <i class='fa fa-gear'></i> menu.

![Screen Shot 2019-05-05 at 11.12.04 PM.png](_images/Screen_Shot_2019-05-05_at_11.12.04_PM.png)



{%
include callout.html
type="info"
title="Coming soon: gantry-mounted slots"
content="We're working on new hardware and the software to support **gantry-mounted slots**. This will allow FarmBot to, for example, pick up seeds more quickly by simply traversing the Y and Z axes, instead of having to travel all the way back and forth along the X-axis as well when sowing."
%}

# Loading tool slots
Select a tool or seed container from the **TOOL OR SEED CONTAINER** dropdown to load it into the slot.

![Screen Shot 2019-05-05 at 11.08.14 PM.png](_images/Screen_Shot_2019-05-05_at_11.08.14_PM.png)

Press <span class="fb-button fb-green">save</span> when you are finished adding, editing, and loading tool slots.

**IMPORTANT:** Now that you have virtually loaded your tool slots, you must also load the **real** tools and/or seed containers into the **real** tool slots to match your **virtual** configuration. If you do not do this, FarmBot may perform undesirably. And don't forget: if you change things up in real life (remove a seed bin, for example), you must come back to this page in the app to update the virtual configuration to match.

{%
include callout.html
type="info"
title="Your FarmBot might not have interchangeable tools"
content="Depending on your FarmBot version, you may not have interchangeable tools (such as the soil sensor) that need to be loaded into a tool slot. If this is the case, you will only need to load seed containers into tool slots."
%}

# Viewing tools and tool slots in the farm designer
Once you are finished creating tool slots and loading them with tools and/or seed containers, navigate to the farm designer to view them on the map. Hovering over a tool will display its name, and clicking it will navigate you back to the tools page.

![Screen Shot 2019-05-05 at 11.18.59 PM.png](_images/Screen_Shot_2019-05-05_at_11.18.59_PM.png)

# Deleting tool slots
To delete a tool slot, press <span class="fb-button fb-gray">edit</span> and then the <span class="fb-button fb-red"><i class='fa fa-times'></i></span> button for the slot you wish to delete. Finish editing by pressing <span class="fb-button fb-gray">back</span>.
