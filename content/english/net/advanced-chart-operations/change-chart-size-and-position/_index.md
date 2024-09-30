---
title: Change Chart Size and Position
linktitle: Change Chart Size and Position
second_title: Aspose.Cells .NET Excel Processing API
description: 
type: docs
weight: 11
url: /net/advanced-chart-operations/change-chart-size-and-position/
---

## Complete Source Code
```csharp
using System;
using System.IO;
using Aspose.Cells;
using Aspose.Cells.Charts;

namespace Aspose.Cells.Examples.CSharp.Charts
{
    public class ChangeChartSizeAndPosition
    {
        //Source directory
        static string sourceDir = "Your Document Directory";

        //Output directory
        static string outputDir = "Your Output Directory";

        public static void Run()
        {
            Workbook workbook = new Workbook(sourceDir + "sampleChangeChartSizeAndPosition.xlsx");

            Worksheet worksheet = workbook.Worksheets[0];

            // Load the chart from source worksheet
            Chart chart = worksheet.Charts[0];

            // Resize the chart
            chart.ChartObject.Width = 400;
            chart.ChartObject.Height = 300;

            // Reposition the chart
            chart.ChartObject.X = 250;
            chart.ChartObject.Y = 150;

            // Output the file
            workbook.Save(outputDir + "outputChangeChartSizeAndPosition.xlsx");

            Console.WriteLine("ChangeChartSizeAndPosition executed successfully.");
        }
    }
}

```
