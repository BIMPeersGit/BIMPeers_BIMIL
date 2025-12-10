---
description: Streamline your structural design workflow with Structure Booster.
---

# Structure Booster

{% hint style="info" %}
This is a third-party add-in developed and provided by SCK.\
Your consent to third-party data provision is required to use this add-in.
{% endhint %}

Structure Booster enhances structural design workflows in Autodesk Revit by enabling seamless conversion of analysis models to Revit models and automated creation of structural schedules from Excel files. This tool simplifies the process of importing structural data and generating comprehensive schedules for various structural elements, helping maintain consistency and efficiency throughout your structural modeling projects.

## Features

* **Import MGT**: Converts analysis model (MGT) files into Revit models, bridging the gap between structural analysis and BIM modeling.

<figure><img src="../../.gitbook/assets/StructureBooster 1.png" alt=""><figcaption></figcaption></figure>

* **Schedule Master**: Automatically creates structural schedules from Excel files for the following elements:
  * Beam
  * Column
  * Slab
  * Footing (Isolated)
  * Footing (Pile)
  * Wall

<figure><img src="../../.gitbook/assets/StructureBooster 2.png" alt=""><figcaption></figcaption></figure>

## Notes

* Excel files exported from Design+ versions prior to Design+ 2024 v1.1 may cause format conflicts in column and shear wall schedules. Please use the provided sample files or export from Design+ 2024 v1.1 or later.
* Only beam members with Section Type SB, SR or EBC are supported. Members are automatically classified as columns or beams based on their angle orientation.
