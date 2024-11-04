---
title: Adjust Compression Level in Workbook
linktitle: Adjust Compression Level in Workbook
second_title: Aspose.Cells .NET Excel Processing API
description: 
type: docs
weight: 14
url: /net/workbook-operations/adjust-compression-level/
---

## Complete Source Code
```csharp
using Aspose.Cells.Rendering;
using Aspose.Cells.WebExtensions;
using System;

namespace Aspose.Cells.Examples.CSharp._Workbook
{
    public class AdjustCompressionLevel
    {
        public static void Run()
        {
            // ExStart:1
            //Source directory
            string sourceDir = "Your Document Directory";
            string outDir = "Your Document Directory";

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
            // ExEnd:1

            Console.WriteLine("AdjustCompressionLevel executed successfully.");
        }
    }
}

```
