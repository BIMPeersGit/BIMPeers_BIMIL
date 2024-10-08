---
description: Automate geometry joining across categories based on user-defined priorities.
---

# Auto Join

**Auto Join** streamlines the process of managing geometries within Autodesk Revit by enabling users to join or unjoin geometries across different categories according to customized priorities. This tool simplifies complex modeling workflows, making it easier to maintain consistency and integrity in your Revit models.

## Features

* **Category Selection**: \
  Choose specific categories as targets for the joining process.
* **Priority Setting:** \
  Drag and arrange categories to establish which ones have precedence in the joining hierarchy.
* **Scope Setting:** \
  Define the scope of Auto Join to include all project objects, only objects visible in the current view, or selected objects.
* **Execute Auto Join:** \
  Performs Join Geometry operations between categories based on the rules set by the user.
* **Execute Unjoin:** \
  Carries out Unjoin Geometry operations between currently selected categories.
* **Save Settings:** \
  Export and import Auto Join configurations, facilitating reuse and sharing of settings across projects.

## Notes

* Certain category pairs are excluded from joining, such as Structural Wall – Wall and Structural Column – Column.
* Objects already joined will be reevaluated and potentially rejoined if they do not meet the established priority criteria.
* It is recommended not to edit the model in Revit while Auto Join or Unjoin operations are in progress to prevent conflicts.

{% embed url="https://www.youtube.com/watch?v=AcSQ5MnXtFg" %}
