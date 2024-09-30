---
title: Create Custom Chart
linktitle: Create Custom Chart
second_title: Aspose.Cells .NET Excel Processing API
description: 
type: docs
weight: 10
url: /net/manipulating-chart-types/create-custom-chart/
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
    public class HowToCreateCustomChart
    {
        //Output directory
        static string outputDir = "Your Document Directory";

        public static void Run()
        {
            // Instantiating a Workbook object
            Workbook workbook = new Workbook();

            // Obtaining the reference of the newly added worksheet by passing its sheet index
            Worksheet worksheet = workbook.Worksheets[0];

            // Adding sample values to cells
            worksheet.Cells["A1"].PutValue(50);
            worksheet.Cells["A2"].PutValue(100);
            worksheet.Cells["A3"].PutValue(150);
            worksheet.Cells["A4"].PutValue(110);
            worksheet.Cells["B1"].PutValue(260);
            worksheet.Cells["B2"].PutValue(12);
            worksheet.Cells["B3"].PutValue(50);
            worksheet.Cells["B4"].PutValue(100);

            // Adding a chart to the worksheet
            int chartIndex = worksheet.Charts.Add(Aspose.Cells.Charts.ChartType.Column, 5, 0, 25, 10);

            // Accessing the instance of the newly added chart
            Aspose.Cells.Charts.Chart chart = worksheet.Charts[chartIndex];

            // Adding NSeries (chart data source) to the chart ranging from "A1" cell to "B4"
            chart.NSeries.Add("A1:B4", true);

            // Setting the chart type of 2nd NSeries to display as line chart
            chart.NSeries[1].Type = Aspose.Cells.Charts.ChartType.Line;
                       
            // Saving the Excel file
            workbook.Save(outputDir + "outputHowToCreateCustomChart.xlsx");

            Console.WriteLine("HowToCreateCustomChart executed successfully.");
        }
    }
}

```
