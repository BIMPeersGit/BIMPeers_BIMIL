---
description: Easily modify slab areas and create slab steps with customizable settings.
---

# Push / Pull Slab

**Push/Pull Slab** allows users to create sunken or raised floor areas by adjusting slab regions using model lines. This Revit add-in enables users to draw the desired area with model lines in a closed loop, select the slab and model lines, and define height, offset, and slab step type to achieve the desired modifications.

## **Features**

* **Height Adjustment:**\
  Set how much to raise or lower the slab area with positive or negative values.
* **Offset:**\
  Define the boundary extension for the new slab area beyond the model lines.
* **Slab Step Options:**
  * **Wall:** Creates a boundary wall with the specified offset thickness. The wall material is taken from the thickest material used in the slab.
  * **Wall + Slab Edge:** Requires specifying a Slab Edge Angle. This option generates a sloped edge outside the wall using the defined angle and the same material as the wall.
  * **None:** No additional steps or walls are created.

## **Notes**

* Model lines must form closed loops.
* Errors may occur if the corners of the closed model line touch the slab boundary.
* Ellipse and spline model lines are not supported.
* Slab steps will not be created in directions where the model line extends beyond the slab boundary.

{% embed url="https://www.youtube.com/watch?t=4s&v=JVF6c2pJgDM" %}
