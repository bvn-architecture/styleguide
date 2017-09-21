# SketchUp 3D Printing

*How to 3D Print site models through SketchUp & Cura*

## Why?

To represent a site effectively to a client, or to provide models to the
City of Sydney archive as per requirement. Other methods that could be
appropriate (for representing models to clients) include creating a VR
experience, producing a poster, video or similar website.

## Methods:

*This is a practical process you can follow to achieve a file ready for 3D printing. For a more conceptual overview of some of the issues you will face, skip to the next section '**Issues***'.

1. **Installing.** Follow this to install the extensions necessary to follow the rest of the processes

2. **Cleaning.** Follow this to clean your model. Cleaning your model throughout the process is recommended.

3. **Slicing.** Follow this to slice your model up into manageable chunks for the 3D printer.

4. **Exporting.** Follow this to export your model into a format acceptable to 3D printing software.

5. **Setting.** Follow this to learn how to set the 3D model up for printing in the 3D printing software.



### **Installating**:

1.  Install SketchUp 2017:

    <https://www.sketchup.com/download>

2.  There are four extensions we need to download:

-   TT\_Lib<sup>2</sup>

    <https://extensions.sketchup.com/en/content/tt_lib%C2%B2>

-   CleanUp<sup>3</sup>

    <https://extensions.sketchup.com/en/content/cleanup%C2%B3>

-   Solid Inspector<sup>2</sup>

    <https://extensions.sketchup.com/en/content/solid-inspector%C2%B2>

-   Zorro2

    <https://extensions.sketchup.com/en/content/zorro2>

> *Note:* Although this guide will go through some of the
> functionalities of these extensions, if you ever get stuck or want to
> learn more about the extensions there are some excellent video and
> article tutorials on the above pages.

3.  Open up SketchUp, select **Window &gt; Preferences**, then open the
    **Extensions** tab.

4.  Install the extensions above in the given order.

### **Cleaning**:

1.  Import the model into SketchUp.

    Note: If you’re going to do any modelling in SketchUp, leave it all
    in “Layer0”. Layers don’t work the same in SketchUp as they do in
    other programs like Rhino, instead use groups for
    similar functionality.

    Note: DO NOT scale the geometry down to size just yet. This will
    cause a lot of issues especially in the clean-up process.

2.  Select **Window &gt; Preferences**, then change the precision to as
    high as possible.

    Note: You probably shouldn’t do this while actually working on your
    model making large changes, as this will slow down the
    software significantly.

3.  Group the model into manageable chunks. In order to group some
    elements, select them and then right click on them, selecting **Make
    Group**. If you make a mistake while grouping, you can ungroup by
    selecting the group and right clicking again, but selecting
    **Explode** instead.

    Note: Grouping the model ensures that your computer doesn’t crash
    when it tries to clean up the entire model.

4.  Select one of these groups and go to **Tools &gt; Solid Inspector**.

5.  There will likely be multiple items such as “Reversed Faces” and
    “Stray Edges” that will have a button next to them that says fix.
    Click these to deal with the relevant issues.

> ![Missing Image](/images/image_1.png)

6.  There may be some other items that say “Info” rather than fix. These
    represent issues that Solid Inspector can’t fix because there are
    multiple possible solutions. Clicking info will highlight the
    relevant issues – you’ll need to fix these yourself.

    Note: A common issue that will say info is when there is an open
    surface that isn’t planar. To fix this, draw lines that split the
    surface into planar parts.

![Missing Image](/images/image_2.png)

7.  If you’ve managed to fix everything, you should see a window like
    this when you open Solid Inspector!

![Missing Image](/images/image_3.png)

8.  After this, go to **Window &gt; CleanUp<sup>3</sup>** with one of
    the groups selected.

![Missing Image](/images/image_4.png)

9.  Make sure that either the **Local** or **Selection** radio button is
    selected, **Model** will ignore your group and try to
    clean everything.

10.  If you have any hidden geometry that you would like to keep, either
    unhide it temporarily or uncheck the **Erase Hidden** checkbox.

11.  If you exported from Revit, it is highly likely that you will want
    to keep the **Merge Adjacent Surfaces** checkbox ticked, as walls
    and ceilings do not automatically ‘connect’.

12.  For the other buttons, leaving them as they were will most likely
    be fine. If you’d like to understand what any of them do, mousing
    over them will give you a description of how they should be used.

13.  Click on the “**CleanUp**” button to start the process.

    Note: Repeating this method to clean your model regularly throughout
    this process will reduce the amount of errors you have to deal with
    later on.

### **Slicing**:

1.  The maximum print size on the Ultimaker printers is 223mm wide by
    223mm deep by 300mm high. If your model is larger than any of these
    dimensions, you’ll need to split it up.

    Note: If it is only just larger than only one of these dimensions,
    you may be able to rotate it to fit it in. Here is the formula for
    working out whether your model will fit on the 3D printer:

