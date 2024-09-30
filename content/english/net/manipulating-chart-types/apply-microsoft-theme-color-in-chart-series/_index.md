---
title: Apply Microsoft Theme Color in Chart Series
linktitle: Apply Microsoft Theme Color in Chart Series
second_title: Aspose.Cells .NET Excel Processing API
description: 
type: docs
weight: 14
url: /net/manipulating-chart-types/apply-microsoft-theme-color-in-chart-series/
---

## Complete Source Code
```csharp
using System;
using System.IO;

using Aspose.Cells;
using Aspose.Cells.Drawing;
using System.Drawing;
using Aspose.Cells.Charts;

namespace Aspose.Cells.Examples.CSharp.Charts
{
    public class MicrosoftThemeColorInChartSeries
    {
        //Source directory
        static string sourceDir = "Your Document Directory";

        //Output directory
        static string outputDir = "Your Document Directory";

        public static void Run()
        {                       
            // Instantiate the workbook to open the file that contains a chart
            Workbook workbook = new Workbook(sourceDir + "sampleMicrosoftThemeColorInChartSeries.xlsx");

            // Get the first worksheet
            Worksheet worksheet = workbook.Worksheets[0];

            // Get the first chart in the sheet
            Chart chart = worksheet.Charts[0];

            // Specify the FilFormat's type to Solid Fill of the first series
            chart.NSeries[0].Area.FillFormat.FillType = Aspose.Cells.Drawing.FillType.Solid;

            // Get the CellsColor of SolidFill
            CellsColor cc = chart.NSeries[0].Area.FillFormat.SolidFill.CellsColor;

            // Create a theme in Accent style
            cc.ThemeColor = new ThemeColor(ThemeColorType.Accent6, 0.6);

            // Apply the them to the series
            chart.NSeries[0].Area.FillFormat.SolidFill.CellsColor = cc;

            // Save the Excel file
            workbook.Save(outputDir + "outputMicrosoftThemeColorInChartSeries.xlsx");

            Console.WriteLine("MicrosoftThemeColorInChartSeries executed successfully.");
        }
    }
}

```
