---
description: Automate geometry joining across categories based on user-defined priorities.
---

# Auto Join

**Auto Join** streamlines the process of managing geometries within Autodesk Revit by enabling users to join or unjoin geometries across different categories according to customized priorities. This tool simplifies complex modeling workflows, making it easier to maintain consistency and integrity in your Revit models.

## **Apply to** (Scope Setting)

Define the scope of Auto Join to include.

<figure><img src="../.gitbook/assets/image (17).png" alt=""><figcaption></figcaption></figure>

* **All**: Try joining every elements in the model.
* **Visible in View**: Try joining for elements which can view in the active view.
* **Selected Elements**: Try joining for selected elements.

## Category Selection

Click the checkbox to select a specific category as the geometry joining target.

### Supported Categories

#### **Non Structural Categories**

* Ceiling
* Column
* Floor
* Generic Model
* Roof
* Wall

#### **Structural Categories**

* Structural Column
* Structural Floor
* Structural Foundation
* Structural Framing
* Structural Wall

{% hint style="info" %}
For Walls & Floors, the structural or non-structural classification is determined by whether the 'Structural' parameter is checked.
{% endhint %}

<figure><img src="../.gitbook/assets/image (25).png" alt=""><figcaption></figcaption></figure>

## **Priority Setting:**&#x20;

<figure><img src="../.gitbook/assets/image (21).png" alt=""><figcaption></figcaption></figure>

Drag and arrange categories to establish which ones have precedence in the joining hierarchy.

## Auto Join

Performs Join Geometry operations between categories.

Elements with a higher join hierarchy are not overridden by lower ones.

<figure><img src="../.gitbook/assets/image (24).png" alt=""><figcaption><p>Priority : Column > Structural Frame > Floor</p></figcaption></figure>

{% hint style="info" %}
Objects already joined will be reevaluated and potentially rejoined if they do not meet the established priority criteria.
{% endhint %}

## Unjoin

Performs Unoin Geometry operations between categories.



## **Import / Export Settings:**&#x20;

Export and import Auto Join configurations, facilitating reuse and sharing of settings across projects.



## Detailed Options

<figure><img src="../.gitbook/assets/image (20).png" alt="" width="375"><figcaption></figcaption></figure>

Click the arrow button to show detailed options.

### Allow same category join

<figure><img src="../.gitbook/assets/image (23).png" alt="" width="375"><figcaption></figcaption></figure>

Check for join beween same category elements.



### Allow structural-non structural join

Check for join beween structural element and non structural element.

To prevent joining structural and non-structural elements, leave the checkbox unchecked.

## Notes

* Objects already joined will be reevaluated and potentially rejoined if they do not meet the established priority criteria.
* It is recommended not to edit the model in Revit while Auto Join or Unjoin operations are in progress to prevent conflicts.

{% embed url="https://www.youtube.com/watch?v=AcSQ5MnXtFg" %}
