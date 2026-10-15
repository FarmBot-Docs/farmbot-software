---
title: "Tools"
slug: "tools"
description: "Manage tools and seed containers :hammer: \n[Open this panel in the app](https://my.farm.bot/app/designer/tools)"
---

On the **tools panel** you can manage all of your FarmBot's **slots**, **tools**, and **seed containers** as well as view the currently mounted tool.

{%
include callout.html
type="info"
title=""
content="Only Genesis kits have interchangeable tools, and the user interface may look slightly different depending on which kit you have."
%}

![tools panel](_images/tools_panel.png)

# Slots

**Slots** are locations within FarmBot's coordinate system that can hold a **tool** or **seed container** and correspond to physical hardware such as a toolbay (Genesis kits) or the gantry-mounted seed trough holder (all kits).

![slot in map](_images/slot_in_map.png)

## Creating slots

To create a new slot, press the <span class="fb-button fb-gray"><i class='fa fa-plus'></i></span> button next to the **SLOTS** label in the tools panel.

![add new slot](_images/add_new_slot.png)

Next, provide **coordinates** for the tool slot. To input accurate coordinates, use the manual controls to move FarmBot into the target position and then click the **USE CURRENT LOCATION** <span class="fb-button fb-blue"><i class='fa fa-crosshairs'></i></span> button to copy FarmBot's current coordinates into the **X**, **Y**, and **Z** input fields.

Different tools and seed containers will require different coordinates for the slot:

  * **Interchangeable tools** (Genesis kits only) - Use coordinates for when FarmBot's UTM will fully mount the tool while it is still in the slot.
  * **Seed bins** and **seed troughs** - Use coordinates for when FarmBot's seed injector needle will be positioned to pick up a seed from the container.
  * **Seed trays** (with 16 individual cells) - Use coordinates for when FarmBot's seed injector needle is positioned between cells **A2** and **A3**, approximately 1mm above the top of the seed tray. If your tool slot’s pullout direction is in the Negative X direction, position the needle exactly between cells **D2** and **D3**. In either case, the UTM’s main cylindrical section should be aligned with the outer cylindrical face of the seed tray as in the example image below. Then use the [Pick from Seed Tray](https://my.farm.bot/app/shared/sequence/32) featured sequence for picking up seeds from a specific cell in the tray.
  ![seed tray setup](_images/seed_tray_setup.png)

### Changing slot direction

Some slots (such as the toolbays included with Genesis kits) have a **slot direction**, which is the direction that the tool must be loaded and unloaded from. To specify a slot's direction, use the **SLOT DIRECTION** dropdown.

### Axis-mounted slots

Some slots (such as those provided by the seed trough holder) are gantry-mounted and move with the FarmBot along the x-axis. To account for this and properly render these types of slots in the farm designer, you can specify that a slot's **MOUNT STAGE** is the x-axis using the dropdown. Doing so will display the **X** coordinate as <span class="fb-input fb-disabled-input">X axis</span>.

Choose **Stationary**, **X axis**, **Y axis**, or **Z axis** from the **MOUNT STAGE** dropdown. X-axis mounting follows X movement; Y-axis mounting follows X and Y; Z-axis mounting follows all three axes. Use **MOUNT OFFSET** to specify the slot's offset from FarmBot's current position on those axes. Each mounted coordinate is the current bot coordinate plus its mounting offset; unmounted coordinates use the stored slot coordinates.

## Loading slots

To load a tool or seed container into the slot, select one from the **TOOL OR SEED CONTAINER** dropdown and then press <span class="fb-button fb-green">save</span>.

{%
include callout.html
type="success"
title="IMPORTANT: The virtual configuration must match real life"
content="Now that you have **virtually** loaded your slots, you must also load the **real** tools and/or seed containers into the **real** slots to match your **virtual** configuration. If you do not do this, FarmBot may perform undesirably. And don't forget: if you change things up in real life (remove a seed bin, for example), you must update the virtual configuration to match."
%}

![profile view of tools in toolbays](_images/profile_view_of_tools_in_toolbays.png)

## Deleting slots

To delete a slot, select it from the **SLOTS** list in the main tools panel and then press the <span class="fb-button fb-red">DELETE</span> button.

{%
include callout.html
type="info"
title=""
content="You cannot delete slots with tools or seed containers that are used in sequences."
%}

# Tools and seed containers

## Creating tools and seed containers

To create a new **tool** or **seed container**, press the <span class="fb-button fb-gray"><i class='fa fa-plus'></i></span> button. Provide a **NAME**, choose a **TYPE**, and then press <span class="fb-button fb-green">SAVE</span>. Alternatively, you can select from the available **STOCK NAMES** to add one or more of the standard tools and seed containers included with your FarmBot kit.

![add new tool](_images/add_new_tool.png)

## Editing tools and seed containers

To edit a tool or seed container, click it from the **TOOLS AND SEED CONTAINERS** list (Genesis), or the **SEED CONTAINERS** list (Express) located at the bottom of the main tools panel. Make your desired edits and then press the <span class="fb-button fb-green">SAVE</span> button.

The following settings are available when creating or editing a tool or seed container:

* **TYPE** - Choose Rotary Tool, Seed Bin, Seed Tray, Seed Trough, Seeder, Soil Sensor, Watering Nozzle, Weeder, or None. The type determines the tool's standard graphics and available tool actions.
* **UTM MOUNTABLE** - Enable this for tools that can be mounted by the universal tool mount. Only tools with this setting enabled appear in the **MOUNTED TOOL** dropdown. Leave it disabled for seed containers.
* **EFFECTOR OFFSET** - Enter the X, Y, and Z offsets in millimeters from the tool head's reference position to the tool's working tip. An effector below the reference position has a negative Z offset; for example, a seeder tip 80mm below it has a Z offset of `-80`.
* **WATER FLOW RATE (ML/S)** - Available for tools with the **Watering Nozzle** type. Enter the measured flow rate used by dispensing sequences.

## Deleting tools and seed containers

To delete a tool or seed container, click it from the **TOOLS AND SEED CONTAINERS** list (Genesis), or the **SEED CONTAINERS** list (Express) located at the bottom of the main tools panel. Then click the <span class="fb-button fb-red">DELETE</span> button.

{%
include callout.html
type="info"
title=""
content="You cannot delete a tool or seed container if it is currently loaded into a tool slot."
%}

# What's next?

 * [Message Center](intro/message-center.md)
