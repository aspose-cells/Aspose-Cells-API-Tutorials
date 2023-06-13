---
title: Determine If Paper Size Of Worksheet Is Automatic
linktitle: Determine If Paper Size Of Worksheet Is Automatic
second_title: Aspose.Cells for .NET API Reference
description: Learn how to determine if a spreadsheet's paper size is automatic with Aspose.Cells for .NET.
type: docs
weight: 20
url: /net/excel-page-setup/determine-if-paper-size-of-worksheet-is-automatic/
---
In this article, we will take you step by step to explain the following C# source code: Determine if the paper size of a worksheet is automatic using Aspose.Cells for .NET. We will use the Aspose.Cells library for .NET to perform this operation. Follow the steps below to determine if the paper size of a worksheet is automatic.

## Step 1: Loading workbooks
The first step is to load the workbooks. We will have two workbooks: one with automatic paper size disabled and the other with automatic paper size enabled. Here is the code to load the workbooks:

```csharp
// source directory
string sourceDir = "YOUR_SOURCE_DIR";
// Output directory
string outputDir = "YOUR_OUTPUT_DIRECTORY";

// Load the first workbook with automatic paper size disabled
Workbook wb1 = new Workbook(sourceDir + "samplePageSetupIsAutomaticPaperSize-False.xlsx");

// Load second workbook with auto paper size enabled
Workbook wb2 = new Workbook(sourceDir + "samplePageSetupIsAutomaticPaperSize-True.xlsx");
```

## Step 2: Accessing Spreadsheets
Now that we've loaded the workbooks, we need to access the worksheets so we can check the automatic paper size. We will go to the first worksheet of the two workbooks. Here is the code to access it:

```csharp
// Go to the first worksheet of the first workbook
Worksheet ws11 = wb1.Worksheets[0];

// Go to the first worksheet of the second workbook
Worksheet ws12 = wb2.Worksheets[0];
```

## Step 3: Check the automatic paper size
In this step, we will check if the worksheet paper size is automatic. We will use the `PageSetup.IsAutomaticPaperSize` property to get this information. We will then display the result. Here is the code for that:

```csharp
// Display the IsAutomaticPaperSize property of the first worksheet in the first workbook
Console.WriteLine("First worksheet in first workbook - IsAutomaticPaperSize: " + ws11.PageSetup.IsAutomaticPaperSize);

// Display the IsAutomaticPaperSize property of the first worksheet in the second workbook
Console.WriteLine("First worksheet of second workbook - IsAutomaticPaperSize: " + ws12.PageSetup.IsAutomaticPaperSize);

```

### Sample source code for Determine If Paper Size Of Worksheet Is Automatic using Aspose.Cells for .NET 
```csharp
//Source directory
string sourceDir = "YOUR_SOURCE_DIRECTORY";
//Output directory
string outputDir = "YOUR_OUTPUT_DIRECTORY";
//Load the first workbook having automatic paper size false
Workbook wb1 = new Workbook(sourceDir + "samplePageSetupIsAutomaticPaperSize-False.xlsx");
//Load the second workbook having automatic paper size true
Workbook wb2 = new Workbook(sourceDir + "samplePageSetupIsAutomaticPaperSize-True.xlsx");
//Access first worksheet of both workbooks
Worksheet ws11 = wb1.Worksheets[0];
Worksheet ws12 = wb2.Worksheets[0];
//Print the PageSetup.IsAutomaticPaperSize property of both worksheets
Console.WriteLine("First Worksheet of First Workbook - IsAutomaticPaperSize: " + ws11.PageSetup.IsAutomaticPaperSize);
Console.WriteLine("First Worksheet of Second Workbook - IsAutomaticPaperSize: " + ws12.PageSetup.IsAutomaticPaperSize);
Console.WriteLine();
Console.WriteLine("DetermineIfPaperSizeOfWorksheetIsAutomatic executed successfully.\r\n");
```


## Conclusion
In this article, we learned how to determine if the paper size of a worksheet is automatic using Aspose.Cells for .NET. We followed the following steps: loading the workbooks,

access to spreadsheets and automatic paper size checking. Now you can use this knowledge to determine if the paper size of your spreadsheets is automatic.

### FAQs

Q: How can I load workbooks with Aspose.Cells for .NET?
A: You can load workbooks using the Workbook class from the Aspose.Cells library. Use the Workbook.Load method to load a workbook from a file.

Q: Can I check the automatic paper size for other spreadsheets?
A: Yes, you can check the automatic paper size for any worksheet by accessing the PageSetup.IsAutomaticPaperSize property of the corresponding Worksheet object.

Q: How can I change the automatic paper size of a spreadsheet?
A: To change the automatic paper size of a worksheet, you can use the PageSetup.IsAutomaticPaperSize property and set it to the desired value (true or false).

Q: What other features does Aspose.Cells for .NET offer?
A: Aspose.Cells for .NET offers many features for working with spreadsheets, such as creating, modifying and converting workbooks, as well as manipulating data, formulas and formatting.
