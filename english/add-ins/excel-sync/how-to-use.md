# How to Use

### 1️⃣ Start Excel Sync

\- Open the BIMIL tab in Revit and click \[Excel Sync].

<figure><img src="../../.gitbook/assets/Click Excel Sync.gif" alt="" width="563"><figcaption></figcaption></figure>

### 2️⃣ Choose one of the three tabs at the top to define your target category:

\- In the main window, choose what kind of data you want to work with. There are three tabs available:\
&#x20;  • Model – for physical model elements\
&#x20;  • Annotation – for tags, dimensions, and text\
&#x20;  • Analytical Model – for structural analysis elements\
&#x20;  • <mark style="background-color:yellow;">Schedule (ver 1.0.1.0+) – for creating, editing, applying, or exporting Revit schedules in  Excel format</mark>

<figure><img src="../../.gitbook/assets/Excel Sync 5 (3) (1).png" alt=""><figcaption></figcaption></figure>

Select the desired tab and check the categories or individual elements you want to edit.\
<mark style="background-color:yellow;">You can now also enable checkboxes for elements from Linked Models (view only, v1.0.1.0+).</mark>

<figure><img src="../../.gitbook/assets/Model, Annotation, Analytical Model.gif" alt="" width="563"><figcaption></figcaption></figure>

### 3️⃣ Select Target Elements:&#x20;

Choose how to gather elements:

* &#x20;All : All elements in the model
* &#x20;Active View: Only elements visible in the current view
* &#x20;Selected Elements: Only elements you’ve pre-selected in the model
* <mark style="background-color:yellow;">Include Linked Models (v1.0.1.0+): Option to also include elements from Linked Models (view only)</mark>

<figure><img src="../../.gitbook/assets/All, Active View, Selected Element.gif" alt="" width="563"><figcaption></figcaption></figure>

### 4️⃣ Select Parameters

Choose which parameters to modify:\
\- From the left panel, select parameters and move them to the right “Selected Parameters” panel using the \[▶] button.

\- Parameter icons:

* ![](<../../.gitbook/assets/Instance_12_Light (1).png>)  Instance: Values vary by individual element.
* ![](<../../.gitbook/assets/Icon_12_Type (1).png>)  Type: Shared values across elements of the same type.
* ![](../../.gitbook/assets/ReadOnly_12_Light.png)  Read-Only: Cannot be modified.
* <img src="../../.gitbook/assets/Linked_12_Light (6) (1).png" alt="" data-size="line">  <mark style="background-color:yellow;">Linked included (v1.0.1.0+): Parameters coming from Linked Models (view only)</mark>
* <img src="../../.gitbook/assets/ScheduleParam_12_Light (1).png" alt="" data-size="line">  <mark style="background-color:yellow;">Schedule-Only</mark> _<mark style="background-color:yellow;">(v1.0.1.0+):</mark>_ <mark style="background-color:yellow;"></mark><mark style="background-color:yellow;">Parameters that are exclusive to the Schedule tab.</mark>

These labels help you quickly identify which parameters can be edited.

<figure><img src="../../.gitbook/assets/Select Parameter.gif" alt="" width="563"><figcaption></figcaption></figure>

### 5️⃣ Choose Export or Edit

After [selecting elements](how-to-use.md#id-3-select-target-elements) and [parameters](how-to-use.md#id-4-select-parameters):

➀ Export : Exports the selected parameter values to an Excel file. The file will open automatically.

<figure><img src="../../.gitbook/assets/export.gif" alt="" width="563"><figcaption></figcaption></figure>

#### &#x20;<mark style="background-color:yellow;">※ Export Options (Schedule Only)</mark> <mark style="background-color:yellow;"></mark>_<mark style="background-color:yellow;">(v1.0.1.0+)</mark>_

These options are available **only when exporting from the Schedule tab**.

* **Export in Schedule Format**
  * Exports in the same format as a Revit schedule.
  * Files exported in this format <mark style="color:red;">**cannot be re-imported**</mark> into Excel Sync.
* **Exclude unit from values**
  * Exports parameter values without unit symbols.

> ⚠️ **Exporting with Linked Models**
>
> * In **Model / Annotation / Analytical Model tabs**, linked elements are always included when exporting.
> * In the **Schedule tab**, behavior depends on the option:
>   * _Schedule Format_ → Linked elements included
>   * _Exclude unit from values_ → Linked elements excluded (only current model elements shown)

<figure><img src="../../.gitbook/assets/image (59).png" alt="" width="563"><figcaption></figcaption></figure>

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

