---
title: Fit To Excel Pages Options
linktitle: Fit To Excel Pages Options
second_title: Aspose.Cells for .NET API Reference
description: Learn how to autofit pages in an Excel spreadsheet with Aspose.Cells for .NET.
type: docs
weight: 30
url: /net/excel-page-setup/fit-to-excel-pages-options/
---
In this article, we will take you step by step to explain the following C# source code: Fit to Excel Pages Options using Aspose.Cells for .NET. We will use the Aspose.Cells library for .NET to perform this operation. Follow the steps below to configure fit to pages in Excel.

## Step 1: Creating a Workbook
The first step is to create a workbook. We are going to instantiate a Workbook object. Here is the code to create a workbook:

```csharp
// The path to the documents directory
string dataDir = "YOUR_DIRECTORY_OF_DOCUMENTS";

// Instantiate a Workbook object
Workbook workbook = new Workbook();
```

## Step 2: Accessing the worksheet
Now that we've created the workbook, we need to navigate to the first worksheet. We will use index 0 to access the first sheet. Here is the code to access it:

```csharp
// Access to the first worksheet in the workbook
Worksheet worksheet = workbook.Worksheets[0];
```

## Step 3: Setting Fit to Pages
In this step, we will configure the adjustment to the pages of the worksheet. We will use the `FitToPagesTall` and `FitToPagesWide` properties of the `PageSetup` object to specify the desired number of pages for the height and width of the worksheet. Here is the code for that:

```csharp
// Configure the number of pages for the height of the worksheet
worksheet.PageSetup.FitToPagesTall = 1;

// Configure the number of pages for the width of the worksheet
worksheet.PageSetup.FitToPagesWide = 1;
```

## Step 4: Saving the Workbook
Now that we've configured fit to pages, we can save the workbook. We will use the `Save` method of the Workbook object for this. Here is the code to save the workbook:

```csharp
// Save the workbook
workbook.Save(dataDir + "FitToPagesOptions_out.xls");
```

### Sample source code for Fit To Excel Pages Options using Aspose.Cells for .NET 
```csharp
// The path to the documents directory.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Instantiating a Workbook object
Workbook workbook = new Workbook();
// Accessing the first worksheet in the Excel file
Worksheet worksheet = workbook.Worksheets[0];
// Setting the number of pages to which the length of the worksheet will be spanned
worksheet.PageSetup.FitToPagesTall = 1;
// Setting the number of pages to which the width of the worksheet will be spanned
worksheet.PageSetup.FitToPagesWide = 1;
// Save the workbook.
workbook.Save(dataDir + "FitToPagesOptions_out.xls");
```

## Conclusion
In this article, we learned how to configure fit to pages in Excel using Aspose.Cells for .NET. We went through the following steps: creating the workbook, accessing the worksheet, configuring fit to pages, and saving the workbook. Now you can use this knowledge to adjust your spreadsheets to the desired pages.

### FAQs

#### Q: How can I install Aspose.Cells for .NET?

A: To install Aspose.Cells for .NET, you can use the NuGet package manager in Visual Studio. Find the "Aspose.Cells" package and install it in your project.

#### Q: Can I fit pages both height and width?

A: Yes, you can adjust both height and width of the worksheet using the `FitToPagesTall` and `FitToPagesWide` properties. You can specify the desired number of pages for each dimension.

#### Q: How can I customize the Fit to Pages options?

A: In addition to specifying the number of pages, you can also customize other fit-to-pages options such as worksheet scale, paper orientation, margins, and more. Use the properties available in the `PageSetup` object for this.

#### Q: Can I use Aspose.Cells for .NET to process existing workbooks?

A: Yes, you can use Aspose.Cells for .NET to open and edit existing workbooks. You can access worksheets, cells, formulas, styles, and other workbook items to perform various operations.
