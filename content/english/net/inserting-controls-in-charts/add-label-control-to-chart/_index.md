---
title: Add Label Control to Chart
linktitle: Add Label Control to Chart
second_title: Aspose.Cells .NET Excel Processing API
description: 
type: docs
weight: 10
url: /net/inserting-controls-in-charts/add-label-control-to-chart/
---

## Complete Source Code
```csharp
using System;
using System.IO;

using Aspose.Cells;
using System.Drawing;

namespace Aspose.Cells.Examples.CSharp.Charts
{
    public class AddingLabelControlInChart
    {
        //Source directory
        static string sourceDir = "Your Document Directory";

        //Output directory
        static string outputDir = "Your Document Directory";

        public static void Run()
        {
            // Open the existing file.
            Workbook workbook = new Workbook(sourceDir + "sampleAddingLabelControlInChart.xls");

            // Get the designer chart in the second sheet.
            Worksheet sheet = workbook.Worksheets[0];
            Aspose.Cells.Charts.Chart chart = sheet.Charts[0];

            // Add a new label to the chart.
            Aspose.Cells.Drawing.Label label = chart.Shapes.AddLabelInChart(600, 600, 350, 900);

            // Set the caption of the label.
            label.Text = "A Label In Chart";

            // Set the Placement Type, the way the
            // Label is attached to the cells.
            label.Placement = Aspose.Cells.Drawing.PlacementType.FreeFloating;            

            // Save the excel file.
            workbook.Save(outputDir + "outputAddingLabelControlInChart.xls");

            Console.WriteLine("AddingLabelControlInChart executed successfully.");
        }
    }
}

```
