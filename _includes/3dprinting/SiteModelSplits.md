# Splitting Site Models

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
