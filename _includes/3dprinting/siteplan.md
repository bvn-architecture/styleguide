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

    *Note:* Although this guide will go through some of the
    functionalities of these extensions, if you ever get stuck or want to
    learn more about the extensions there are some excellent video and
    article tutorials on the above pages.

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

> ![Missing Image](/_includes/3dprinting/images/image_1.png)

6.  There may be some other items that say “Info” rather than fix. These
    represent issues that Solid Inspector can’t fix because there are
    multiple possible solutions. Clicking info will highlight the
    relevant issues – you’ll need to fix these yourself.

    Note: A common issue that will say info is when there is an open
    surface that isn’t planar. To fix this, draw lines that split the
    surface into planar parts.

![Missing Image](/_includes/3dprinting/images/image_2.png)

7.  If you’ve managed to fix everything, you should see a window like
    this when you open Solid Inspector!

![Missing Image](/_includes/3dprinting/images/image_3.png)

8.  After this, go to **Window &gt; CleanUp<sup>3</sup>** with one of
    the groups selected.

![Missing Image](/_includes/3dprinting/images/image_4.png)

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
    first. ![Missing Image](/_includes/3dprinting/images/image_5.png)

3.  The following is trickier, as there are no full length cuts to base
    the other cuts off of. To deal with this, either red or green should
    be cut first, the other next, and then blue last off of the red cut.
    Whichever cut was made through the right piece can be patched
    together again using the CleanUp tool used earlier (Merge
    Adjacent Surfaces).

> ![Missing Image](/_includes/3dprinting/images/image_6.png)

4.  Just before cutting, you need to duplicate the item you want to cut.

5.  In order to actually start cutting, select **Tools &gt; Section
    Plane**

![Missing Image](/_includes/3dprinting/images/image_7.png)

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

![Missing Image](/_includes/3dprinting/images/image_8.png)

9.  It’s possible to make some cuts that only go through a part of the
    model by grouping it appropriately, such as the red cut
    pictured below.

    ![Missing Image](/_includes/3dprinting/images/image_9.png)

10.  After all the cuts have been made, it’s a good idea to clean
    it again (refer to the cleaning method above).

11.  If any part of your model has any overhangs, it will needs to
    be sliced. 3D printers can generate support structures, however the
    finish of the underside after the support structures have been
    removed is not the best.

![Missing Image](/_includes/3dprinting/images/image_10.png)

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

![Missing Image](/_includes/3dprinting/images/image_11.png)

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

![Missing Image](/_includes/3dprinting/images/image_12.png)

7.  Then after choosing your file name, set the “Export type:” to obj,
    and click “Export”.

![Missing Image](/_includes/3dprinting/images/image_13.png)

### **Setting**:

1.  To start the printing process, open **Cura**.

2.  Select **File &gt; Open File**, navigate to your file, and open it
    in Cura.

3.  From within Cura you can do the following things to your model after
    it’s been selected:

![Missing Image](/_includes/3dprinting/images/image_14.png)

4.  After fixing your model, ensure that:

    *Print material is set to PLA*

    *Infill is set to Light*

    *Enable Support is unchecked*

    Note: If you are unsure about the other settings, setting them to
    this is recommended:

![Missing Image](/_includes/3dprinting/images/image_15.png)


## Issues

### <a name="modelSplits">How to split up the model:</a>

*Do I need to split up the model?*

The main reason you'll want to split up the model is because your original model is too big. To calculate whether your model is too big, use the following formula:

(Width &lt;= 223 AND Depth &lt;= 223) OR
(Width+Depth)/sqrt(2) &lt; 223)

This formula takes into account the possible ability for you to rotate your model on the 3D printer to make it fit. If one of your dimensions is bigger than 223mm (the printers are 223mm wide by 223mm deep) and yet it fits, you will need to rotate it 45 degrees.

*Note: In order to ensure that your model fits, make a rectangular block of the size you're aiming for and put it into the cura software. Although the advertised dimensions of the 3D printing area is 223mm by 223mm, the software is likely to reject something close to this size.

