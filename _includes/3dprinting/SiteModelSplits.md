# How to split your site model and why you should

![Missing Image](/_includes/3dprinting/images/modelSlotPiece.jpg)

To plan out cities, a lot of inner-city councils these days require 3D-printed site models before allowing a building to be built. At the required scale, they're often too big to fit in most 3D-printers. Until the day that most 3D printers can print large models, we'll have model splitting.

The question is: "Where do I cut?"

It depends on a few things individual to each model:

1.  Size of the 3D printer
2.  Buildings/structures present
3.  Terrain present
4.  Purpose of the model
5.  Lockability (Ensuring the pieces can't slide)

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
