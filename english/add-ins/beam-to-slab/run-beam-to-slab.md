# Run Beam to Slab

After selecting beams and slabs and configuring all settings, click the **OK** button to execute the _Beam to Slab_ operation.

<figure><img src="../../.gitbook/assets/image (32).png" alt=""><figcaption></figcaption></figure>

During processing, a progress window will appear, showing the current completion rate. As the process runs, you can observe each beam attaching to the slabs in real time in the active view.



## **Execution Process**

* **Detection**\
  For each beam, _Beam to Slab_ verifies the presence of any slab directly above the beam’s center point, within the range defined by the **Offset Limit** in _Detail Options_. Only slabs above the beam within this limit are considered; slabs below the beam are disregarded.
* **Attachment**
  * When a slab is detected within range, the beam attaches to the specified face of the slab (top or bottom).
  * For sloped slabs, _Beam to Slab_ adjusts the beam’s angle to align precisely with the slope.
* **Final Z-Offset Adjustment**
  * Upon completion, all beams are set with a Z offset of 0 for precise alignment. Note that during processing, beams may temporarily display a different Z offset, leading to a brief appearance of displacement until the final adjustment is applied.
