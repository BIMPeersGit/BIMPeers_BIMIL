---
description: >-
  Quickly and accurately identifies where a selected element is located in a
  Revit model.
---

# Finder

## 📌 **What is Finder?**

Finder Add-in helps you quickly identify **where any selected element is located in your Revit model.**\
With a single click, it automatically analyzes spatial information without the need for manual checking or complicated workflows.

<figure><img src="../../.gitbook/assets/Mail IMG2 (1).png" alt=""><figcaption><p>Displays an element’s <strong>Grid, Level, Room, Space, Zone, and Area</strong> with a single click.</p></figcaption></figure>

## ✅ Features

✔️ **Grid** – Shows the grid lines based on the element’s overall geometry. Supports vertical, horizontal, and diagonal grids.

✔️ **Level** – Shows the name of the level the element belongs to, based on its elevation.

✔️ **Room** – Shows information about the architectural room containing the element, including the room name and number.

✔️ **Space -** Shows the MEP space where the element is located. Typically used in mechanical, electrical, and plumbing design.

✔️ **Zone -** Shows the logical MEP zone that groups multiple spaces for system-level organization (e.g., HVAC zones).

✔️ **Area** – Shows the name or number of the area containing the element.

***

## 💡 Useful Tips

Exporting location data to reports

* copy and paste the location information easily.

#### &#x20;Use for QA/QC Checklists

* Quickly check **“Which space should this element belong to?”**
* Identify elements **missing Room or Area assignment** to catch modeling errors.

#### &#x20;Empty Space Detection

* If an element is **not in any Room, Space, or Area**,\
  → it may indicate a **missing spatial assignment or boundary issue**.

***

## ⚠️ Notes

* Finder only supports selecting **a single element at a time**!&#x20;
* **Elements from Linked Models are not supported.** Only elements in the active project file are analyzed.
* **Some elements may return inaccurate location results**, especially if they lack geometric placement or host references.

{% hint style="warning" %}
Due to the complexity of Revit models, **Finder Add-in may not always return perfectly accurate location data for every element.**\
This tool is continuously evolving, and **your feedback plays a key role in making it better.**\
If you encounter any issues or have suggestions, please don’t hesitate to share them with us.
{% endhint %}

{% embed url="https://youtu.be/NCTOEuIcvAc" %}
