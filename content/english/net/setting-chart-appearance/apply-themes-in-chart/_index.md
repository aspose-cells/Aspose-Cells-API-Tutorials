---
title: Apply Themes in Chart
linktitle: Apply Themes in Chart
second_title: Aspose.Cells .NET Excel Processing API
description: 
type: docs
weight: 10
url: /net/setting-chart-appearance/apply-themes-in-chart/
---

## Complete Source Code
```csharp
using System;
using System.IO;

using Aspose.Cells;
using Aspose.Cells.Charts;

namespace Aspose.Cells.Examples.CSharp.Charts
{
    public class ApplyingThemesInChart
    {
        //Source directory
        static string sourceDir = "Your Document Directory";

        //Output directory
        static string outputDir = "Your Document Directory";

        public static void Run()
        {
            // Instantiate the workbook to open the file that contains a chart
            Workbook workbook = new Workbook(sourceDir + "sampleApplyingThemesInChart.xlsx");

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
            workbook.Save(outputDir + "outputApplyingThemesInChart.xlsx");

            Console.WriteLine("ApplyingThemesInChart executed successfully.");
        }
    }
}

```
