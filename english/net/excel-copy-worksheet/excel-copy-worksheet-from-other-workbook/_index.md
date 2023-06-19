---
title: Excel Copy Worksheet From Other Workbook
linktitle: Excel Copy Worksheet From Other Workbook
second_title: Aspose.Cells for .NET API Reference
description: Easily copy an Excel worksheet from one workbook to another using Aspose.Cells for .NET.
type: docs
weight: 10
url: /net/excel-copy-worksheet/excel-copy-worksheet-from-other-workbook/
---
In this tutorial, we will walk you through the steps to copy an Excel worksheet from another workbook using the Aspose.Cells library for .NET. Follow the instructions below to complete this task.

## Step 1: Preparation

Before you begin, make sure you've installed Aspose.Cells for .NET and created a C# project in your preferred integrated development environment (IDE).

## Step 2: Set the document directory path

Declare a `dataDir` variable and initialize it with the path to your documents directory. For example :

```csharp
string dataDir = "YOUR_DIRECTORY_OF_DOCUMENTS";
```

Be sure to replace `"YOUR_DOCUMENTS_DIRECTORY"` with the actual path to your directory.

## Step 3: Create a new Excel workbook

Use the `Workbook` class from Aspose.Cells to create a new Excel workbook:

```csharp
Workbook excelWorkbook0 = new Workbook();
```

## Step 4: Get the first worksheet in the workbook

Navigate to the first worksheet in the workbook using index 0:

```csharp
Worksheet ws0 = excelWorkbook0.Worksheets[0];
```

## Step 5: Add data to header rows (A1:A4)

Use a `for` loop to add data to the header rows (A1:A4):

```csharp
for (int i = 0; i < 5; i++)
{
     ws0.Cells[i, 0].PutValue(string.Format("Header row {0}", i));
}
```

## Step 6: Add detailed data (A5:A999)

Use another `for` loop to add detailed data (A5:A999):

```csharp
for (int i = 5; i < 1000; i++)
{
     ws0.Cells[i, 0].PutValue(string.Format("Detail row {0}", i));
}
```

## Step 7: Set layout options

Set page setup options for the worksheet using the `PageSetup` object:

```csharp
PageSetup pagesetup = ws0.PageSetup;
pagesetup.PrintTitleRows = "$1:$5";
```

## Step 8: Create another Excel workbook

Create another Excel workbook:

```csharp
Workbook excelWorkbook1 = new Workbook();
```

## Step 9: Get the first worksheet from the second workbook

Navigate to the first worksheet in the second workbook:

```csharp
Worksheet ws1 = excelWorkbook1.Worksheets[0];
```

## Step 10: Name the worksheet

name the fire

calculation island:

```csharp
ws1.Name = "MySheet";
```

## Step 11: Copy data from the first worksheet of the first workbook to the first worksheet of the second workbook

Copy the data from the first worksheet of the first workbook to the first worksheet of the second workbook:

```csharp
ws1.Copy(ws0);
```

## Step 12: Save the Excel file

Save the Excel file:

```csharp
excelWorkbook1.Save(dataDir + "CopyWorkbookSheetToOther_out.xls");
```

Be sure to specify the desired path and filename for the output file.

### Sample source code for Excel Copy Worksheet From Other Workbook using Aspose.Cells for .NET 
```csharp
// The path to the documents directory.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Create a new Workbook.
Workbook excelWorkbook0 = new Workbook();
// Get the first worksheet in the book.
Worksheet ws0 = excelWorkbook0.Worksheets[0];
// Put some data into header rows (A1:A4)
for (int i = 0; i < 5; i++)
{
	ws0.Cells[i, 0].PutValue(string.Format("Header Row {0}", i));
}
// Put some detail data (A5:A999)
for (int i = 5; i < 1000; i++)
{
	ws0.Cells[i, 0].PutValue(string.Format("Detail Row {0}", i));
}
// Define a pagesetup object based on the first worksheet.
PageSetup pagesetup = ws0.PageSetup;
// The first five rows are repeated in each page...
// It can be seen in print preview.
pagesetup.PrintTitleRows = "$1:$5";
// Create another Workbook.
Workbook excelWorkbook1 = new Workbook();
// Get the first worksheet in the book.
Worksheet ws1 = excelWorkbook1.Worksheets[0];
// Name the worksheet.
ws1.Name = "MySheet";
// Copy data from the first worksheet of the first workbook into the
// first worksheet of the second workbook.
ws1.Copy(ws0);
// Save the excel file.
excelWorkbook1.Save(dataDir + "CopyWorksheetFromWorkbookToOther_out.xls");
```

## Conclusion

Congratulation ! You have now learned how to copy an Excel worksheet from another workbook using Aspose.Cells for .NET. Feel free to use this method in your own projects to efficiently manipulate Excel files.

### FAQs

#### Q. What libraries are needed to use Aspose.Cells for .NET?

     A. To use Aspose.Cells for .NET, you must include the Aspose.Cells library in your project. Make sure you have referenced this library correctly in your integrated development environment (IDE).

#### Q. Does Aspose.Cells support other Excel file formats, such as XLSX?

     A. Yes, Aspose.Cells supports various Excel file formats including XLSX, XLS, CSV, HTML, and many more. You can manipulate these file formats using the features of Aspose.Cells for .NET.

#### Q. Can I customize the layout options when copying the worksheet?

     A. Yes, you can customize the page setup options when copying the worksheet using the properties of the `PageSetup` object. You can specify page headers, footers, margins, orientations, etc.
