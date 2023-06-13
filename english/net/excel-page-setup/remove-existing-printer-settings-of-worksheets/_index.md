---
title: Remove Existing Printer Settings Of Worksheets
linktitle: Remove Existing Printer Settings Of Worksheets
second_title: Aspose.Cells for .NET API Reference
description: Learn how to remove existing printer settings from Excel spreadsheets with Aspose.Cells for .NET. 
type: docs
weight: 80
url: /net/excel-page-setup/remove-existing-printer-settings-of-worksheets/
---
In this tutorial, we will walk you through step by step how to remove existing printer settings from worksheets in Excel using Aspose.Cells for .NET. We will use C# source code to illustrate the process.

## Step 1: Setting up the environment

Make sure you have Aspose.Cells for .NET installed on your machine. Also create a new project in your preferred development environment.

## Step 2: Import necessary libraries

In your code file, import the libraries needed to work with Aspose.Cells. Here is the corresponding code:

```csharp
using Aspose.Cells;
```

## Step 3: Set source and output directories

Set the source and output directories where the original Excel file is located and where you want to save the modified file respectively. Use the following code:

```csharp
string sourceDir = "SOURCE DIRECTORY PATH";
string outputDir = "OUTPUT DIRECTORY PATH";
```

Be sure to specify full directory paths.

## Step 4: Loading the Source Excel File

Load the source Excel file using the following code:

```csharp
Workbook wb = new Workbook(sourceDir + "fileName.xlsx");
```

This will load the specified Excel file into the Workbook object.

## Step 5: Navigate the worksheets

Iterate through all the worksheets in the workbook using a loop. Use the following code:

```csharp
int sheetCount = wb. Worksheets. Count;

for (int i = 0; i < sheetCount; i++)
{
     Worksheet ws = wb.Worksheets[i];
     // The rest of the code will be added in the next step.
}
```

## Step 6: Delete Existing Printer Settings

Check if printer settings exist for each worksheet and delete them if necessary. Use the following code:

```csharp
PageSetup ps = ws.PageSetup;

if (ps.PrinterSettings != null)
{
     Console.WriteLine("Printer settings for this spreadsheet exist.");
     Console.WriteLine("Sheet name: " + ws.Name);
     Console.WriteLine("Paper size: " + ps.PaperSize);

     ps.PrinterSettings = null;

     Console.WriteLine("Printer settings for this spreadsheet have been removed by setting them to null.");
     Console.WriteLine("");
}
```

## Step 7: Saving the Modified Workbook

Save the modified workbook using the following code:

```csharp
wb.Save(outputDir + "modifiedFilename.xlsx");
```

This will save the modified workbook to the specified output directory.

### Sample source code for Remove Existing Printer Settings Of Worksheets using Aspose.Cells for .NET 
```csharp
//Source directory
string sourceDir = RunExamples.Get_SourceDirectory();
//Output directory
string outputDir = RunExamples.Get_OutputDirectory();
//Load source Excel file
Workbook wb = new Workbook(sourceDir + "sampleRemoveExistingPrinterSettingsOfWorksheets.xlsx");
//Get the sheet counts of the workbook
int sheetCount = wb.Worksheets.Count;
//Iterate all sheets
for (int i = 0; i < sheetCount; i++)
{
    //Access the i-th worksheet
    Worksheet ws = wb.Worksheets[i];
    //Access worksheet page setup
    PageSetup ps = ws.PageSetup;
    //Check if printer settings for this worksheet exist
    if (ps.PrinterSettings != null)
    {
        //Print the following message
        Console.WriteLine("PrinterSettings of this worksheet exist.");
        //Print sheet name and its paper size
        Console.WriteLine("Sheet Name: " + ws.Name);
        Console.WriteLine("Paper Size: " + ps.PaperSize);
        //Remove the printer settings by setting them null
        ps.PrinterSettings = null;
        Console.WriteLine("Printer settings of this worksheet are now removed by setting it null.");
        Console.WriteLine("");
    }//if
}//for
//Save the workbook
wb.Save(outputDir + "outputRemoveExistingPrinterSettingsOfWorksheets.xlsx");
```

## Conclusion

You have now learned how to remove existing printer settings from worksheets in Excel using Aspose.Cells for .NET. This tutorial walked you through every step of the process, from setting up the environment to navigating through spreadsheets and clearing printer settings. You can now use this knowledge to manage printer settings in your Excel files.

## FAQ's

**Q1: How do I know if a spreadsheet has existing printer settings?**

A1: You can check if printer settings exist for a worksheet by accessing the `PrinterSettings` property of the `PageSetup` object. If the value is non-null, it means there are existing printer settings.

**Q2: Can I delete printer settings for a specific spreadsheet only?**

A2: Yes, you can use the same approach to remove printer settings for a specific worksheet by accessing that worksheet's `PageSetup` object.

**Q3: Does this method remove other layout settings as well?**

A3: No, this method only deletes printer settings. Other layout settings, such as margins, paper orientation, etc., remain unchanged.

**Q4: Does this method work for all Excel file formats, such as .xls and .xlsx?**

A4: Yes, this method works for all Excel file formats supported by Aspose.Cells, including .xls and .xlsx.

**Q5: Are changes made to printer settings permanent in the edited Excel file?**

A5: Yes, changes to printer settings are permanently saved in the edited Excel file.