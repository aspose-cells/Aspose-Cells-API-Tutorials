---
title: Excel Move Worksheet
linktitle: Excel Move Worksheet
second_title: Aspose.Cells for .NET API Reference
description: Easily move worksheet into an Excel workbook using Aspose.Cells for .NET.
type: docs
weight: 40
url: /net/excel-copy-worksheet/excel-move-worksheet/
---
In this tutorial, we will walk you through the steps to move a worksheet into an Excel workbook using the Aspose.Cells library for .NET. Follow the instructions below to complete this task.


## Step 1: Preparation

Make sure you have installed Aspose.Cells for .NET and created a C# project in your preferred integrated development environment (IDE).

## Step 2: Set the document directory path

Declare a `dataDir` variable and initialize it with the path to your documents directory. For example :

```csharp
string dataDir = "YOUR_DIRECTORY_OF_DOCUMENTS";
```

Be sure to replace `"YOUR_DOCUMENTS_DIRECTORY"` with the actual path to your directory.

## Step 3: Define the input file path

Declare an `InputPath` variable and initialize it with the full path of the existing Excel file you want to modify. For example :

```csharp
string InputPath = dataDir + "book1.xls";
```

Make sure you have the Excel file `book1.xls` in your documents directory or specify the correct file name and location.

## Step 4: Open the Excel file

Use the `Workbook` class of Aspose.Cells to open the specified Excel file:

```csharp
Workbook wb = new Workbook(InputPath);
```

## Step 5: Get the spreadsheet collection

Create a `WorksheetCollection` object to refer to worksheets in the workbook:

```csharp
WorksheetCollection sheets = wb.Worksheets;
```

## Step 6: Get the first worksheet

Get the first worksheet in the workbook:

```csharp
Worksheet worksheet = sheets[0];
```

## Step 7: Move the worksheet

Use the `MoveTo` method to move the first worksheet to the third position in the workbook:

```csharp
worksheet.MoveTo(2);
```

## Step 8: Save the modified Excel file

Save the Excel file with the moved worksheet:

```csharp
wb.Save(dataDir + "MoveWorksheet_out.xls");
```

Be sure to specify the desired path and filename for the output file.

### Sample source code for Excel Move Worksheet using Aspose.Cells for .NET 
```csharp
// The path to the documents directory.
string dataDir = "YOUR DOCUMENT DIRECTORY";
string InputPath = dataDir + "book1.xls";
// Open an existing excel file.
Workbook wb = new Workbook(InputPath);
// Create a Worksheets object with reference to
// the sheets of the Workbook.
WorksheetCollection sheets = wb.Worksheets;
// Get the first worksheet.
Worksheet worksheet = sheets[0];
// Move the first sheet to the third position in the workbook.
worksheet.MoveTo(2);
// Save the excel file.
wb.Save(dataDir + "MoveWorksheet_out.xls");
```

## Conclusion

Congratulation ! You have now learned how to move a worksheet into an Excel workbook using Aspose.Cells for .NET. Feel free to use this method in your own projects to efficiently manipulate Excel files.

### FAQs

#### Q. Can I move a worksheet to another position in the same Excel workbook?

	 A. Yes, you can move a worksheet to another position in the same Excel workbook using `MoveTo` method of Worksheet object. Just specify the index of the destination position in the workbook.

#### Q. Can I move a worksheet to another Excel workbook?

	 A. Yes, you can move a worksheet to another Excel workbook using the `MoveTo` method of the Worksheet object. Just specify the index of the destination position in the target workbook.

#### Q. Does the supplied source code work with other Excel file formats, such as XLSX?

	 A. Yes, the provided source code works with other Excel file formats, including XLSX. Aspose.Cells for .NET supports a variety of Excel file formats, allowing you to manipulate and move worksheet into different file types.

#### Q. How can I specify the output file path and name when saving the modified Excel file?

	 A. When saving the modified Excel file, use the `Save` method of the Workbook object specifying the full path and name of the output file. Be sure to specify the appropriate file extension, such as `.xls` or `.xlsx`, depending on the desired file format.
