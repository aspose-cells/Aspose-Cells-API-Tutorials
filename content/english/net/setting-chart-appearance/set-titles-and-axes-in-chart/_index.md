---
title: Set Titles and Axes in Chart
linktitle: Set Titles and Axes in Chart
second_title: Aspose.Cells .NET Excel Processing API
description: 
type: docs
weight: 15
url: /net/setting-chart-appearance/set-titles-and-axes-in-chart/
---

## Complete Source Code
```csharp
using System;
using System.IO;

using Aspose.Cells;
using System.Drawing;

namespace Aspose.Cells.Examples.CSharp.Charts
{
    public class SettingTitlesAxes
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
            worksheet.Cells["B1"].PutValue(60);
            worksheet.Cells["B2"].PutValue(32);
            worksheet.Cells["B3"].PutValue(50);

            // Adding a chart to the worksheet
            int chartIndex = worksheet.Charts.Add(Aspose.Cells.Charts.ChartType.Column, 5, 0, 25, 10);

            // Accessing the instance of the newly added chart
            Aspose.Cells.Charts.Chart chart = worksheet.Charts[chartIndex];

            // Adding SeriesCollection (chart data source) to the chart ranging from "A1" cell to "B3"
            chart.NSeries.Add("A1:B3", true);

            // Setting the foreground color of the plot area
            chart.PlotArea.Area.ForegroundColor = Color.Blue;

            // Setting the foreground color of the chart area
            chart.ChartArea.Area.ForegroundColor = Color.Yellow;

            // Setting the foreground color of the 1st SeriesCollection area
            chart.NSeries[0].Area.ForegroundColor = Color.Red;

            // Setting the foreground color of the area of the 1st SeriesCollection point
            chart.NSeries[0].Points[0].Area.ForegroundColor = Color.Cyan;

            // Filling the area of the 2nd SeriesCollection with a gradient
            chart.NSeries[1].Area.FillFormat.SetOneColorGradient(Color.Lime, 1, Aspose.Cells.Drawing.GradientStyleType.Horizontal, 1);

            // Setting the title of a chart
            chart.Title.Text = "Title";

            // Setting the font color of the chart title to blue
            chart.Title.Font.Color = Color.Blue;

            // Setting the title of category axis of the chart
            chart.CategoryAxis.Title.Text = "Category";

            // Setting the title of value axis of the chart
            chart.ValueAxis.Title.Text = "Value";

            // Saving the Excel file
            workbook.Save(outputDir + "outputSettingTitlesAxes.xlsx");

            Console.WriteLine("SettingTitlesAxes executed successfully.");
        }
    }
}

```
