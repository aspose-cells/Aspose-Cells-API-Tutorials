---
title: Excel Copy Worksheets Between Workbooks
linktitle: Excel Copy Worksheets Between Workbooks
second_title: Aspose.Cells for .NET API Reference
description: Easily copy worksheets between Excel workbooks using Aspose.Cells for .NET.
type: docs
weight: 30
url: /net/excel-copy-worksheet/excel-copy-worksheets-between-workbooks/
---
In this tutorial, we will guide you through the steps to copy worksheets between Excel workbooks using the Aspose.Cells library for .NET. Follow the instructions below to complete this task.

## Step 1: Preparation

Make sure you have installed Aspose.Cells for .NET and created a C# project in your preferred integrated development environment (IDE).

## Step 2: Set the document directory path

Declare a `dataDir` variable and initialize it with the path to your documents directory. For example :

```csharp
string dataDir = "YOUR_DIRECTORY_OF_DOCUMENTS";
```

Be sure to replace `"YOUR_DOCUMENTS_DIRECTORY"` with the actual path to your directory.

## Step 3: Define the input file path

Declare an `InputPath` variable and initialize it with the full path of the Excel file from which you want to copy the spreadsheet. For example :

```csharp
string InputPath = dataDir + "book1.xls";
```

Make sure you have the Excel file `book1.xls` in your documents directory or specify the correct file name and location.

## Step 4: Create a first Excel workbook

Use the `Workbook` class of Aspose.Cells to create a first Excel workbook and open the specified file:

```csharp
Workbook excelWorkbook0 = new Workbook(InputPath);
```

## Step 5: Create a second Excel workbook

Create a second Excel workbook:

```csharp
Workbook excelWorkbook1 = new Workbook();
```

## Step 6: Copy the worksheet from the first workbook to the second workbook

Use the `Copy` method to copy the first worksheet from the first workbook to the second workbook:

```csharp
excelWorkbook1.Worksheets[0].Copy(excelWorkbook0.Worksheets[0]);
```

## Step 7: Save the Excel file

Save the Excel file containing the copied spreadsheet:

```csharp
excelWorkbook1.Save(dataDir + "Copy WorksheetsBetweenWorkbooks_out.xls");
```

Be sure to specify the desired path and filename for the output file.

### Sample source code for Excel Copy Worksheets Between Workbooks using Aspose.Cells for .NET 
```csharp
// The path to the documents directory.
string dataDir = "YOUR DOCUMENT DIRECTORY";
string InputPath = dataDir + "book1.xls";
// Create a Workbook.
// Open a file into the first book.
Workbook excelWorkbook0 = new Workbook(InputPath);
// Create another Workbook.
Workbook excelWorkbook1 = new Workbook();
// Copy the first sheet of the first book into second book.
excelWorkbook1.Worksheets[0].Copy(excelWorkbook0.Worksheets[0]);
// Save the file.
excelWorkbook1.Save(dataDir + "CopyWorksheetsBetweenWorkbooks_out.xls");
```

## Conclusion

Congratulation ! You have now learned how to copy worksheets between Excel workbooks using Aspose.Cells for .NET. Feel free to use this method in your own projects to efficiently manipulate Excel files.

### FAQs

#### Q. What libraries are needed to use Aspose.Cells for .NET?

     A. To use Aspose.Cells for .NET, you must include the Aspose.Cells library in your project. Make sure you have referenced this library correctly in your integrated development environment (IDE).

#### Q. Does Aspose.Cells support other Excel file formats, such as XLSX?

	 A. Yes, Aspose.Cells supports various Excel file formats including XLSX, XLS, CSV, HTML, and many more. You can manipulate these file formats using the features of Aspose.Cells for .NET.

#### Q. Can I customize the layout options when copying the spreadsheet?

     A. Yes, you can customize the page setup options when copying the spreadsheet using the properties of the `PageSetup` object. You can specify page headers, footers, margins, orientations, etc.
