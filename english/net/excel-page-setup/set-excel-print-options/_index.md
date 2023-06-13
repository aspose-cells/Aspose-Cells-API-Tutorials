---
title: Set Excel Print Options
linktitle: Set Excel Print Options
second_title: Aspose.Cells for .NET API Reference
description: Learn to manipulate Excel files and customize printing options with ease using Aspose.Cells for .NET.
type: docs
weight: 150
url: /net/excel-page-setup/set-excel-print-options/
---
In this guide, we will walk you through how to set print options for an Excel workbook using Aspose.Cells for .NET. We'll take you step-by-step through the provided C# source code to accomplish this task.

## Step 1: Setting up the environment

Before you begin, make sure you have set up your development environment and installed Aspose.Cells for .NET. You can download the latest version of the library from Aspose official website.

## Step 2: Import required namespaces

In your C# project, import the necessary namespaces to work with Aspose.Cells:

```csharp
using Aspose.Cells;
```

## Step 3: Setting the path to the documents directory

Declare a `dataDir` variable to specify the path to the directory where you want to save the generated Excel file:

```csharp
string dataDir = "YOUR_DIRECTORY_OF_DOCUMENTS";
```

Be sure to replace `"YOUR_DOCUMENT_DIRECTORY"` with the correct path on your system.

## Step 4: Creating a Workbook Object

Instantiate a Workbook object that represents the Excel workbook you want to create:

```csharp
Workbook workbook = new Workbook();
```

## Step 5: Obtaining the PageSetup reference of the worksheet

To set the print options, we first need to get the PageSetup reference from the worksheet. Use the following code to get the reference:

```csharp
PageSetup pageSetup = workbook.Worksheets[0].PageSetup;
```

## Step 6: Enable Printing Grid Lines

To enable grid lines to be printed, use the following code:

```csharp
pageSetup. PrintGridlines = true;
```

## Step 7: Enable Row/Column Header Printing

To enable the printing of row and column headers, use the following code:

```csharp
pageSetup.PrintHeadings = true;
```

## Step 8: Enabling Black and White Print Mode

To enable printing of the worksheet in black and white mode, use the following code:

```csharp
pageSetup.BlackAndWhite = true;
```

## Step 9: Enabling Feedback Printing

To allow comments to be printed as they appear on the spreadsheet, use the following code:

```csharp
pageSetup.PrintComments = PrintCommentsType.PrintInPlace;
```

## Step 10: Enable Draft Mode Printing

To enable printing of the spreadsheet in draft mode, use the following code:

```csharp
pageSetup.PrintDraft = true;
```

## Step 11: Enable Printing Cell Errors as N/A

To allow cell errors to be printed as

  than N/A, use the following code:

```csharp
pageSetup.PrintErrors = PrintErrorsType.PrintErrorsNA;
```

## Step 12: Saving the Excel workbook

To save the Excel workbook with the print options set, use the `Save` method of the Workbook object:

```csharp
workbook.Save(dataDir + "OtherPrintOptions_out.xls");
```

This will save the Excel workbook with file name "OtherPrintOptions_out.xls" in the specified directory.

### Sample source code for Set Excel Print Options using Aspose.Cells for .NET 
```csharp
// The path to the documents directory.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Instantiating a Workbook object
Workbook workbook = new Workbook();
// Obtaining the reference of the PageSetup of the worksheet
PageSetup pageSetup = workbook.Worksheets[0].PageSetup;
// Allowing to print gridlines
pageSetup.PrintGridlines = true;
// Allowing to print row/column headings
pageSetup.PrintHeadings = true;
// Allowing to print worksheet in black & white mode
pageSetup.BlackAndWhite = true;
// Allowing to print comments as displayed on worksheet
pageSetup.PrintComments = PrintCommentsType.PrintInPlace;
// Allowing to print worksheet with draft quality
pageSetup.PrintDraft = true;
// Allowing to print cell errors as N/A
pageSetup.PrintErrors = PrintErrorsType.PrintErrorsNA;
// Save the workbook.
workbook.Save(dataDir + "OtherPrintOptions_out.xls");
```
## Conclusion

You have now learned how to set print options for an Excel workbook using Aspose.Cells for .NET. This powerful and user-friendly library allows you to customize the print settings of your Excel workbooks in an easy and efficient way.

### FAQs


**1. Can I further customize print options, such as margins or page orientation?**

Yes, Aspose.Cells for .NET offers a wide range of customizable printing options, such as margins, page orientation, scale, etc.

**2. Does Aspose.Cells for .NET support other Excel file formats?**

Yes, Aspose.Cells for .NET supports a variety of Excel file formats, such as XLSX, XLS, CSV, HTML, PDF, etc.

**3. Is Aspose.Cells for .NET compatible with all versions of .NET Framework?**

Aspose.Cells for .NET is compatible with .NET Framework 2.0 or later, including versions 3.5, 4.0, 4.5, 4.6, etc.