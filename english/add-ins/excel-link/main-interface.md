# Main Interface

<figure><img src="../../.gitbook/assets/image (6) (1).png" alt=""><figcaption></figcaption></figure>

The **Excel Link** main interface allows users to manage and integrate Excel data into Autodesk Revit projects seamlessly. The interface provides tools to add, update, duplicate, and delete data entries, as well as options to customize how data is displayed in Revit.

<figure><img src="../../.gitbook/assets/image (8).png" alt="" width="563"><figcaption></figcaption></figure>

## **Overview**

The main interface consists of a data table displaying all linked Excel/Clipboard entries and essential tools for managing those entries. Users can manage linked data entries in the table by adding new data, updating configurations, duplicating views, or removing views no longer needed.

Each entry in the table represents a connection between Revit and a specific set of Excel data, including its **status**, file path, and display settings. The interface ensures that updates in Excel are reflected in Revit with minimal effort, keeping your documentation accurate and up to date.

## Features

* [**Add from File**](add-from-file.md): Upload an Excel file to create a new data entry. Specify the worksheet, region, and view settings for integration into Revit.
* [**Add from Clipboard**](add-from-clipboard.md): Use data copied to the clipboard to create a table directly in Revit. Specify additional settings for how the data is displayed.
* **Edit**: Opens a configuration window to modify an existing entry. Click the pencil icon on the right side of the entry to access the editing options.
* **Refresh**: Updates the status of all entries in the data table based on their original sources.
* **Duplicate**: Creates a copy of the selected entry for additional adjustments. Works only on checked items.
* **Delete**: Removes the selected entry from the list. Works only on checked items.
* **OK**: Confirms and applies changes made to the data table. Works only on checked items.

<figure><img src="../../.gitbook/assets/image (10).png" alt=""><figcaption><p>Example : Legend View created by Excel Link</p></figcaption></figure>

## **Data Table**

The data table displays a detailed list of all linked Excel entries. Each row provides essential information, such as:

* **Status**: Indicates the current state of the entry. Possible statuses include:
  * **New**: The entry has been added to the table but has not yet been used to generate a view in Revit.
  * **Edited**: Modifications have been made to the entry within the Excel Link interface, such as updating view settings or changing the view name.
  * **Outdated**: The associated Excel file has been modified since the view was last created or updated in Revit, requiring a refresh to synchronize the data.
  * **File Not Found**: The Excel file linked to this entry cannot be located at the specified file path.
  * **View Deleted**: The Revit view created from this entry has been removed from the project, leaving the data entry without a corresponding view.
  * **Worksheet Not Found**: The worksheet specified in this entry no longer exists in the linked Excel file.
  * **Region Not Found**: The defined cell range in this entry is no longer available in the linked Excel file.
  * **Clipboard Lost**: The data originally sourced from the clipboard is no longer accessible, likely because it has been overwritten or cleared.
* **Source Type**: Specifies whether the entry is from an Excel file or clipboard.
* **View Details**: Includes the name, type (Legend, Schedule, Drafting View), and scale of the view in Revit.
* **File Information**: Displays the file path, last modified date, and selected worksheet or region from the Excel file.
