---
title: Manage Excel Paper Size
linktitle: Manage Excel Paper Size
second_title: Aspose.Cells for .NET API Reference
description: Learn how to manage paper size in Excel with Aspose.Cells for .NET. Step by step tutorial with source code in C#.
type: docs
weight: 70
url: /net/excel-page-setup/manage-excel-paper-size/
---
In this tutorial, we will guide you step by step on how to manage paper size in Excel document using Aspose.Cells for .NET. We'll show you how to configure the paper size using C# source code.

## Step 1: Setting up the environment

Make sure you have Aspose.Cells for .NET installed on your machine. Also create a new project in your preferred development environment.

## Step 2: Import necessary libraries

In your code file, import the libraries needed to work with Aspose.Cells. Here is the corresponding code:

```csharp
using Aspose.Cells;
```

## Step 3: Set Document Directory

Set the directory where the Excel document you want to work with is located. Use the following code to set the directory:

```csharp
string dataDir = "YOUR DOCUMENTS DIRECTORY";
```

Be sure to specify the full directory path.

## Step 4: Creating a Workbook Object

The Workbook object represents the Excel document with which you will work. You can create it using the following code:

```csharp
Workbook workbook = new Workbook();
```

This creates a new empty Workbook object.

## Step 5: Access to the first worksheet

To access the first spreadsheet of the Excel document, use the following code:

```csharp
Worksheet worksheet = workbook.Worksheets[0];
```

This will allow you to work with the first worksheet in the workbook.

## Step 6: Paper Size Setup

Use the PageSetup.PaperSize property of the Worksheet object to set the paper size. In this example, we will set the paper size to A4. Here is the corresponding code:

```csharp
worksheet.PageSetup.PaperSize = PaperSizeType.PaperA4;
```

This sets the spreadsheet paper size to A4.

## Step 7: Saving the workbook

To save changes to the workbook, use the Save() method of the Workbook object. Here is the corresponding code:

```csharp
workbook.Save(dataDir + "ManagePaperSize_out.xls");
```

This will save the workbook with the changes to the specified directory.

### Sample source code for Manage Excel Paper Size using Aspose.Cells for .NET 
```csharp
// The path to the documents directory.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Instantiating a Workbook object
Workbook workbook = new Workbook();
// Accessing the first worksheet in the Excel file
Worksheet worksheet = workbook.Worksheets[0];
// Setting the paper size to A4
worksheet.PageSetup.PaperSize = PaperSizeType.PaperA4;
// Save the Workbook.
workbook.Save(dataDir + "ManagePaperSize_out.xls");
```
## Conclusion

You have now learned how to manage paper size in an Excel document using Aspose.Cells for .NET. This tutorial walked you through every step of the process, from setting up the environment to saving changes. You can now use this knowledge to customize the paper size of your Excel documents.

### FAQ's

**Q1: Can I set a custom paper size other than A4?**

A1: Yes, Aspose.Cells supports a variety of predefined paper sizes as well as the ability to set a custom paper size by specifying the desired dimensions.

**Q2: How can I know the current paper size in an Excel document?**

A2: You can use the `PageSetup.PaperSize` property of the `Worksheet` object to get the currently set paper size.

**Q3: Is it possible to set extra page margins with paper size?**

A3: Yes, you can use `PageSetup.LeftMargin`, `PageSetup.RightMargin`, `PageSetup.TopMargin` and `PageSetup.BottomMargin` properties to set additional page margins besides paper size.

**Q4: Does this method work for all Excel file formats, such as .xls and .xlsx?**

A4: Yes, this method works for both .xls and .xlsx file formats.

**Q5: Can I apply different paper sizes to different worksheets in the same workbook?**

A5: Yes, you can apply different paper sizes to different worksheets in the same workbook by using the `PageSetup.PaperSize` property of each worksheet.