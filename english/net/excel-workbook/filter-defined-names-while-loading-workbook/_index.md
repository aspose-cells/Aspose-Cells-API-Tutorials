---
title: Filter Defined Names While Loading Workbook
linktitle: Filter Defined Names While Loading Workbook
second_title: Aspose.Cells for .NET API Reference
description: Learn how to filter defined names when loading an Excel workbook with Aspose.Cells for .NET.
type: docs
weight: 100
url: /net/excel-workbook/filter-defined-names-while-loading-workbook/
---
When working with Excel workbooks in a .NET application, it is often necessary to filter data on load. Aspose.Cells for .NET is a powerful library to easily manipulate Excel workbooks. In this guide, we will show you how to filter the names defined when loading a workbook using Aspose.Cells for .NET. Follow these simple steps to get the desired results:

## Step 1: Specify loading options

First, you need to specify the loading options to define the loading behavior of the workbook. In our case, we want to ignore the names set on load. Here's how to do it using Aspose.Cells:

```csharp
// Specifies loading options
LoadOptions opts = new LoadOptions();

// Don't load defined names
opts. LoadFilter = new LoadFilter(~LoadDataFilterOptions.DefinedNames);
```

## Step 2: Load the workbook

Once the load options are configured, you can load the Excel workbook from the source file. Be sure to specify the correct file path. Here is a sample code:

```csharp
// Load the workbook
Workbook wb = new Workbook(sourceDir + "sampleFilterDefinedNamesWhileLoadingWorkbook.xlsx", opts);
```

## Step 3: Save the filtered workbook

After loading the workbook, you can perform other operations or edits as needed. Then you can save the filtered workbook to an output file. Here's how:

```csharp
// Save the filtered Excel workbook
wb.Save(outputDir + "outputFilterDefinedNamesWhileLoadingWorkbook.xlsx");
```

### Sample source code for Filter Defined Names While Loading Workbook using Aspose.Cells for .NET 
```csharp
//Specify the load options
LoadOptions opts = new LoadOptions();
//We do not want to load defined names
opts.LoadFilter = new LoadFilter(~LoadDataFilterOptions.DefinedNames);
//Load the workbook
Workbook wb = new Workbook(sourceDir + "sampleFilterDefinedNamesWhileLoadingWorkbook.xlsx", opts);
//Save the output Excel file, it will break the formula in C1
wb.Save(outputDir + "outputFilterDefinedNamesWhileLoadingWorkbook.xlsx");
Console.WriteLine("FilterDefinedNamesWhileLoadingWorkbook executed successfully.");
```

## Conclusion

Filtering defined names when loading an Excel workbook can be critical for many applications. Aspose.Cells for .NET makes this task easier by providing flexible options for loading and filtering data. By following the steps in this guide, you will be able to effectively filter out the defined names and achieve the desired results in your Excel workbooks.


### FAQs

#### Q: Does Aspose.Cells support other programming languages besides C#?
    
A: Yes, Aspose.Cells is a cross-platform library that supports many programming languages such as Java, Python, C++, and many more.

#### Q: Can I filter other data types when loading a workbook with Aspose.Cells?
    
A: Yes, Aspose.Cells offers a range of filtering options for data including formulas, styles, macros, etc.

#### Q: Does Aspose.Cells retain the formatting and properties of the original workbook?
    
A: Yes, Aspose.Cells retains formatting, styles, formulas and other properties of the original workbook when working with Excel files.
