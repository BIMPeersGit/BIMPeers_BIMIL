# Add From File

<figure><img src="../../.gitbook/assets/image (4) (1) (1).png" alt="" width="443"><figcaption></figcaption></figure>

The **Add From File** interface lets you select and configure data from an Excel file for seamless integration into Revit. It provides options to choose a file, specify the worksheet and region, and customize the resulting view settings, all within a single window.

## **Excel File Selection**

Start by selecting the Excel file that contains the data you want to use. The selected file’s path will be displayed at the top of the interface for reference.

## **Worksheet and Region Selection**

* **Worksheet**: Choose the worksheet from the dropdown menu. Only the data from the selected sheet will be included.
* **Region**: Define the area within the worksheet to use. You can either:
  * Select a predefined named worksheet region stored in excel.
  * Manually highlight cells in the **Preview Panel** by dragging over the desired range (\*Custom Range).

## **Preview Panel**

The preview panel provides a visual representation of the selected worksheet and highlights any defined regions or manually selected cell ranges.

## **View Configuration**

Customize how the imported data will appear in Revit:

* **View Name**: Define the name of the view that will display the data in Revit.
* **View Type**: Choose from **Legend**, **Schedule**, or **Drafting View** to control how the data is integrated into your project.
* **View Scale**: Adjust the scale of the view to fit your project's requirements.
* **Font**: Select the font style for the table:
  * Use Revit’s font library.
  * Or retain the font style applied to the clipboard data (from Excel).

## **Action Buttons**

* **OK**: Confirms your settings and adds the entry to the main interface.
* **Cancel**: Closes the window without saving any changes.
