---
title: Set Excel Print Area
linktitle: Set Excel Print Area
second_title: Aspose.Cells for .NET API Reference
description: Step by step guide to set Excel print area using Aspose.Cells for .NET. Optimize and customize your Excel workbooks easily.
type: docs
weight: 140
url: /net/excel-page-setup/set-excel-print-area/
---
Using Aspose.Cells for .NET can greatly facilitate the management and manipulation of Excel files in .NET applications. In this guide, we will show you how to set the print area of an Excel workbook using Aspose.Cells for .NET. We will guide you step by step through the provided C# source code to accomplish this task.

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

To set the print area, we first need to get the reference from the worksheet's PageSetup. Use the following code to get the reference:

```csharp
PageSetup pageSetup = workbook.Worksheets[0].PageSetup;
```

## Step 6: Specifying the print area cell range

Now that we have the PageSetup reference, we can specify the range of cells that make up the print area. In this example, we will set the cell range from A1 to T35 as the print area. Use the following code:

```csharp
pageSetup.PrintArea = "A1:T35";
```

You can adjust the cell range according to your needs.

## Step 7: Saving the Excel workbook

To save the Excel workbook with the print area defined, use the `Save` method of the Workbook object:

```csharp
workbook.Save(dataDir + "SetPrintArea_out.xls");
```

This will save the Excel workbook with file name "SetPrintArea_out.xls" in the specified directory.

### Sample source code for Set Excel Print Area using Aspose.Cells for .NET 
```csharp
// The path to the documents directory.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Instantiating a Workbook object
Workbook workbook = new Workbook();
// Obtaining the reference of the PageSetup of the worksheet
PageSetup pageSetup = workbook.Worksheets[0].PageSetup;
// Specifying the cells range (from A1 cell to T35 cell) of the print area
pageSetup.PrintArea = "A1:T35";
// Save the workbook.
workbook.Save(dataDir + "SetPrintArea_out.xls");
```

## Conclusion

Congratulation ! You have now learned how to set the print area of an Excel workbook using Aspose.Cells for .NET. This powerful and user-friendly library makes it much easier to work with Excel files in your .NET applications. If you have additional questions or run into any difficulties, feel free to check out the official Aspose.Cells documentation for more information and resources.

### FAQ's

#### 1. Can I further customize the layout of the print area, such as orientation and margins?

Yes, you can access other PageSetup properties such as page orientation, margins, scale, etc. to further customize your print area layout.

#### 2. Does Aspose.Cells for .NET support other Excel file formats, such as XLSX and CSV?

Yes, Aspose.Cells for .NET supports a variety of Excel file formats including XLSX, XLS, CSV, HTML, PDF and many more.

#### 3. Is Aspose.Cells for .NET compatible with all versions of .NET Framework?

Aspose.Cells for .NET is compatible with .NET Framework 2.0 or later, including versions 3.5, 4.0, 4.5, 4.6, etc.