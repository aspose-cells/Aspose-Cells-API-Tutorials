---
title: Adjust Compression Level
linktitle: Adjust Compression Level
second_title: Aspose.Cells for .NET API Reference
description: 
type: docs
weight: 50
url: /net/excel-workbook/adjust-compression-level/
---
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