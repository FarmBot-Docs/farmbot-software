---
title: "Groups"
slug: "groups"
---

* toc
{:toc}

**Groups** allow you to organize the plants in your garden so you can easily run sequences to perform farming operations on many plants, rather than just individual plants. To create and edit groups, navigate to the **groups panel** on the farm designer page.

![Screen Shot 2019-08-15 at 3.13.39 PM.png](_images/Screen_Shot_2019-08-15_at_3.13.39_PM.png)

# Creating a group
To create a group, click the <span class="fb-button fb-blue"><i class='fa fa-plus'></i></span> button on the groups panel. This will open up the [multi-select mode](../../Web-App/farm-designer.md#select-mode) in the farm designer. Click and hold anywhere in the map and then drag the mouse cursor to create a **box selection** of the plants you wish to add to the group. Then click <span class="fb-button fb-blue">CREATE GROUP</span>.

![Groups 2.png](_images/Groups_2.png)

# Editing a group
Upon creating a group, the **edit group** panel will be opened. From here, you can change the **GROUP NAME** and make further edits. When you are finished editing, press the <i class='fa fa-arrow-left'></i> to save your changes and go back to the list of all groups.

## Sort by
The **SORT BY** method will change the ordering that FarmBot uses when traveling to each plant in the group when the group is used in a sequence. A dashed line will be shown in the map visualizing the path. Sorting options include `X/Y, Ascending`, `X/Y, Descending`, `Y/X, Ascending`, `Y/X, Descending`, and `Random Order`. We encourage you to play around with this option to find the most efficient path FarmBot can take.

![Groups 3.png](_images/Groups_3.png)



{%
include callout.html
type="info"
title="On the roadmap"
content="In the future we hope to offer additional sorting options for more efficient FarmBot operation, such as a [Traveling Salesman](https://en.wikipedia.org/wiki/Travelling_salesman_problem) option."
%}

## Adding group members
To add a plant to the group, click its icon in the farm designer map.

## Removing group members
To remove a plant from the group, click its icon in the **GROUP MEMBERS** list. When mousing over icons in this list, the corresponding icon in the map will be highlighted, allowing you to ensure you're removing the correct plant.

# Using groups
Once you're happy with your group, try it in a sequence! Simply create a sequence with an [externally defined location variable](../../Web-App/sequences/externally-defined-variables.md):

![Groups 4.png](_images/Groups_4.png)

Then use the <span class="fb-button fb-orange">TEST</span> button, making sure to select your group:

![Groups 4b.png](_images/Groups_4b.png)

Once you've verified that FarmBot is operating how you intend, you can run this sequence over your group of plants with an <span class="fb-step fb-execute">EXECUTE SEQUENCE</span> command in another sequence, or in a regimen, or an event!

![Groups 4c.png](_images/Groups_4c.png)

# Deleting a group
To delete a group, click the <span class="fb-button fb-red">DELETE GROUP</span> button. Note that you cannot delete a group that is in-use by a sequence, regimen, or event.

# What's next?

 * [Gardens](gardens.md)
