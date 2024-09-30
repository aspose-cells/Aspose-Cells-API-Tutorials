---
title: Handle Automatic Units of Chart Axis like Microsoft Excel
linktitle: Handle Automatic Units of Chart Axis like Microsoft Excel
second_title: Aspose.Cells .NET Excel Processing API
description: 
type: docs
weight: 10
url: /net/customizing-chart-axes-and-units/handle-automatic-units-of-chart-axis-like-microsoft-excel/
---

## Complete Source Code
```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;

using Aspose.Cells;
using Aspose.Cells.Charts;

namespace Aspose.Cells.Examples.CSharp.Charts
{
    class HandleAutomaticUnitsOfChartAxisLikeMicrosoftExcel
    {
        //Source directory
        static string sourceDir = RunExamples.Get_SourceDirectory();

        //Output directory
        static string outputDir = RunExamples.Get_OutputDirectory();

        public static void Run()
        {
            //Load the sample Excel file
            Workbook wb = new Workbook(sourceDir + "sampleHandleAutomaticUnitsOfChartAxisLikeMicrosoftExcel.xlsx");

            //Access first worksheet
            Worksheet ws = wb.Worksheets[0];

            //Access first chart
            Chart ch = ws.Charts[0];

            //Render chart to pdf
            ch.ToPdf(outputDir + "outputHandleAutomaticUnitsOfChartAxisLikeMicrosoftExcel.pdf");

            Console.WriteLine("HandleAutomaticUnitsOfChartAxisLikeMicrosoftExcel executed successfully.");
        }
    }
}

```
