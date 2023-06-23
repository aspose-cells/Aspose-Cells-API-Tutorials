---
title: Copy Page Setup Settings From Other Worksheet
linktitle: Copy Page Setup Settings From Other Worksheet
second_title: Aspose.Cells for .NET API Reference
description: Learn how to copy page configuration settings from one spreadsheet to another using Aspose.Cells for .NET. A step-by-step guide to optimizing the use of this library.
type: docs
weight: 10
url: /net/excel-page-setup/copy-page-setup-settings-from-other-worksheet/
---
In this article, we will take you step by step to explain the following C# source code: Copy page configuration settings from another spreadsheet using Aspose.Cells for .NET. We will use the Aspose.Cells library for .NET to perform this operation. If you want to copy page setup settings from one worksheet to another, follow the steps below.

## Step 1: Creating the Workbook
The first step is to create a workbook. In our case, we will use the Workbook class provided by the Aspose.Cells library. Here is the code to create a workbook:

```csharp
Workbook wb = new Workbook();
```

## Step 2: Adding Test Worksheets
After creating the workbook, we need to add test worksheets. In this example, we will add two worksheets. Here is the code to add two worksheets:

```csharp
wb.Worksheets.Add("TestSheet1");
wb.Worksheets.Add("TestSheet2");
```

## Step 3: Accessing Worksheets
Now that we've added the worksheets, we need to access them to be able to change their settings. We will access the "TestSheet1" and "TestSheet2" worksheets using their names. Here is the code to access it:

```csharp
Worksheet TestSheet1 = wb. Worksheets["TestSheet1"];
Worksheet TestSheet2 = wb. Worksheets["TestSheet2"];
```

## Step 4: Setting Paper Size
In this step, we will set the paper size of the "TestSheet1" worksheet. We will use the `PageSetup.PaperSize` property to set the paper size. For example, we will set the paper size to "PaperA3ExtraTransverse". Here is the code for that:

```csharp
TestSheet1.PageSetup.PaperSize = PaperSizeType.PaperA3ExtraTransverse;
```

## Step 5: Copying Page Setup Settings
Now we will copy the page configuration settings from the "TestSheet1" worksheet to "TestSheet2". We will use the `PageSetup.Copy` method to perform this operation. Here is the code for that:

```csharp
TestSheet2.PageSetup.Copy(TestSheet1.PageSetup, new CopyOptions());
```

## Step 6: Printing Paper Sizes
After copying the page setup settings, we will print the paper sizes of the two worksheets. We will use `Console.WriteLine` to display the paper sizes. Here is the code for that:

```csharp
Console.WriteLine("Before Paper Size: " + TestSheet1.PageSetup.PaperSize);
Console.WriteLine("Before Paper Size: " + TestSheet2.PageSetup.PaperSize);
```

### Sample source code for Copy Page Setup Settings From Other Worksheet using Aspose.Cells for .NET 
```csharp
//Create workbook
Workbook wb = new Workbook();
//Add two test worksheets
wb.Worksheets.Add("TestSheet1");
wb.Worksheets.Add("TestSheet2");
//Access both worksheets as TestSheet1 and TestSheet2
Worksheet TestSheet1 = wb.Worksheets["TestSheet1"];
Worksheet TestSheet2 = wb.Worksheets["TestSheet2"];
//Set the Paper Size of TestSheet1 to PaperA3ExtraTransverse
TestSheet1.PageSetup.PaperSize = PaperSizeType.PaperA3ExtraTransverse;
//Print the Paper Size of both worksheets
Console.WriteLine("Before Paper Size: " + TestSheet1.PageSetup.PaperSize);
Console.WriteLine("Before Paper Size: " + TestSheet2.PageSetup.PaperSize);
Console.WriteLine();
//Copy the PageSetup from TestSheet1 to TestSheet2
TestSheet2.PageSetup.Copy(TestSheet1.PageSetup, new CopyOptions());
//Print the Paper Size of both worksheets
Console.WriteLine("After Paper Size: " + TestSheet1.PageSetup.PaperSize);
Console.WriteLine("After Paper Size: " + TestSheet2.PageSetup.PaperSize);
Console.WriteLine();
Console.WriteLine("CopyPageSetupSettingsFromSourceWorksheetToDestinationWorksheet executed successfully.\r\n");
```

## Conclusion
In this article, we learned how to copy page configuration settings from one worksheet to another using Aspose.Cells for .NET. We went through the following steps: creating the workbook, adding test worksheets, accessing the worksheets, setting the paper size, copying the page setup settings, and printing paper sizes. Now you can use this knowledge to copy page configuration settings into your own projects.

### FAQs

#### Q: Can I copy page configuration settings between different workbook instances?

A: Yes, you can copy page setup settings between different workbook instances using the `PageSetup.Copy` method of the Aspose.Cells library.

#### Q: Can I copy other page setup settings, like orientation or margins?

A: Yes, you can copy other page setup settings using the `PageSetup.Copy` method with the appropriate options. For example, you can copy orientation using `CopyOptions.Orientation` and margins using `CopyOptions.Margins`.

#### Q: How do I know what options are available for paper size?

A: You can check the Aspose.Cells library API Reference for available options for paper size. There is an enum called `PaperSizeType` which lists the different supported paper sizes.

#### Q: How can I download the Aspose.Cells library for .NET?

A: You can download Aspose.Cells library for .NET from [Aspose Releases](https://releases.aspose.com/cells/net). There are free trial versions available, as well as paid licenses for commercial use.

#### Q: Does the Aspose.Cells library support other programming languages?

A: Yes, the Aspose.Cells library supports multiple programming languages including C#, Java, Python, and many more.