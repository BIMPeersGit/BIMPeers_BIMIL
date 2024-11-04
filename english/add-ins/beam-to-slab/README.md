---
description: Automatically attach beams to the nearest upper floor.
---

# Beam to Slab

<figure><img src="../../.gitbook/assets/image (27).png" alt="" width="280"><figcaption></figcaption></figure>

**Beam to Slab** simplifies structural projects by automatically detecting and attaching beams to the nearest upper floor. It enhances alignment between beams and floors, boosting workflow efficiency and reducing the need for manual adjustments. This add-in accurately identifies floors directly above beams, facilitating precise and seamless attachment with minimal user input.

## Features

* **Upper Floor Recognition:** \
  Automatically identifies and attaches beams to the closest floor above in the Z-axis direction. The 'Offset Limit' allows users to set a specific detection range.
* **Reference Plane Setting:** \
  Choose to attach beams to either the top or bottom surface of the floor.
* **Orientation Options:**
  * Normal: Aligns beams perpendicular to sloped floors modified with Slope Arrow. Does not support curved floors.
  * Horizontal: Keeps beams horizontal regardless of the floor's slope.

## Notes

* Movement of curved beams is not supported.
* Detects the nearest floor based on the beam's central point.
* Recognizes only floors that overlap with or are above the beam.
* For curved floors, only the 'Horizontal' orientation is supported.
* Beams attach to floors based on the central point of the beam's top surface.

{% embed url="https://www.youtube.com/watch?v=TQXyse9eqZA" %}
