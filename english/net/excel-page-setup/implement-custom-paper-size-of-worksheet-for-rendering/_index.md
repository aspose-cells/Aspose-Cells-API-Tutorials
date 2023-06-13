---
title: Implement Custom Paper Size Of Worksheet For Rendering
linktitle: Implement Custom Paper Size Of Worksheet For Rendering
second_title: Aspose.Cells for .NET API Reference
description: Step-by-step guide to implement custom worksheet size with Aspose.Cells for .NET. Set the dimensions, add a message and save as PDF.
type: docs
weight: 50
url: /net/excel-page-setup/implement-custom-paper-size-of-worksheet-for-rendering/
---
Implementing a custom size for your worksheet can be very useful when you want to create a PDF document with a specific size. In this tutorial, we'll learn how to use Aspose.Cells for .NET to set a custom size for a worksheet and then save the document as a PDF.

## Step 1: Creating the output folder

Before starting, you need to create an output folder where the generated PDF file will be saved. You can use whatever path you want for your output folder.

```csharp
// Output directories
string outputDir = "YOUR_OUTPUT_FOLDER";
```

Make sure you specify the correct path to your output folder.

## Step 2: Creating the Workbook object

To get started, you need to create a Workbook object using Aspose.Cells. This object represents your spreadsheet.

```csharp
// Create the Workbook object
Workbook wb = new Workbook();
```

## Step 3: Access to the first worksheet

After creating the Workbook object, you can access the first worksheet within it.

```csharp
// Access to the first worksheet
Worksheet ws = wb.Worksheets[0];
```

## Step 4: Setting custom worksheet size

Now you can set custom worksheet size using `CustomPaperSize(width, height)` method of PageSetup class.

```csharp
// Set custom worksheet size (in inches)
ws.PageSetup.CustomPaperSize(6, 4);
```

In this example, we've set the worksheet size to be 6 inches wide and 4 inches high.

## Step 5: Access to cell B4

After that, we can access a specific cell in the worksheet. In this case, we will access cell B4.

```csharp
// Access to cell B4
Cell b4 = ws.Cells["B4"];
```

## Step 6: Adding the message in cell B4

We can now add a message to cell B4 using the `PutValue(value)` method.

```csharp
// Add the message in cell B4
b4.PutValue("PDF page size: 6.00 x 4.00 inches");
```

In this example, we've added the message "PDF Page Size: 6.00" x 4.00" in cell B4.

## Step 7: Saving the worksheet in PDF format

Finally, we can save the worksheet in PDF format using the `Save(filePath)` method of the Workbook object.

```csharp
// Save the worksheet in PDF format
wb.Save(outputDir + "outputCustomPaperSize.pdf");
```

Specify the desired path to the generated PDF file, using the output folder created earlier.

### Sample source code for Implement Custom Paper Size Of Worksheet For Rendering using Aspose.Cells for .NET 
```csharp
//Output directory
string outputDir = "YOUR_OUTPUT_DIRECTORY";
//Create workbook object
Workbook wb = new Workbook();
//Access first worksheet
Worksheet ws = wb.Worksheets[0];
//Set custom paper size in unit of inches
ws.PageSetup.CustomPaperSize(6, 4);
//Access cell B4
Cell b4 = ws.Cells["B4"];
//Add the message in cell B4
b4.PutValue("Pdf Page Dimensions: 6.00 x 4.00 in");
//Save the workbook in pdf format
wb.Save(outputDir + "outputCustomPaperSize.pdf");
```

## Conclusions

In this tutorial, you learned how to implement custom size of a worksheet using Aspose.Cells for .NET. You can use these steps to set specific dimensions for your worksheets and then save the documents in PDF format. We hope this guide has been helpful in understanding the process of implementing a custom spreadsheet size.

### Frequently Asked Questions (FAQ)

**Question 1: Can I further customize the spreadsheet layout?**

Yes, Aspose.Cells offers many options to customize your worksheet layout. You can set custom dimensions, page orientation, margins, headers and footers, and much more.

**Question 2: What other output formats does Aspose.Cells support?**

Aspose.Cells supports many different output formats, including PDF, XLSX, XLS, CSV, HTML, TXT and many more. You can choose the desired output format according to your needs.