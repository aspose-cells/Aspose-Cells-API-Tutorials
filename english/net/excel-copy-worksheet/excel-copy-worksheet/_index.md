---
title: Excel Copy Worksheet
linktitle: Excel Copy Worksheet
second_title: Aspose.Cells for .NET API Reference
description: Copy one Excel worksheet to another with Aspose.Cells for .NET.
type: docs
weight: 20
url: /net/excel-copy-worksheet/excel-copy-worksheet/
---

In this guide, we will explain how to copy an Excel worksheet using the Aspose.Cells library for .NET. We'll provide you with C# source code and walk you through the steps needed to complete this task. At the end, we will show you the expected result. Follow the instructions below to get started.

## Step 1: Preparation

Before you begin, make sure you've installed Aspose.Cells for .NET and created a C# project in your preferred integrated development environment (IDE). Also make sure you have a copy of the Excel file you want to manipulate.

## Step 2: Import required libraries

In your C# source file, import the necessary libraries from Aspose.Cells using the `using` directive:

```csharp
using Aspose.Cells;
```

## Step 3: Set the file path

Declare a `dataDir` variable and initialize it with the directory containing your Excel file. For example :

```csharp
string dataDir = "PATH_TO_YOUR_DOCUMENT_DIRECTORY";
```

Be sure to replace `"PATH_TO_YOUR_DOCUMENT_DIRECTORY"` with the actual path to your directory.

## Step 4: Load existing Excel file

Use the `Workbook` class from Aspose.Cells to open the existing Excel file. Use the `InputPath` variable to specify the file path:

```csharp
string InputPath = dataDir + "book1.xls";
Workbook wb = new Workbook(InputPath);
```

Make sure you have replaced `"book1.xls"` with the actual name of your Excel file.

## Step 5: Copy the worksheet

Now we will copy the existing worksheet to a new worksheet. Use the `Worksheets` property of the `Workbook` object to access the collection of worksheets:

```csharp
WorksheetCollection sheets = wb.Worksheets;
```

Then use the `AddCopy` method to copy the specified worksheet. For example, to copy "Sheet1":

```csharp
sheets.AddCopy("Sheet1");
```

## Step 6: Save the Excel file

Use the `Save` method of the `Workbook` object to save changes to a new file:

```csharp
wb.Save(dataDir + "CopyWithinWorkbook_out.xls");
```

Be sure to specify the desired path and filename for the output file.

### Sample source code for Excel Copy Worksheet using Aspose.Cells for .NET 

```csharp
// The path to the documents directory.
string dataDir = "YOUR DOCUMENT DIRECTORY";
string InputPath = dataDir + "book1.xls";
// Open an existing Excel file.
Workbook wb = new Workbook(InputPath);
// Create a Worksheets object with reference to
// the sheets of the Workbook.
WorksheetCollection sheets = wb.Worksheets;
// Copy data to a new sheet from an existing
// sheet within the Workbook.
sheets.AddCopy("Sheet1");
// Save the Excel file.
wb.Save(dataDir + "CopyWithinWorkbook_out.xls");
```

## Conclusion

Congratulation ! You have now learned how to copy an Excel worksheet using Aspose.Cells for .NET. This step-by-step guide showed how to import the necessary libraries, load an existing Excel file, copy the worksheet and save the modified file. Feel free to use this method in your own projects to efficiently manipulate Excel files.

### FAQs

#### Q. Is Aspose.Cells compatible with other programming languages?

	 A. Yes, Aspose.Cells supports multiple programming languages including C#, Java, Python and many more.

#### Q. Can I copy a worksheet to another Excel workbook?

     A. Yes, you can use the `AddCopy` method to copy a worksheet to another Excel workbook.

#### Q. Does Aspose.Cells preserve formulas and formatting when copying the worksheet?

	 A. Yes, Aspose.Cells preserves formulas, formatting and other properties when copying a worksheet.

#### Q. Does Aspose.Cells require a license for commercial use?

     A. Yes, Aspose.Cells is a commercial product and requires the purchase of a license for commercial use. You can find more licensing information on Aspose's official website.