Another reason that you may want to split the model is to make a certain section hot-swappable. In this case, you should know already where you would like to split your model. ***POSSIBLE CONTINUATION HERE (DIFFERENT BRANCH)***

*I need to split up my model because it's too big. Where do I cut?*

It depends on a few factors individual to each model:

1.  Buildings/structures present
2.  Terrain present
3.  Purpose of the model

And some static factors too:

1.  Size of the 3D printer
2.  Lockability (Ensuring the pieces can't slide)

The first thing that needs to be considered in the slicing process is the size - you need to maximise the size while still remaining within the dimensions of the 3D printer. The following image shows how you might do that:

![Missing Image](/_includes/3dprinting/images/CityCutLinesGrid.jpg)

Having said that, it's likely that you'd rather not cut through any buildings present. Instead, following roads (or similar, e.g. rivers, paths, etc.) can be a logical way to split the buildings while minimising the impact on the design:

![Missing Image](/_includes/3dprinting/images/CityCutLinesRoads.jpg)

The method pictured above is better, but if the design was cut this way the pieces would be free to slide easily between their respective locations. When this happens, the model can be frustrating to use as pieces constantly push each other out of the way (especially when there are multiple pieces that are supposed to move - if not, the pieces can always be glued down). One method that solves this is creating indented edges that lock in pieces more effectively, or L-shaped (among other non-rectangularly shaped) pieces that are less likely to slide around:

![Missing Image](/_includes/3dprinting/images/CityCutLinesJagged.jpg)

Another method that can be used is putting magnets inside the floor of the 3D print and inside each of the removable sections of the 3D print. This method can also be used to create parts that light up when places on the magnet using magnetic induction lights. These techniques are difficult to achieve (assistance would be required. ***ASK ABOUT HOW THIS IS ACHIEVED***

![Missing Image](/_includes/3dprinting/images/MagnetWithinPrint.jpg)

These techniques can always be combined for even more secure results.

The last main thing that needs to be considered is what meaning is being conveyed by the different split sections - usually, there will be a main piece that should be centred and not split. Splitting the model into sections that are less likely or more likely overall to be remodelled and then reprinted reduces the amount of time wasted in the future while also reducing 3D print waste.

![Missing Image](/_includes/3dprinting/images/CityCutLinesZoning.jpg)

After the lines have been chosen, it's important to make sure that when the lines are cut they create a 0.5mm gap. If the models are cut without the gap, they won't fit together flush.

### Dealing with overhangs

slice vs cura tool

Overhangs are difficult to deal with 


### Determining the scale

Different scales may need to be used for different prints. If you are providing a building for the City of Sydney's scale model, the exact specifications can be viewed [here](http://www.cityofsydney.nsw.gov.au/development/application-guide/application-process/model-requirements), which overall requires:

 - A scale of 1:500
 - 100 metres of site context if there are 10 or below stories
 - 200 metres of site context if there are more than 10 stories

However, if you aren't modelling for the City of Sydney and there aren't any other preset constrictions on what scale should be used, there are a few things that need to be considered:

 - **Model Size**
    The larger the model, the greater the scale, but what is more important than the overall site size is the size of the centre piece. Given that you haven't chosen the size of the exterior pieces, scale the centre piece until it will fit inside the 223mm by 223mm printer, using that scale to [determine the splits of the model](#modelSplits). If you have already decided on the model splits, choose the largest piece and scale it so that it fits, using that scale for the rest of the model.
    
    *Note: Although you don't necessarily have to fill it up, bigger is usually more impressive and makes it easier to see details.
 
 - **Model Detail**
    As there is greater detail in the model, the scale should decrease so that the details can be produced by the 3D printer without apprearing really messy. This also means that it's easier to see the details in the model. Similarly, as there are less details in the model, the scale should increase. This ensures that the model seems less 'chunky' while also reducing the necessary size of the model without comprimising feature visibility.
    
 - **Model Purpose**
    sdgsdghsfhdFHDFHdfshf

### Whether to use magnets & how

 - Re-usability of model
 
 - 



**Q**

1. Current doc

2. Hot-swappable. When/How?

3. Magnets in 3D prints & floor. Possible inductive lighting?

4. 3D Printing settings










