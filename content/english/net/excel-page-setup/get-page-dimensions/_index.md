---
title: Get Page Dimensions
linktitle: Get Page Dimensions
second_title: Aspose.Cells for .NET API Reference
description: Learn how to retrieve page dimensions in Excel using Aspose.Cells for .NET. Step by step guide with source code in C#.
type: docs
weight: 40
url: /net/excel-page-setup/get-page-dimensions/
---
Aspose.Cells for .NET is a powerful library that allows developers to work with Microsoft Excel files programmatically. It offers a wide range of features for manipulating Excel documents, including the ability to get page dimensions. In this tutorial, we'll walk you through the steps to retrieve page dimensions using Aspose.Cells for .NET.

## Step 1: Create an instance of the Workbook class

To start, we need to create an instance of the Workbook class, which represents the Excel workbook. This can be achieved using the following code:

```csharp
Workbook book = new Workbook();
```

## Step 2: Accessing the spreadsheet

Next, we need to navigate to the worksheet in the workbook where we want to set the page dimensions. In this example, suppose we want to work with the first worksheet. We can access it using the following code:

```csharp
Worksheet sheet = book.Worksheets[0];
```

## Step 3: Set paper size to A2 and print width and height in inches

Now we will set the paper size to A2 and print the page width and height in inches. This can be achieved using the following code:

```csharp
sheet.PageSetup.PaperSize = PaperSizeType.PaperA2;
Console.WriteLine("A2: " + sheet.PageSetup.PaperWidth + "x" + sheet.PageSetup.PaperHeight);
```

## Step 4: Set paper size to A3 and print width and height in inches

Next, we'll set the paper size to A3 and print the page width and height in inches. Here is the corresponding code:

```csharp
sheet.PageSetup.PaperSize = PaperSizeType.PaperA3;
Console.WriteLine("A3: " + sheet.PageSetup.PaperWidth + "x" + sheet.PageSetup.PaperHeight);
```

## Step 5: Set paper size to A4 and print width and height in inches

We will now set the paper size to A4 and print the page width and height in inches. Here is the code:

```csharp
sheet.PageSetup.PaperSize = PaperSizeType.PaperA4;
Console.WriteLine("A4: " + sheet.PageSetup.PaperWidth + "x" + sheet.PageSetup.PaperHeight);
```

## Step 6: Set the paper size to Letter and print the width and height in inches

Finally, we'll set the paper size to Letter and print the page width and height in inches. Here is the code:

```csharp
sheet.PageSetup.PaperSize = PaperSizeType.PaperLetter;
Console.WriteLine("Letter: " + sheet.PageSetup.PaperWidth + "x" + sheet.PageSetup.PaperHeight);
```

### Sample source code for Get Page Dimensions using Aspose.Cells for .NET 
```csharp
// Create an instance of Workbook class
Workbook book = new Workbook();
// Access first worksheet
Worksheet sheet = book.Worksheets[0];
// Set paper size to A2 and print paper width and height in inches
sheet.PageSetup.PaperSize = PaperSizeType.PaperA2;
Console.WriteLine("PaperA2: " + sheet.PageSetup.PaperWidth + "x" + sheet.PageSetup.PaperHeight);
// Set paper size to A3 and print paper width and height in inches
sheet.PageSetup.PaperSize = PaperSizeType.PaperA3;
Console.WriteLine("PaperA3: " + sheet.PageSetup.PaperWidth + "x" + sheet.PageSetup.PaperHeight);
// Set paper size to A4 and print paper width and height in inches
sheet.PageSetup.PaperSize = PaperSizeType.PaperA4;
Console.WriteLine("PaperA4: " + sheet.PageSetup.PaperWidth + "x" + sheet.PageSetup.PaperHeight);
// Set paper size to Letter and print paper width and height in inches
sheet.PageSetup.PaperSize = PaperSizeType.PaperLetter;
Console.WriteLine("PaperLetter: " + sheet.PageSetup.PaperWidth + "x" + sheet.PageSetup.PaperHeight);
Console.WriteLine("GetPageDimensions executed successfully.\r\n");
```

## Conclusion

Congratulation ! You learned how to retrieve page dimensions using Aspose.Cells for .NET. This feature can be useful when you need to perform specific operations based on page dimensions in your Excel files.

Don't forget to further explore the documentation of Aspose.Cells to discover all the powerful features it offers.

### FAQ's

#### 1. What other paper sizes does Aspose.Cells for .NET support?

Aspose.Cells for .NET supports a variety of paper sizes including A1, A5, B4, B5, Executive, Legal, Letter and many more. You can check the documentation for the full list of supported paper sizes.

#### 2. Can I set custom page dimensions with Aspose.Cells for .NET?

Yes, you can set custom page dimensions by specifying the desired width and height. Aspose.Cells offers full flexibility to customize page dimensions to your needs.

#### 3. Can I get page dimensions in units other than inches?

Yes, Aspose.Cells for .NET allows you to get page dimensions in different units, including inches, centimeters, millimeters, and points.

#### 4. Does Aspose.Cells for .NET support other page settings editing features?

Yes, Aspose.Cells offers a full range of features for editing page settings, including setting margins, orientation, headers and footers, etc.
