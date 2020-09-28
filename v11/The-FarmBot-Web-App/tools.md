---
title: "Tools"
slug: "tools"
excerpt: "Manage tools and seed containers :hammer: \n[Open this panel in the app](https://my.farm.bot/app/designer/tools)"
---

* toc
{:toc}

On the **tools panel** you can manage all of your FarmBot's **tools**, **seed containers**, and **slots**.

{%
include callout.html
type="info"
title=""
content="Only Genesis kits have interchangeable tools, and the user interface may look slightly different depending on which kit you have."
%}



![Screen Shot 2020-02-20 at 12.57.44 PM.png](Screen_Shot_2020-02-20_at_12.57.44_PM.png)

# Tools and seed containers
## Creating tools and seed containers
To create a new **tool** or **seed container**, press the <span class="fb-button fb-gray"><i class="fa fa-plus"></i></span> button. Provide a <span class="fb-input">Name</span> to define the tool or seed container and then press <span class="fb-button fb-green">SAVE</span>. Alternatively, press <span class="fb-button fb-green"><i class="fa fa-plus"></i> STOCK NAMES</span> to add all of the standard tools and seed containers included with your FarmBot kit.

![Screen Shot 2020-02-20 at 1.00.19 PM.png](Screen_Shot_2020-02-20_at_1.00.19_PM.png)

## Editing tools and seed containers
To edit a tool or seed container, click it from the **TOOLS AND SEED CONTAINERS** list (Genesis), or the **SEED CONTAINERS** list (Express) located at the bottom of the main tools panel. Make your desired edits and then press the <span class="fb-button fb-green">SAVE</span> button.

![Screen Shot 2020-02-20 at 1.06.25 PM.png](Screen_Shot_2020-02-20_at_1.06.25_PM.png)

## Deleting tools and seed containers
To delete a tool or seed container, click it from the **TOOLS AND SEED CONTAINERS** list (Genesis), or the **SEED CONTAINERS** list (Express) located at the bottom of the main tools panel. Then click the <span class="fb-button fb-red">DELETE</span> button.

{%
include callout.html
type="info"
title=""
content="You cannot delete a tool or seed container if it is currently loaded into a tool slot."
%}



![Screen Shot 2020-02-20 at 1.03.20 PM.png](Screen_Shot_2020-02-20_at_1.03.20_PM.png)

# Slots
Once you've added all of your tools and seed containers, its time to load some or all of them into **slots**. Slots are locations within FarmBot's coordinate system that can hold a **tool** or **seed container** and correspond to physical hardware such as a toolbay (Genesis kits) or the gantry-mounted seed trough holder (all kits).

![202d59e-Screen_Shot_2019-05-05_at_11.18.59_PM.png](Screen_Shot_2019-05-05_at_11.18.59_PM.png)

## Creating slots
To create a new slot, press the <span class="fb-button fb-gray"><i class="fa fa-plus"></i></span> button next to the **SLOTS** label in the tools panel.

Next, provide **coordinates** for the tool slot.
  * If you plan to load an **interchangeable tool** into the slot (Genesis kits only), use coordinates for when FarmBot's UTM will fully mount the tool while it is still in the slot.
  * If you plan to load a **seed container** into the slot, use coordinates for when FarmBot's seed injector needle will be positioned to pick up a seed from the container.

To input accurate coordinates, use the manual controls to move FarmBot into the desired position (mounting the tool or picking up a seed). Then click the **USE CURRENT LOCATION** <span class="fb-button fb-light-blue"><i class="fa fa-crosshairs"></i></span> button to copy FarmBot's current coordinates into the **X**, **Y**, and **Z** input fields.

![Screen Shot 2020-02-20 at 1.30.58 PM.png](Screen_Shot_2020-02-20_at_1.30.58_PM.png)

### Changing slot direction
Some slots (such as the toolbays included with Genesis kits) have a **slot direction**, which is the direction that the tool must be loaded and unloaded from. To specify a slot's direction, use the **CHANGE SLOT DIRECTION** dropdown.

![Screen Shot 2020-02-20 at 1.32.12 PM.png](Screen_Shot_2020-02-20_at_1.32.12_PM.png)

### Gantry-mounted slots
Some slots (such as those provided by the seed trough holder) are **gantry-mounted** and move with the FarmBot along the x-axis. To account for this and properly render these types of slots in the farm designer, you can specify that a slot is **GANTRY-MOUNTED** with a checkbox. Doing so will display the **X** coordinate as <span class="fb-input fb-disabled-input">Gantry</span>.

![Screen Shot 2020-02-20 at 1.39.07 PM.png](Screen_Shot_2020-02-20_at_1.39.07_PM.png)

## Loading slots
To load a tool or seed container into the slot, select one from the **TOOL OR SEED CONTAINER** dropdown and then press <span class="fb-button fb-green">save</span>.

![Screen Shot 2020-02-20 at 1.40.08 PM.png](Screen_Shot_2020-02-20_at_1.40.08_PM.png)



{%
include callout.html
type="success"
title="IMPORTANT: The virtual configuration must match real life"
content="Now that you have **virtually** loaded your slots, you must also load the **real** tools and/or seed containers into the **real** slots to match your **virtual** configuration. If you do not do this, FarmBot may perform undesirably. And don't forget: if you change things up in real life (remove a seed bin, for example), you must update the virtual configuration to match."
%}

## Deleting slots
To delete a slot, select it from the **SLOTS** list in the main tools panel and then press the <span class="fb-button fb-red">DELETE</span> button.

{%
include callout.html
type="info"
title=""
content="You cannot delete slots with tools or seed containers that are used in sequences."
%}

