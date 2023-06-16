---
title: Set Excel Page Order
linktitle: Set Excel Page Order
second_title: Aspose.Cells for .NET API Reference
description: Step by step guide to set page order in Excel using Aspose.Cells for .NET. Detailed instructions and source code included.
type: docs
weight: 120
url: /net/excel-page-setup/set-excel-page-order/
---
In this article, we will guide you step by step to explain the following C# source code to set Excel page order using Aspose.Cells for .NET. We'll show you how to set up the documents directory, instantiate a Workbook object, get the PageSetup reference, set the page print order, and save the workbook.

## Step 1: Document Directory Setup

Before you start, you need to configure the document directory where you want to save the Excel file. You can specify the directory path by replacing the value of the `dataDir` variable with your own path.

```csharp
// The path to the documents directory.
string dataDir = "YOUR_DIRECTORY_OF_DOCUMENTS";
```

## Step 2: Instantiating a Workbook Object

The first step is to instantiate a Workbook object. This represents the Excel workbook we will be working with.

```csharp
// Instantiate a Workbook object
Workbook workbook = new Workbook();
```

## Step 3: Obtaining the PageSetup reference

Next, we need to get the PageSetup object reference of the worksheet on which we want to set the page order.

```csharp
// Obtain the PageSetup reference of the worksheet
PageSetup pageSetup = workbook.Worksheets[0].PageSetup;
```

## Step 4: Setting the Print Order of Pages

Now we can set the print order of the pages. In this example, we are using the "OverThenDown" option, which means that the pages will be printed left to right, then top to bottom.

```csharp
// Set the page print order to "OverThenDown"
pageSetup.Order = PrintOrderType.OverThenDown;
```

## Step 5: Saving the workbook

Finally, we save the Excel workbook with the page order changes.

```csharp
// Save the workbook
workbook.Save(dataDir + "SetPageOrder_out.xls");
```

### Sample source code for Set Excel Page Order using Aspose.Cells for .NET 
```csharp
// The path to the documents directory.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Instantiating a Workbook object
Workbook workbook = new Workbook();
// Obtaining the reference of the PageSetup of the worksheet
PageSetup pageSetup = workbook.Worksheets[0].PageSetup;
// Setting the printing order of the pages to over then down
pageSetup.Order = PrintOrderType.OverThenDown;
// Save the workbook.
workbook.Save(dataDir + "SetPageOrder_out.xls");
```

## Conclusion

In this tutorial, we explained how to set page order in an Excel file using Aspose.Cells for .NET. By following the steps provided, you can easily configure the document directory, instantiate a Workbook object, get the PageSetup reference, set the page print order, and save the workbook.

### FAQ's

#### Q1: Why is it important to set page order in an Excel file?

Defining the order of pages in an Excel file is important because it determines how the pages will be printed or displayed. By specifying a specific order, you can organize the data logically and make the file easier to read or print.

#### Q2: Can I use other page print orders with Aspose.Cells for .NET?

Yes, Aspose.Cells for .NET supports multiple page print orders such as "DownThenOver", "OverThenDown", "DownThenOverThenDownAgain", etc. You can choose the one that best suits your needs.

#### Q3: Can I set additional options for printing pages with Aspose.Cells for .NET?

Yes, you can set various page printing options such as scale, orientation, margins, etc., using the properties of the PageSetup object in Aspose.Cells for .NET.

#### Q4: Does Aspose.Cells for .NET support other Excel file formats?

Yes, Aspose.Cells for .NET supports a wide range of Excel file formats such as XLSX, XLS, CSV, HTML, PDF, etc. You can easily convert between these formats using the features provided by the library.
