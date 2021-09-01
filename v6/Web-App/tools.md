---
title: "Tools"
slug: "tools"
description: "Specify tools for FarmBot's Universal Tool Mount to use [my.farm.bot/app/tools](https://my.farm.bot/app/tools)"
---

* toc
{:toc}

On this page you can specify the location of the tools in the tool bay so that FarmBot can use them with its Universal Tool Mount.

<div class="nav-image">
  <img class="nav-image" src="_images/tools_page.png" alt="Tools page" />
  <a href="#toolbay" style="top: 16.56%; left: 3.9%; width: 52.77%; height: 33.38%;"></a>
  <a href="#tools" style="top: 16.7%; left: 59.4%; width: 37%; height: 43.5%;"></a>
</div>
<figcaption class="caption">Click a widget in the image to learn more!</figcaption>



<iframe class="embedly-embed" src="//cdn.embedly.com/widgets/media.html?src=https%3A%2F%2Fwww.youtube.com%2Fembed%2Fvideoseries%3Flist%3DPLMhsMRlKjcNIYlDKDdKvPQuHqBjjS1ZGc&url=http%3A%2F%2Fwww.youtube.com%2Fwatch%3Fv%3DIcOyf28YJNk&image=https%3A%2F%2Fi.ytimg.com%2Fvi%2FIcOyf28YJNk%2Fhqdefault.jpg&key=f2aa6fc3595946d0afc3d76cbbd25dc3&type=text%2Fhtml&schema=youtube" width="854" height="480" scrolling="no" frameborder="0" allowfullscreen></iframe>



# Tools

Press the <span class="fb-button fb-gray">EDIT</span> button to add a tool.

![tools_widget.png](_images/tools_widget.png)

Press the Press the <span class="fb-button fb-green">+</span> button to add a tool, or the Press the <span class="fb-button fb-green">+ STOCK TOOLS</span> button to add all of the standard tools.


![empty_tools.png](_images/empty_tools.png)



![stock_tools.png](_images/stock_tools.png)

Press the <span class="fb-button fb-green">SAVE</span> button to save.

# Toolbay

![toolbay.png](_images/toolbay.png)

Press <span class="fb-button fb-gray">edit</span> to add your tools to the toolbay. Fill out the X, Y, and Z coordinates of the tool, select a tool that you added in the [tools](#tools) widget, and press the <span class="fb-button fb-green">+</span> button to add the tool to the toolbay.

__Tip__: Use the [Move](controls.md#move) widget on the controls page to determine the location of your tool in the toolbay. The coordinates should correspond to where the UTM is making contact while directly above the tool in the toolbay. You may use the jog buttons to reach the location, and enter the coordinates displayed in the Move widget into the toolbay widget.

You can click the <img class="nav-image" src="_images/current_location_button.png" alt="Use Current Location" width="5%" height="5%" /> button to fill the tool slot coordinate inputs with FarmBot's current coordinates.



{%
include callout.html
type="info"
title=""
content="Enter all of the tools you would like to use into the toolbay in the app. Support for multiple virtual toolbays is coming soon."
%}

__Tip__: Enter your seed bin location into a toolbay slot as well. The X and Y coordinates should follow the same pattern as the other tools. Determine the Z coordinate by mounting the seed injector tool you will be using to plant seeds and using the controls to move it carefully to a position that it will be able to pick up seeds from the bin.

Press <span class="fb-button fb-green">save</span> when done to save your tool locations.

# What's next?

 * [Sequences](sequences.md)
