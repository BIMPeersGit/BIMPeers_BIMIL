---
description: >-
  A cleanup tool that selectively removes unnecessary elements to keep your
  Revit model light and optimized
---

# Cleaning Service

{% hint style="info" %}
### **Requirements**

* Revit **2022–2026**
* BIMIL Manager **v 1.1.9.0+**\
  👉 How to check your BIMIL Manager version:  [Check here](../../get-started/check-and-update-bimil-manager-version.md)
{% endhint %}

## 📌 What is Cleaning Service?

Cleaning Service is a Revit Add-in that helps you **quickly clean unnecessary data** and keep your model lightweight and optimized.\
With features like **Triple Purge, auto backup, and Detailed Cleaning Preferences**, it reduces project size, improves performance, and ensures a clean model environment for collaboration.

<figure><img src="../../.gitbook/assets/Cleaning Service 2.png" alt=""><figcaption></figcaption></figure>

## ✅ Features

### 🔹 Basic Cleaning Service

* **Triple Purge (After Detail Cleaning):** Runs Purge Unused three times automatically to thoroughly remove residual unused data
* **Save Option**
  * Cleaning current model → Run cleaning directly in the current model
  * Cleaning and save as a new file → Save as a new file while cleaning
* **Backup before Cleaning:** Automatically creates a backup file in the designated path
* **Ignore non-critical warnings:** Skips minor warnings to prevent workflow interruptions

### 🔹 Detailed Cleaning Preferences

{% tabs %}
{% tab title="Basics+" %}
### Families&#x20;

* Optimize used families by purging unused types/materials  _<mark style="color:red;">(In development)</mark>_\
  →  This feature is currently under development and will be available in a future release.

### **Groups**

* **Delete unused groups** \
  →  Deletes group definitions that are not used anywhere in the model.
* **Ungroup all model groups**\
  →  Ungroups all model groups and converts them into individual elements to reduce dependencies.
* **Ungroup all detail groups** \
  →  Ungroups all detail groups and breaks them into standalone 2D elements.
* **Ungroup array-generated group** \
  →  Ungroups array-generated groups and turns them into independent items.

### **Design Options**

* **Delete non-primary design options** \
  →  Deletes all secondary options, keeping only the primary option in each set to simplify models.
{% endtab %}

{% tab title="Model" %}
### **Host-Detached Elements**

* **Delete orphaned tags**\
  →  Removes tags whose hosts no longer exist.
* **Delete "Orphaned" elements**\
  →  Deletes elements that show as “Orphaned” in Revit.
* **Delete “\<not associated>” elements**\
  →  Deletes elements that show as “\<not associated>” in Revit.

### **Room / Area / Space**

* **Delete unplaced rooms/areas/spaces** \
  →  Deletes definitions not placed in the model.
* **Delete enclosed rooms/areas/spaces** \
  →  Deletes enclosed items as configured for housekeeping scenarios.
* **Delete unused Room/Area/Space Separation Lines** \
  →  Deletes separation lines that bound no valid region.

### **Model Lines**

* **Delete Model Lines not associated with any element** \
  →  Deletes model lines not tied to geometry.
{% endtab %}

{% tab title="Views" %}
### **Views & Sheets**

* **Delete Views (not placed on sheets)** \
  →  Deletes standard views not assigned to any sheet (excluding Legends and Schedules).
* **Delete Legends (not placed on sheets)** \
  →  Deletes legends that are not assigned to any sheet.
*   **Delete Schedules (not placed on sheets)**&#x20;

    →  Deletes schedules that are not assigned to any sheet.
* **Delete empty Sheets (with no views)**\
  →  Deletes sheets that contain no views.

### **Details**

* **Delete Drafting views named ‘Drafting 1/2/3…’** \
  →  Deletes user-created drafting views that still use default names without being renamed.
* **Delete 3D views named ‘3D View 1/2/3…’** \
  →  Deletes user-created 3D views that still use default names without being renamed.

### **Others**

* **Delete unused view templates** \
  →  Deletes templates not applied to any view.
* **Delete unused view filters** \
  →  Deletes filters with zero usage.
* **Delete unused scope boxes**\
  →  Deletes scope boxes not referenced by views.
{% endtab %}

{% tab title="Links" %}
### **Revit Link**

* **Delete all Revit links** \
  →  Deletes all Revit link instances and types.
* **Delete unloaded/missing Revit Links** \
  →  Deletes broken or unloaded Revit links.

**CAD Link & Import**

* **Delete all CAD links** \
  →  Deletes all linked DWG/DXF files.
* **Delete unloaded/missing CAD Links** \
  →  Deletes broken or unloaded CAD links.
* **Delete all CAD Imports** \
  →  Deletes all imported CAD geometry from the model.

**Image Link & Import**

* **Delete all Image Imports** \
  →  Deletes all embedded or linked images.
*   **Delete unused Image Imports**&#x20;

    →  Deletes images not placed on any view/sheet.

**Point Clouds**

*   **Delete all Point Clouds**&#x20;

    →  Deletes all point cloud instances and types.
{% endtab %}
{% endtabs %}

## 💼 Ideal for

* BIM managers who want to improve **file size and performance** by removing unnecessary elements in large projects
* Designers who prefer **one-click optimization** over repetitive cleanup tasks
* Any Revit user who needs to maintain a **lightweight model environment** during collaboration

{% hint style="info" %}
### Cleaning Service is the **main installation package**.

By downloading this Add-in, you also get **Family Cleaner and Spatial Cleaner** included.
{% endhint %}
