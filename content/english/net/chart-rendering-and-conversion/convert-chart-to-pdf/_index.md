---
title: Convert Chart to PDF
linktitle: Convert Chart to PDF
second_title: Aspose.Cells .NET Excel Processing API
description: 
type: docs
weight: 11
url: /net/chart-rendering-and-conversion/convert-chart-to-pdf/
---

## Complete Source Code
```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using Aspose.Cells.Charts;
using System.IO;

namespace Aspose.Cells.Examples.CSharp.Charts
{
    public class ChartToPdf
    {
        //Source directory
        static string sourceDir = RunExamples.Get_SourceDirectory();

        //Output directory
        static string outputDir = RunExamples.Get_OutputDirectory();

        public static void Run()
        {
            // Load excel file containing charts
            Workbook workbook = new Workbook(sourceDir + "sampleChartToPdf.xlsx");

            // Access first worksheet
            Worksheet worksheet = workbook.Worksheets[0];

            // Access first chart inside the worksheet
            Chart chart = worksheet.Charts[0];

            // Save the chart into pdf format
            chart.ToPdf(outputDir + "outputChartToPdf.pdf");

            // Save the chart into pdf format in stream
            MemoryStream ms = new MemoryStream();
            chart.ToPdf(ms);

            Console.WriteLine("ChartToPdf executed successfully.");
        }
    }
}

```
