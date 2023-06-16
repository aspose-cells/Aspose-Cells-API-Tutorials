---
title: Remove Panes Of Worksheet
linktitle: Remove Panes Of Worksheet
second_title: Aspose.Cells for .NET API Reference
description: Step by step guide to remove panes from an Excel worksheet using Aspose.Cells for .NET.
type: docs
weight: 120
url: /net/excel-display-settings-csharp-tutorials/remove-panes-of-worksheet/
---
In this tutorial, we will explain how to remove panes from an Excel worksheet using Aspose.Cells for .NET. Follow these steps to get the desired result:

## Step 1: Setting up the environment

Make sure you have installed Aspose.Cells for .NET and set up your development environment. Also, make sure you have a copy of the Excel file you want to remove the panes from.

## Step 2: Import the necessary dependencies

Add the necessary directives to use the classes from Aspose.Cells:

```csharp
using Aspose.Cells;
```

## Step 3: Code initialization

Start by initializing the path to the directory containing your Excel documents:

```csharp
string dataDir = "YOUR DOCUMENTS DIRECTORY";
```

## Step 4: Opening the Excel file

Instantiate a new `Workbook` object and open the Excel file using the `Open` method:

```csharp
Workbook book = new Workbook(dataDir + "Book1.xls");
```

## Step 5: Define the active cell

Set the active cell of the worksheet using the `ActiveCell` property:

```csharp
book.Worksheets[0].ActiveCell = "A20";
```

## Step 6: Deleting the panes

Remove panes from the worksheet window using the `RemoveSplit` method:

```csharp
book.Worksheets[0].RemoveSplit();
```

## Step 7: Saving Changes

Save the changes made to the Excel file:

```csharp
book.Save(dataDir + "output.xls");
```

### Sample source code for Remove Panes Of Worksheet using Aspose.Cells for .NET 
```csharp
// The path to the documents directory.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Instantiate a new workbook and Open a template file
Workbook book = new Workbook(dataDir + "Book1.xls");
// Set the active cell
book.Worksheets[0].ActiveCell = "A20";
// Split the worksheet window
book.Worksheets[0].RemoveSplit();
// Save the excel file
book.Save(dataDir + "output.xls");
```

## Conclusion

In this tutorial, you learned how to remove panes from an Excel worksheet using Aspose.Cells for .NET. By following the steps described, you can easily customize the appearance and behavior of your Excel files.

## Frequently Asked Questions (FAQ)

**What is Aspose.Cells for .NET?**

Aspose.Cells for .NET is a popular software library for manipulating Excel files in .NET applications.

**How can I set the active cell of a worksheet in Aspose.Cells?**

You can set the active cell using the `ActiveCell` property of the Worksheet object.

**Can I remove only horizontal or vertical panes from the worksheet window?**

Yes, using Aspose.Cells you can remove only horizontal or vertical panes using the appropriate methods such as `RemoveHorizontalSplit` or `RemoveVerticalSplit`.

**Does Aspose.Cells only work with Excel files in .xls format?**

No, Aspose.Cells supports various Excel file formats including .xls and .xlsx.
	