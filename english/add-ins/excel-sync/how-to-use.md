# How to Use

### 1️⃣ Start Excel Sync

\- Open the BIMIL tab in Revit and click \[Excel Sync].

<figure><img src="../../.gitbook/assets/Click Excel Sync.gif" alt="" width="563"><figcaption></figcaption></figure>

### 2️⃣ Choose one of the three tabs at the top to define your target category:

\- In the main window, choose what kind of data you want to work with. There are three tabs available:\
&#x20;  • Model – for physical model elements\
&#x20;  • Annotation – for tags, dimensions, and text\
&#x20;  • Analytical Model – for structural analysis elements

Select the desired tab and check the categories or individual elements you want to edit.

<figure><img src="../../.gitbook/assets/Model, Annotation, Analytical Model.gif" alt="" width="563"><figcaption></figcaption></figure>

### 3️⃣ Select Target Elements:&#x20;

Choose how to gather elements:

* &#x20;All : All elements in the model
* &#x20;Active View: Only elements visible in the current view
* &#x20;Selected Elements: Only elements you’ve pre-selected in the model

{% hint style="info" %}
Note: \
The “Include Link Models” checkbox is currently disabled. \
This feature will be available in a future update!
{% endhint %}

<figure><img src="../../.gitbook/assets/All, Active View, Selected Element.gif" alt="" width="563"><figcaption></figcaption></figure>

### 4️⃣ Select Parameters

Choose which parameters to modify:\
\- From the left panel, select parameters and move them to the right “Selected Parameters” panel using the \[▶] button.

\- Parameter icons:

* ![](<../../.gitbook/assets/Instance_12_Light (1).png>)  Instance: Values vary by individual element.
* ![](<../../.gitbook/assets/Icon_12_Type (1).png>)  Type: Shared values across elements of the same type.
* ![](../../.gitbook/assets/ReadOnly_12_Light.png)  Read-Only: Cannot be modified.

These labels help you quickly identify which parameters can be edited.

<figure><img src="../../.gitbook/assets/Select Parameter.gif" alt="" width="563"><figcaption></figcaption></figure>

### 5️⃣ Choose Export or Edit

After [selecting elements](how-to-use.md#id-3-select-target-elements) and [parameters](how-to-use.md#id-4-select-parameters):

➀ Export : Exports the selected parameter values to an Excel file. The file will open automatically.

<figure><img src="../../.gitbook/assets/export.gif" alt="" width="563"><figcaption></figcaption></figure>

➁ Edit : Opens a spreadsheet-style interface directly in Revit for fast, in-app editing.

<figure><img src="../../.gitbook/assets/Edit (1).gif" alt="" width="563"><figcaption></figcaption></figure>

### 6️⃣ Edit Parameter Values

You can update parameter values using either of these two methods:

#### ➀ Export to Excel&#x20;

* Export parameter values to an Excel file. Edit the values directly in Excel.

#### ➁ Edit in Spreadsheet&#x20;

* Open an in-app spreadsheet view inside Revit. Edit values instantly without leaving the model.



### 7️⃣ Apply Changes to the Model

Depending on how you edited the values, apply changes as follows:

#### ➀ From Excel

* After editing values in Excel, click \[Import] in Excel Sync to apply changes to the model.

<figure><img src="../../.gitbook/assets/import excel.gif" alt="" width="563"><figcaption></figcaption></figure>

#### ➁ From Spreadsheet&#x20;

* If you edited values in the in-app spreadsheet, click \[Apply] to immediately update the model.

<figure><img src="../../.gitbook/assets/Edit Apply.gif" alt="" width="563"><figcaption></figcaption></figure>

