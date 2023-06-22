---
title: Adjust Compression Level
linktitle: Adjust Compression Level
second_title: Aspose.Cells for .NET API Reference
description: Reduce the size of your Excel workbooks by adjusting the compression level with Aspose.Cells for .NET.
type: docs
weight: 50
url: /net/excel-workbook/adjust-compression-level/
---
In this step-by-step tutorial, we will explain the provided C# source code that will allow you to adjust the compression level using Aspose.Cells for .NET. Follow the steps below to adjust the compression level in your Excel workbook.

## Step 1: Set source and output directories

```csharp
// source directory
string sourceDir = RunExamples.Get_SourceDirectory();
// Output directory
string outDir = RunExamples.Get_OutputDirectory();
```

In this first step, we define the source and output directories for the Excel files.

## Step 2: Load Excel Workbook

```csharp
// Load the Excel workbook
Workbook workbook = new Workbook(sourceDir + "LargeSampleFile.xlsx");
```

We load the Excel workbook from the specified file using the `Workbook` class from Aspose.Cells.

## Step 3: Set backup options

```csharp
// Define backup options
XlsbSaveOptions options = new XlsbSaveOptions();
```

We create an instance of the `XlsbSaveOptions` class to set save options.

## Step 4: Adjust the compression level (Level 1)

```csharp
// Adjust the compression level (Level 1)
options.CompressionType = OoxmlCompressionType.Level1;
var watch = System.Diagnostics.Stopwatch.StartNew();
workbook.Save(outDir + "LargeSampleFile_level_1_out.xlsb", options);
watch.Stop();
let elapsedMs = watch.ElapsedMilliseconds;
Console.WriteLine("Elapsed time (Level 1): " + elapsedMs);
```

We adjust the compression level by setting `CompressionType` to `Level1`. Then we save the Excel workbook with this compression option specified.

## Step 5: Adjust the compression level (Level 6)

```csharp
// Adjust the compression level (Level 6)
options.CompressionType = OoxmlCompressionType.Level6;
watch = System.Diagnostics.Stopwatch.StartNew();
workbook.Save(outDir + "LargeSampleFile_level_6_out.xlsb", options);
watch.Stop();
elapsedMs = watch. ElapsedMilliseconds;
Console.WriteLine("Elapsed time (Level 6): " + elapsedMs);
```

We repeat the process to adjust the compression level to `Level6` and save the Excel workbook with this option.

## Step 6: Adjust the compression level (Level 9)

```csharp
// Adjust the compression level (Level 9)
options.CompressionType = OoxmlCompressionType.Level9;
watch = System.Diagnostics.Stopwatch.StartNew();
workbook.Save(outDir + "LargeSampleFile_level_9_out.xlsb", options);
watch.Stop();
elapsedMs = watch. ElapsedMilliseconds;
Console.WriteLine("Elapsed time (Level 9): " + elapsedMs);
```

We repeat the process one last time to adjust the compression level to `Level9` and save the Excel workbook with this option.

### Sample source code for Adjust Compression Level using Aspose.Cells for .NET 
```csharp
//Source directory
string sourceDir = RunExamples.Get_SourceDirectory();
string outDir = RunExamples.Get_OutputDirectory();
Workbook workbook = new Workbook(sourceDir + "LargeSampleFile.xlsx");
XlsbSaveOptions options = new XlsbSaveOptions();
options.CompressionType = OoxmlCompressionType.Level1;
var watch = System.Diagnostics.Stopwatch.StartNew();
workbook.Save(outDir + "LargeSampleFile_level_1_out.xlsb", options);
watch.Stop();
var elapsedMs = watch.ElapsedMilliseconds;
Console.WriteLine("Level 1 Elapsed Time: " + elapsedMs);
watch = System.Diagnostics.Stopwatch.StartNew();
options.CompressionType = OoxmlCompressionType.Level6;
workbook.Save(outDir + "LargeSampleFile_level_6_out.xlsb", options);
watch.Stop();
elapsedMs = watch.ElapsedMilliseconds;
Console.WriteLine("Level 6 Elapsed Time: " + elapsedMs);
watch = System.Diagnostics.Stopwatch.StartNew();
options.CompressionType = OoxmlCompressionType.Level9;
workbook.Save(outDir + "LargeSampleFile_level_9_out.xlsb", options);
watch.Stop();
elapsedMs = watch.ElapsedMilliseconds;
Console.WriteLine("Level 9 Elapsed Time: " + elapsedMs);
Console.WriteLine("AdjustCompressionLevel executed successfully.");
```

## Conclusion

Congratulation ! You learned how to adjust the compression level in an Excel workbook using Aspose.Cells for .NET. Experiment with different levels of compression to find the one that best suits your needs.

### FAQs

#### Q: What is compression in an Excel workbook?

	 A: Compression in an Excel workbook is a process of reducing file size by using compression algorithms. This reduces the storage space required and improves performance when loading and manipulating the file.

#### Q: What levels of compression are available with Aspose.Cells?

	 A: With Aspose.Cells, you can adjust the compression level from 1 to 9. The higher the compression level, the smaller the file size will be, but it can also increase processing time.

#### Q: How do I choose the right compression level for my Excel workbook?

	 A: The choice of compression level depends on your specific needs. If you want maximum compression and processing time is not an issue, you can go for level 9. If you prefer a compromise between file size and processing time, you can choose an intermediate level.

#### Q: Does compression affect data quality in Excel workbook?

	 A: No, the compression does not affect the data quality in the Excel workbook. It simply reduces the file size using compression techniques without altering the data itself.

#### Q: Can I adjust the compression level after saving the Excel file?

	 A: No, once you save the Excel file with a specific compression level, you cannot adjust the compression level later. You will need to save the file again with the new compression level if you wish to modify it.