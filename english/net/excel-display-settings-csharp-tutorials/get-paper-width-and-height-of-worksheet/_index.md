---
title: Get Paper Width And Height Of Worksheet
linktitle: Get Paper Width And Height Of Worksheet
second_title: Aspose.Cells for .NET API Reference
description: Create a step by step guide to explain the following C# source code to get the paper width and height of a spreadsheet using Aspose.Cells for .NET.
type: docs
weight: 80
url: /net/excel-display-settings-csharp-tutorials/get-paper-width-and-height-of-worksheet/
---
In this tutorial, we will take you step by step to explain the following C# source code to get the paper width and height of a worksheet using Aspose.Cells for .NET. Follow the steps below:

## Step 1: Create the workbook
Start by creating a new workbook using the `Workbook` class:

```csharp
Workbook wb = new Workbook();
```

## Step 2: Access the first worksheet
Next, navigate to the first worksheet in the workbook using the `Worksheet` class:

```csharp
Worksheet ws = wb.Worksheets[0];
```

## Step 3: Set paper size to A2 and show paper width and height in inches
Use the `PaperSize` property of the `PageSetup` object to set the paper size to A2, then use the `PaperWidth` and `PaperHeight` properties to get the paper width and height respectively. Display these values using the `Console.WriteLine` method:

```csharp
ws.PageSetup.PaperSize = PaperSizeType.PaperA2;
Console.WriteLine("PaperA2: " + ws.PageSetup.PaperWidth + "x" + ws.PageSetup.PaperHeight);
```

## Step 4: Repeat steps for other paper sizes
Repeat the previous steps, changing the paper size to A3, A4, and Letter, then displaying the paper width and height values for each size:

```csharp
ws.PageSetup.PaperSize = PaperSizeType.PaperA3;
Console.WriteLine("PaperA3: " + ws.PageSetup.PaperWidth + "x" + ws.PageSetup.PaperHeight);

ws.PageSetup.PaperSize = PaperSizeType.PaperA4;
Console.WriteLine("PaperA4: " + ws.PageSetup.PaperWidth + "x" + ws.PageSetup.PaperHeight);

ws.PageSetup.PaperSize = PaperSizeType.PaperLetter;
Console.WriteLine("PaperLetter: " + ws.PageSetup.PaperWidth + "x" + ws.PageSetup.PaperHeight);
```

### Sample source code for Get Paper Width And Height Of Worksheet using Aspose.Cells for .NET 

```csharp
//Create workbook
Workbook wb = new Workbook();
//Access first worksheet
Worksheet ws = wb.Worksheets[0];
//Set paper size to A2 and print paper width and height in inches
ws.PageSetup.PaperSize = PaperSizeType.PaperA2;
Console.WriteLine("PaperA2: " + ws.PageSetup.PaperWidth + "x" + ws.PageSetup.PaperHeight);
//Set paper size to A3 and print paper width and height in inches
ws.PageSetup.PaperSize = PaperSizeType.PaperA3;
Console.WriteLine("PaperA3: " + ws.PageSetup.PaperWidth + "x" + ws.PageSetup.PaperHeight);
//Set paper size to A4 and print paper width and height in inches
ws.PageSetup.PaperSize = PaperSizeType.PaperA4;
Console.WriteLine("PaperA4: " + ws.PageSetup.PaperWidth + "x" + ws.PageSetup.PaperHeight);
//Set paper size to Letter and print paper width and height in inches
ws.PageSetup.PaperSize = PaperSizeType.PaperLetter;
Console.WriteLine("PaperLetter: " + ws.PageSetup.PaperWidth + "x" + ws.PageSetup.PaperHeight);
```


## Conclusion

You learned how to use Aspose.Cells for .NET to get the paper width and height of a spreadsheet. This feature can be useful for the configuration and precise layout of your Excel documents.

## Frequently Asked Questions (FAQ)

**What is Aspose.Cells for .NET?**

Aspose.Cells for .NET is a powerful library for manipulating and processing Excel files in .NET applications. It offers many features for creating, modifying, converting and analyzing Excel files.

**How can I get the paper size of a spreadsheet with Aspose.Cells for .NET?**

You can use the `PageSetup` class of the `Worksheet` object to access the paper size. Use the `PaperSize` property to set the paper size and the `PaperWidth` and `PaperHeight` properties to get the paper width and height respectively.

**What paper sizes does Aspose.Cells for .NET support?**

Aspose.Cells for .NET supports a wide range of commonly used paper sizes, such as A2, A3, A4, and Letter, as well as many other custom sizes.

**Can I customize the paper size of a spreadsheet with Aspose.Cells for .NET?**

Yes, you can set a custom paper size by specifying the exact width and height dimensions using the `PaperWidth` and `PaperHeight` properties of the `PageSetup` class.

**How can I download Aspose.Cells for .NET?**

You can download Aspose.Cells for .NET from Aspose official website at: [https://www.aspose.com/en/cells/net](https://www.aspose .com/fr/cells/net)

**Is there any sample code and documentation for using Aspose.Cells for .NET?**

Yes, Aspose.Cells for .NET has extensive documentation and many code examples available on the Aspose site. You can consult the documentation and examples to learn how to use all the features offered by the library.