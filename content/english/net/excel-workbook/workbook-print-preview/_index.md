---
title: Workbook Print Preview
linktitle: Workbook Print Preview
second_title: Aspose.Cells for .NET API Reference
description: Learn how to generate a print preview of a workbook using Aspose.Cells for .NET.
type: docs
weight: 170
url: /net/excel-workbook/workbook-print-preview/
---
Print preview of a Workbook is an essential feature when working with Excel files with Aspose.Cells for .NET. You can easily generate a print preview by following these steps:

## Step 1: Specify source directory

First, you need to specify the source directory where the Excel file you want to preview is located. Here's how to do it:

```csharp
// source directory
string sourceDir = RunExamples.Get_SourceDirectory();
```

## Step 2: Load the Workbook

Then you need to load the Workbook workbook from the specified Excel file. Here's how to do it:

```csharp
// Load the Workbook workbook
Workbook workbook = new Workbook(sourceDir + "Book1.xlsx");
```

## Step 3: Configure image and print options

Before generating the print preview, you can configure the image and print options as needed. In this example, we are using the default options. Here's how to do it:

```csharp
// Image and print options
ImageOrPrintOptions imgOptions = new ImageOrPrintOptions();
```

## Step 4: Generate the print preview of the workbook

Now you can generate the print preview of Workbook workbook by using WorkbookPrintingPreview class. Here's how to do it:

```csharp
// Print preview of the workbook
WorkbookPrintingPreview preview = new WorkbookPrintingPreview(workbook, imgOptions);
Console.WriteLine("Workbook page count: " + preview.EvaluatedPageCount);
```

## Step 5: Generate the print preview of the worksheet

If you want to generate the print preview of a specific worksheet, you can use the SheetPrintingPreview class. Here is an example :

```csharp
// Print preview of the worksheet
SheetPrintingPreview preview2 = new SheetPrintingPreview(workbook.Worksheets[0], imgOptions);
Console.WriteLine("Number of worksheet pages: " + preview2.EvaluatedPageCount);
```

### Sample source code for Workbook Print Preview using Aspose.Cells for .NET 
```csharp
//Source directory
string sourceDir = RunExamples.Get_SourceDirectory();
Workbook workbook = new Workbook(sourceDir + "Book1.xlsx");
ImageOrPrintOptions imgOptions = new ImageOrPrintOptions();
WorkbookPrintingPreview preview = new WorkbookPrintingPreview(workbook, imgOptions);
Console.WriteLine("Workbook page count: " + preview.EvaluatedPageCount);
SheetPrintingPreview preview2 = new SheetPrintingPreview(workbook.Worksheets[0], imgOptions);
Console.WriteLine("Worksheet page count: " + preview2.EvaluatedPageCount);
Console.WriteLine("PrintPreview executed successfully.");
```

## Conclusion

Generating the print preview of a workbook is a powerful feature offered by Aspose.Cells for .NET. By following the steps given above, you can easily preview your Excel workbook and get information about the number of pages to print.

### FAQs

#### Q: How can I specify a different source directory to load my Workbook?
    
A: You can use the `Set_SourceDirectory` method to specify a different source directory. For example: `RunExamples.Set_SourceDirectory("Path_to_the_source_directory")`.

#### Q: Can I customize the image and print options when generating the print preview?
    
A: Yes, you can customize image and print options by changing the properties of the `ImageOrPrintOptions` object. For example, you can set image resolution, output file format, etc.

#### Q: Is it possible to generate a print preview for multiple worksheets in a Workbook?
    
A: Yes, you can iterate over the different worksheets in the Workbook and generate a print preview for each sheet using the `SheetPrintingPreview` class.

#### Q: How do I save the print preview as an image or PDF file?
    
A: You can use `ToImage` or `ToPdf` method of `WorkbookPrintingPreview` or `SheetPrintingPreview` object to save print preview as image or PDF file.

#### Q: What can I do with the print preview once generated?
    
A: Once you have generated the print preview, you can view it on screen, save it as an image or PDF file, or use it for other operations such as sending by email or print.
	