*Formula:* (Width &lt;= 223 AND Depth &lt;= 223) OR
(Width+Depth)/sqrt(2) &lt; 223)

2.  When splitting the model, the technique used goes through everything
    in that slice when not inside a group, and only whatever is inside
    the group when in a group. For example, the following can’t be cut
    in the order blue &gt; red &gt; green, because blue will cut all the
    way through the buildings. Rather, it should be cut with red
    first. ![Missing Image](/images/image_5.png)

3.  The following is trickier, as there are no full length cuts to base
    the other cuts off of. To deal with this, either red or green should
    be cut first, the other next, and then blue last off of the red cut.
    Whichever cut was made through the right piece can be patched
    together again using the CleanUp tool used earlier (Merge
    Adjacent Surfaces).

> ![Missing Image](/images/image_6.png)

4.  Just before cutting, you need to duplicate the item you want to cut.

5.  In order to actually start cutting, select **Tools &gt; Section
    Plane**

![Missing Image](/images/image_7.png)

6.  Now select a surface that has the angle you want to section from.

    Note: If you want to create a section on an odd angle that none of
    your surfaces have, you’ll have to create a surface at that angle to
    base it off. You can then hold shift after hovering on this angle
    with the section tool and move it to a better location while
    retaining the angle.

7.  Once the section has been placed in the right location, right click
    it and select **“Cut at Section”**. Patch the hole of the surface up
    that’s left by recreating one of the surrounding lines.

8.  Repeat steps 5-7 for the duplicate, except flipping the section by
    right clicking and selecting **“Reverse”**.

![Missing Image](/images/image_8.png)

9.  It’s possible to make some cuts that only go through a part of the
    model by grouping it appropriately, such as the red cut
    pictured below.

    ![Missing Image](/images/image_9.png)

10.  After all the cuts have been made, it’s a good idea to clean
    it again (refer to the cleaning method above).

11.  If any part of your model has any overhangs, it will needs to
    be sliced. 3D printers can generate support structures, however the
    finish of the underside after the support structures have been
    removed is not the best.

![Missing Image](/images/image_10.png)

Note: the 3d printers can handle an overhang that is under 30 degrees
without needing to build supports.

12.  To slice the overhangs, follow steps 4-8, using the bottom side of
    the overhang as the slicing surface (if it is 90 degrees. Otherwise,
    make a surface that is parallel to the ground at the correct spot
    and use that). As always, it’s best to clean after this (refer to
    the cleaning method above).
    
### **Exporting**:

1.  To scale the models down, select everything you want to scale and
    press **S**. The model should be in a wireframe yellow box with
    green cubes around it.

![Missing Image](/images/image_11.png)

2.  Click on one of the corner green cubes. Then, type the scale you
    have calculated you want to achieve, with 1 being the original size.
    The scale appears in the bottom right hand corner of the screen.
    Press enter to set the scale.

3.  After everything has been resized, it’s a good idea to clean it
    once more (refer to the cleaning method above).

4.  The model should be ready for exporting. Make sure each separate
    piece is on the ground (although this can be fixed later in the
    Cura software).

5.  Copy each piece into its own separate SketchUp files.

6.  Select **File &gt; Export &gt; 3D Model**

![Missing Image](/images/image_12.png)

7.  Then after choosing your file name, set the “Export type:” to obj,
    and click “Export”.

![Missing Image](/images/image_13.png)

### **Setting**:

1.  To start the printing process, open **Cura**.

2.  Select **File &gt; Open File**, navigate to your file, and open it
    in Cura.

3.  From within Cura you can do the following things to your model after
    it’s been selected:

![Missing Image](/images/image_14.png)

4.  After fixing your model, ensure that:

<!-- -->

>  *Print material is set to PLA*

>  *Infill is set to Light*

>  *Enable Support is unchecked*

    Note: If you are unsure about the other settings, setting them to
    this is recommended:

![Missing Image](/images/image_15.png)


## Issues

### How to split up the model:

*Do I need to split up the model?*

The main reason you'll want to split up the model is because your original model is too big. To calculate whether your model is too big, use the following formula:

*Formula:* (Width &lt;= 223 AND Depth &lt;= 223) OR
(Width+Depth)/sqrt(2) &lt; 223)

Another reason that you may want to split the model is to make a certain section hot-swappable. In this case, you should know already where you would like to split your model. ***POSSIBLE CONTINUATION HERE (DIFFERENT BRANCH)***

*I need to split up my model because it's too big. Where do I cut?*

It depends on a few factors individual to each model:

1.  Buildings/structures present
2.  Terrain present
3.  Purpose of the model

And some static factors too:

1.  Size of the 3D printer
2.  Lockability (Ensuring the pieces can't slide)

It's likely that you'd rather not cut through any buildings present.

![Missing Image](CityCutLinesGrid.jpg)

![Missing Image](CityCutLinesRoads.jpg)

![Missing Image](CityCutLinesJagged.jpg)

![Missing Image](CityCutLinesZoning.jpg)




2.  Model
















