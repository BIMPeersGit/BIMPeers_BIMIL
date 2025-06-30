---
description: >-
  Quickly and accurately identifies where a selected element is located in a
  Revit model.
---

# Finder

### 📌 **What is Finder?**

Finder Add-in helps you quickly identify **where any selected element is located in your Revit model.**\
With a single click, it automatically analyzes spatial information without the need for manual checking or complicated workflows.

<figure><img src="../../.gitbook/assets/Mail IMG2 (1).png" alt=""><figcaption><p>Displays an element’s <strong>Grid, Level, Room, Space, Zone, and Area</strong> with a single click.</p></figcaption></figure>

### ✅ Features

✔️ **Grid** – Returns the name of the **grid line closest to the element’s center point**. Supports vertical, horizontal, and diagonal grids.

✔️ **Level** – Returns the name of the **level that the element belongs to**, based on its elevation.

✔️ **Room** – Provides information about the **architectural room that contains the element**, including room name and number.

✔️ **Space -** Returns the **MEP space** the element is located in. This is typically used in mechanical, electrical, and plumbing design.

✔️ **Zone -** Returns the **logical MEP zone** that groups multiple spaces for system-level organization (e.g., HVAC zones).

✔️ **Area** – Returns the **name or number of the area** that contains the element.

***

### 💡 Useful Tips

Exporting location data to reports

* copy and paste the location information easily.

#### &#x20;Use for QA/QC Checklists

* Quickly check **“Which space should this element belong to?”**
* Identify elements **missing Room or Area assignment** to catch modeling errors.

#### &#x20;Empty Space Detection

* If an element is **not in any Room, Space, or Area**,\
  → it may indicate a **missing spatial assignment or boundary issue**.

***

### ⚠️ Notes

* Finder only supports selecting **a single element at a time**!&#x20;
* **Elements from Linked Models are not supported.** Only elements in the active project file are analyzed.
* **Some elements may return inaccurate location results**, especially if they lack geometric placement or host references.

{% hint style="warning" %}
Due to the complexity of Revit models, **Finder Add-in may not always return perfectly accurate location data for every element.**\
This tool is continuously evolving, and **your feedback plays a key role in making it better.**\
If you encounter any issues or have suggestions, please don’t hesitate to share them with us.
{% endhint %}

( Youtube 영상 기입 예정 )&#x20;
