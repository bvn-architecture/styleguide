# SketchUp 3D Printing

*How to 3D Print site models through SketchUp & Cura*

## Why?

To represent a site effectively to a client, or to provide models to the
City of Sydney archive as per requirement. Other methods that could be
appropriate (for representing models to clients) include creating a VR
experience, producing a poster, video or similar website. Here is a list of the major pros and cons of each method:


|Method|Pros|Cons|
|:---:|---|---|
|3D Printing|• Shows 3D space intuitively<br>• Potentially interactive<br>• Common representation technique|• Possibly difficult to produce<br>• Static representation<br>• Potentially expensive material|
|Poster|• Communicates intentions effectively<br>• Relatively easy production<br>• Easy delivery over internet|• Static Representation<br>• Non-3D Representation|
|Video|• Communicates intentions effectively<br>• Easy delivery over internet|• Non-interactive<br>• Professional standard difficult to achieve|
|VR Experience|• Interactive<br>• Scale-realistic<br>• High innovation potential|• Requires extensive technology to present<br>• Possibly difficult to produce|

## Methods:

*This is a practical process you can follow to achieve a file ready for 3D printing. For a more conceptual overview of some of the issues you will face, skip to the next section,* ['***Issues***'](#issues).

1. [**Installing.**](#installing) Follow this to install the extensions necessary to follow the rest of the processes

2. [**Cleaning.**](#cleaning) Follow this to clean your model. Cleaning your model throughout the process is recommended.

3. [**Slicing.**](#slicing) Follow this to slice your model up into manageable chunks for the 3D printer.

4. [**Exporting.**](#exporting) Follow this to export your model into a format acceptable to 3D printing software.

5. [**Setting.**](#setting) Follow this to learn how to set the 3D model up for printing in the 3D printing software.



### <a name="installing">**Installating**</a>:

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

    *Note: Although this guide will go through some of the
    functionalities of these extensions, if you ever get stuck or want to
    learn more about the extensions there are some excellent video and
    article tutorials on the above pages.*

3.  Open up SketchUp, select **Window &gt; Preferences**, then open the
    **Extensions** tab.

4.  Install the extensions above in the given order.

### <a name="cleaning">**Cleaning**</a>:

1.  Import the model into SketchUp. Don't scale the geometry down to size just yet - this will cause a lot of issues especially in the clean-up process.

    *Note: If you’re going to do any modelling in SketchUp, leave it all in “Layer0”. Layers don’t work the same in SketchUp as they do in other programs like Rhino, instead use groups for similar functionality.*

2.  Select **Window &gt; Preferences**, then change the precision to as high as possible.

    Note: You probably shouldn’t do this while actually working on your model making large changes, as this will slow down the software significantly.

3.  Group the model into manageable chunks. In order to group some elements, select them and then right click on them, selecting **Make Group**. If you make a mistake while grouping, you can ungroup by selecting the group and right clicking again, but selecting **Explode** instead.

    *Note: Grouping the model ensures that your computer doesn’t crash when it tries to clean up the entire model.*

4.  Select one of these groups and go to **Tools &gt; Solid Inspector**.

5.  There will likely be multiple items such as “Reversed Faces” and “Stray Edges” that will have a button next to them that says fix. Click these to deal with the relevant issues.

    ![Missing Image](/_includes/3dprinting/images/image_1.png)

6.  There may be some other items that say “Info” rather than fix. These represent issues that Solid Inspector can’t fix because there are multiple possible solutions. Clicking info will highlight the relevant issues – you’ll need to fix these yourself.

    *Note: A common issue that will say info is when there is an open surface that isn’t planar. To fix this, draw lines that split the surface into planar parts.*

    ![Missing Image](/_includes/3dprinting/images/image_2.png)

7.  If you’ve managed to fix everything, you should see a window like this when you open Solid Inspector!

    ![Missing Image](/_includes/3dprinting/images/image_3.png)

8.  After this, go to **Window &gt; CleanUp<sup>3</sup>** with one of the groups selected.

    ![Missing Image](/_includes/3dprinting/images/image_4.png)

9.  Make sure that either the **Local** or **Selection** radio button is selected, **Model** will ignore your group and try to clean everything.

10. If you have any hidden geometry that you would like to keep, either unhide it temporarily or uncheck the **Erase Hidden** checkbox.

11. If you exported from Revit, it is highly likely that you will want to keep the **Merge Adjacent Surfaces** checkbox ticked, as walls and ceilings do not automatically ‘connect’.

12. For the other buttons, leaving them as they were will most likely be fine. If you’d like to understand what any of them do, mousing over them will give you a description of how they should be used.

13. Click on the “**CleanUp**” button to start the process.

    *Note: Repeating this method to clean your model regularly throughout this process will reduce the amount of errors you have to deal with later on.*

### <a name="slicing">**Slicing**</a>:

1.  The maximum print size on the Ultimaker printers is 223mm wide by 223mm deep by 300mm high. If your model is larger than any of these dimensions, you’ll need to split it up.

    *Note: If it is only just larger than only one of these dimensions, you may be able to rotate it to fit it in. Here is the formula for working out whether your model will fit on the 3D printer:*

    *Formula:* (Width &lt;= 223 AND Depth &lt;= 223) OR (Width+Depth)/sqrt(2) &lt; 223)

2.  When splitting the model, the technique used goes through everything in that slice when not inside a group, and only whatever is inside the group when in a group. For example, the following can’t be cut in the order blue &gt; red &gt; green, because blue will cut all the way through the buildings. Rather, it should be cut with red first.

    ![Missing Image](/_includes/3dprinting/images/image_5.png)

3.  The following is trickier, as there are no full length cuts to base the other cuts off of. To deal with this, either red or green should be cut first, the other next, and then blue last off of the red cut. Whichever cut was made through the right piece can be patched together again using the CleanUp tool used earlier (Merge Adjacent Surfaces).

    ![Missing Image](/_includes/3dprinting/images/image_6.png)

4.  Just before cutting, you need to duplicate the item you want to cut.

5.  In order to actually start cutting, select **Tools &gt; Section Plane**

    ![Missing Image](/_includes/3dprinting/images/image_7.png)

6.  Now select a surface that has the angle you want to section from.

    *Note: If you want to create a section on an odd angle that none of your surfaces have, you’ll have to create a surface at that angle to base it off. You can then hold shift after hovering on this angle with the section tool and move it to a better location while retaining the angle.*

7.  Once the section has been placed in the right location, right click it and select **“Cut at Section”**. Patch the hole of the surface up that’s left by recreating one of the surrounding lines.

8.  Repeat steps 5-7 for the duplicate, except flipping the section by right clicking and selecting **“Reverse”**.

    ![Missing Image](/_includes/3dprinting/images/image_8.png)

9.  It’s possible to make some cuts that only go through a part of the model by grouping it appropriately, such as the red cut pictured below.

    ![Missing Image](/_includes/3dprinting/images/image_9.png)

10. After all the cuts have been made, it’s a good idea to clean it again (refer to the cleaning method above).

11. If any part of your model has any overhangs, it will needs to be sliced. 3D printers can generate support structures, however the finish of the underside after the support structures have been removed is not the best.

    ![Missing Image](/_includes/3dprinting/images/image_10.png)

    *Note: the 3d printers can handle an overhang that is under 30 degrees without needing to build supports.*

12.  To slice the overhangs, follow steps 4-8, using the bottom side of the overhang as the slicing surface (if it is 90 degrees. Otherwise, make a surface that is parallel to the ground at the correct spot and use that). As always, it’s best to clean after this (refer to the cleaning method above).
    
### <a name="exporting">**Exporting**</a>:

1.  To scale the models down, select everything you want to scale and press **S**. The model should be in a wireframe yellow box with green cubes around it.

    ![Missing Image](/_includes/3dprinting/images/image_11.png)

2.  Click on one of the corner green cubes. Then, type the scale you have calculated you want to achieve, with 1 being the original size. The scale appears in the bottom right hand corner of the screen. Press enter to set the scale.

3.  After everything has been resized, it’s a good idea to clean it once more (refer to the cleaning method above).

4.  The model should be ready for exporting. Make sure each separate piece is on the ground (although this can be fixed later in the Cura software).

5.  Copy each piece into its own separate SketchUp files.

6.  Select **File &gt; Export &gt; 3D Model**

    ![Missing Image](/_includes/3dprinting/images/image_12.png)

7.  Then after choosing your file name, set the “Export type:” to obj, and click “Export”.

    ![Missing Image](/_includes/3dprinting/images/image_13.png)

### <a name="setting">**Setting**</a>:

1.  To start the printing process, open **Cura**.

2.  Select **File &gt; Open File**, navigate to your file, and open it in Cura.

3.  From within Cura you can do the following things to your model after it’s been selected:

    ![Missing Image](/_includes/3dprinting/images/image_14.png)

4.  After fixing your model, ensure that:

    -   Print material is set to PLA

    -   Infill is set to Light

    -   Enable Support is unchecked

    *Note: If you are unsure about the other settings, setting them to
    this is recommended:*

    ![Missing Image](/_includes/3dprinting/images/image_15.png)


## <a name="issues">Issues</a>

### <a name="modelSplits">How to split up the model:</a>

*Do I need to split up the model?*

The main reason you'll want to split up the model is because your original model is too big. To calculate whether your model is too big, use the following formula:

(Width &lt;= 223 AND Depth &lt;= 223) OR
(Width+Depth)/sqrt(2) &lt; 223)

This formula takes into account the possible ability for you to rotate your model on the 3D printer to make it fit. If one of your dimensions is bigger than 223mm (the printers are 223mm wide by 223mm deep) and yet it fits, you will need to rotate it 45 degrees.

*Note: In order to ensure that your model fits, make a rectangular block of the size you're aiming for and put it into the cura software. Although the advertised dimensions of the 3D printing area is 223mm by 223mm, the software is likely to reject something close to this size.*

Another reason that you may want to split the model is to make a certain section hot-swappable. In this case, you should know already where you would like to split your model.

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

Another method that can be used is putting magnets inside the floor of the 3D print and inside each of the removable sections of the 3D print. This method and the reasoning you might use it can be [found here](#MagnetMethod)

![Missing Image](/_includes/3dprinting/images/MagnetWithinPrint.jpg)

These techniques should always be combined for even more secure results.

The last main thing that needs to be considered is what meaning is being conveyed by the different split sections - usually, there will be a main piece that should be centred and not split. Splitting the model into sections that are less likely or more likely overall to be remodelled and then reprinted reduces the amount of time wasted in the future while also reducing 3D print waste.

![Missing Image](/_includes/3dprinting/images/CityCutLinesZoning.jpg)

After the lines have been chosen, it's important to make sure that when the lines are cut they create a 0.5mm gap. If the models are cut without the gap, they won't fit together flush.


### Dealing with overhangs

There are three main ways to deal with overhangs, each with their own positives and negatives:

| Method | Overview | Positives | Negatives |
| --- | --- | --- | --- |
| Supports | Support structures can be generated that branch up from the ground at allowed angles to support structures that overhang. The 3D print is built on top of these structures that can be ripped away once finished. | Easy to generate and use | Bad undersurface finish, can be difficult to remove |
| Slicing | Slicing the model at overhang points, gluing the pieces together once the print has finished. | Allows for accurate modelling, no material waste | Only applies to 90 degree overhangs, manual process |
| Angling | Cura software technique that makes every overhang into an angle that can be printed | Easy to generate and use, deals with models that have many overhangs well | Model deformations, experimental technique |

Different situations call for different techniques to be used for an optimal result:

 - When printing a structure with steep overhangs that aren't 90 degrees, while also requiring high accuracy, using supports will ensure that the model isn't deformed, although the finish may not be the best. For example, a 3D printed tree's branches could possibly be printed using the angling technique, although deformations would be avoided using supports.

![Missing Image](/_includes/3dprinting/images/tree.png)

 - When printing a structure with many vertically parallel overhangs that require good quality surface finishes, angling is the appropriate technique. The angling is difficult to see unless pointed out, and allows for a professional quality finish especially on the surfaces below the overhangs when compared to support structures. For example, a print of an apartment block with many balconies would print well with this technique, as the balconies' surfaces would remain relatively well finished.

![Missing Image](/_includes/3dprinting/images/ApartmentBalcony.jpg)

 - When printing a large uninterrupted 90 degree overhang, slicing the model so that this surface can rest on the printing bed is the appropriate technique. For example, a print of a suspension bridge should be sliced so that excessive amounts of support underneath are avoided, and the surface remains smooth.
 
![Missing Image](/_includes/3dprinting/images/SuspensionBridge.png)

### Determining the scale

Different scales may need to be used for different prints. If you are providing a building for the City of Sydney's scale model, the exact specifications can be viewed [here](http://www.cityofsydney.nsw.gov.au/development/application-guide/application-process/model-requirements), which overall requires:

 - A scale of 1:500
 - 100 metres of site context if there are 10 or below stories
 - 200 metres of site context if there are more than 10 stories

However, if you aren't modelling for the City of Sydney and there aren't any other preset constrictions on what scale should be used, there are a few things that need to be considered:

 - **Model Size.**
    The larger the model, the greater the scale, but what is more important than the overall site size is the size of the centre piece. Given that you haven't chosen the size of the exterior pieces, scale the centre piece until it will fit inside the 223mm by 223mm printer, using that scale to [determine the splits of the model](#modelSplits). If you have already decided on the model splits, choose the largest piece and scale it so that it fits, using that scale for the rest of the model.
    
    *Note: Although you don't necessarily have to fill it up, bigger is usually more impressive and makes it easier to see details.*
 
 - **Model Detail.**
    As there is greater detail in the model, the scale should decrease so that the details can be produced by the 3D printer without apprearing really messy. This also means that it's easier to see the details in the model. Similarly, as there are less details in the model, the scale should increase. This ensures that the model seems less 'chunky' while also reducing the necessary size of the model without comprimising feature visibility.
    
 - **Model Accuracy & Finish.**
    When 3D printing, the height of each layer determines how well-finished (i.e. smooth) and accurate the final result is (with a smaller height resulting in a more accurate and smoother finish). However, as the layer height decreases and naturally the amount of layers required increases, the time needed to complete the job increases dramatically. To combat this, if you require a better finish, reducing the scale might be appropriate. You can do a large job with a smooth finish, but make sure you know how much time it will take.

![Missing Image](/_includes/3dprinting/images/3dPrintRes.png)

 - **Proximity to Standardisation.**
    If you've decided on the model's scale after taking into account the above factors, and you've realised it's going to be 1:493.4, downscaling to 1:500 won't affect the size greatly but will make the model a standard size which may become useful when comparing to other models. Having said this, be careful about upsizing the model (e.g. from 1:2004.3 to 1:2000) as it may not fit. Always check with a rectangular block in the cura software before proceeding.


### <a name="MagnetMethod"> Whether to use magnets & how </a>

Using magnets can make a site model presentation to a client look more professional, among many other reasons why you may want to use magnets. However, there are some factors that need to be considered before going ahead with this:
 
 - **3D Printer Model.** At the Sydney BVN office, there are 2 different types of 3D printers - the Ultimaker 2+ and the Ultimaker 3+. The 2+ has a metal head, so magnets can't be inserted into the prints by that printer. This means that if your model needs the slightly larger print range of the 2+ you won't be able to print to that size and use a magnet.
 
    Ultimaker 2+:
 ![Missing Image](/_includes/3dprinting/images/UM2_Volume.png)

    Ultimaker 3+:
 ![Missing Image](/_includes/3dprinting/images/UM3_Volume.png)


 - **Amount of movable pieces.** Embedding a magnet's main function is to make sure that a site model sits exactly where it needs to be placed every time it is put back after being removed. If there's only one piece being removed and it's enclosed (diagram 1), then magnets may not be necessary as there's no possibility for sliding - they might even make it more difficult to use than it needs to be given the difficulty of taking the piece out. However, if there are multiple pieces that can be moved (diagram 2), then a magnet can ensure the buildings are placed correctly.
 
 ![Missing Image](/_includes/3dprinting/images/Slidable1.png)

 ![Missing Image](/_includes/3dprinting/images/Slidable2.png)


 - **Reusability.** As mentioned above, embedding a magnet ensures that a piece sits where it needs to every time it is placed after being removed. If this isn't going to be a regular occurence, the magnets might be a superfluous addition making the printing process unnecessarily difficult.
 
 - **Laser cutter access.** In order to achieve the floor part of the design, a laser cutter is needed. This will most likely cost a decent amount of money if you need to outsource it (BVN currently does not have a laser cutter in the Sydney office).

***FIX THESE STEPS UP!!!!***

If you've considered the above issues and have decided to use a magnet, these are the steps that need to be followed:

1. Determine the dimensions of the magnet

2. Create an equivalent hole in the model

3. During the set up of the print, finding out the layer number that the print needs to be stopped at

4. Start the print

5. Insert the magnet, noting which side is facing down (north/south)

6. Unpause the print.


Your site model now has a magnet embedded inside it. In order for the magnets to connect to the right locations, the floor of the site model will need magnets also embedded inside of it. The best way to achieve this is using a laser cutter. After ensuring that the cutting locations line up exactly with the embedded magnets, you'll need to find a business to outsource the laser cutting to. [Kink](http://www.kinkfab.com/profile/) is a great company that has worked with BVN on this before, having cut the material, embedded the magnets, gluing them and the covering material on themselves (all within 48 hours, with the possibility of a 24 hour return service given an additional fee). Their only downside is they have quite high rates, so if budget is an issue and deadlines are flexible, some other companies may be more suitable. Given that the company you find only does the laser cutting, the rest of the process is detailed here:

1. Ensure that the cutting locations line up exactly with the embedded magnets (even a millimetre of difference is too much).

2. Most companies will accept (or require) an illustrator file, so export to this. [Here is a guide](https://static1.squarespace.com/static/548a3f6ee4b0c0f815c40ae1/t/5763a3b7ebbd1a9356dc6459/1466147783949/KINK+laser+cutting+details+17_6_16.pdf) on how kink recieves files; most companies will have a similar policy.

3. On deciding what material to use, this will depend on the thickness of the magnet and the aesthetics you want to achieve. White acrylic works well generally. Try and match the thickness of the material to the thickness of the magnet, preferably going over a little bit. Never have the magnet thicker than the material.

4. In order to achieve a smooth finish for easy sliding and a professional aesthetic, you'll need to cut another piece of material to place on top. This material does not need the magnet holes cut into it, but will need to be cut to the same size and shape as the site model. This material needs to be as thin as possible while still remaining opaque.

5. Once the material has been cut, glue the magnets in the holes. ***ASK WHAT GLUE TO USE***

    *Note: Secure the magnet(s) embedded inside the floor opposite in polarity to the magnet(s) inside the prints to ensure that the magnets attract, rather than repel!*

6. Once these have set, glue the surface material on top. ***ASK WHAT GLUE TO USE***

The floor and site model(s) are now finished. Test to see if it works!


## Extra Ideas

This article so far has dealt with (relatively) well polished ideas that have been tested multiple times beforehand. Here are some ideas that may suit your project that haven't been as thoroughly proven:

 - **Buildable model.** 
 
    In this method, the model's parts are printed seperately on the building level, so that the actual building can be taken apart. The reasons that you may want to do this include:

    - Being able to show the building's facade and its interior in the one model. This could also allow you to be able to show different levels of information at the same time.

    - The ability to replace certain parts of the building (e.g. the facade) without having to re-print the entire model, which takes less time and less material.

 - **Induction-lit model.**

    If magnets are going to be put into the design, it's possible to incorporate some induction lighting circuitry into the 3D print so that lights turn on when the model is placed on the magnet. You may want to use this because of a few reasons:

    - The ability of the model to show how the light it projects shines. This could be especially useful for projects where the building will be used a lot at night time (e.g. stadiums, bars).
    
    - Its capability to highlight certain regions of the design. This can be combined with RGB lights to highlight different sections of the design in different colours to represent data.
    
    A further possibility for this design could be to incorporate moving magnets on the underside (or magnets in different locations) that change the lighting configurations. Having said all this, incorporating circuitry inside a 3D print of a site model is quite difficult, especially if hidden, so attempt it knowing that it probably won't take as short as you planned and it likely won't work as well as you hope.


