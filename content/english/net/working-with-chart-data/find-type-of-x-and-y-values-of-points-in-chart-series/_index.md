---
title: Find Type of X and Y Values of Points in Chart Series
linktitle: Find Type of X and Y Values of Points in Chart Series
second_title: Aspose.Cells .NET Excel Processing API
description: 
type: docs
weight: 11
url: /net/working-with-chart-data/find-type-of-x-and-y-values-of-points-in-chart-series/
---

## Complete Source Code
```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;

using Aspose.Cells.Charts;

namespace Aspose.Cells.Examples.CSharp.Charts
{
    class FindTypeOfXandYValuesOfPointsInChartSeries
    { 
        //Source directory
        static string sourceDir = RunExamples.Get_SourceDirectory();

        public static void Main()
        {
            //Load sample Excel file containing chart.
            Workbook wb = new Workbook(sourceDir + "sampleFindTypeOfXandYValuesOfPointsInChartSeries.xlsx");

            //Access first worksheet.
            Worksheet ws = wb.Worksheets[0];

            //Access first chart.
            Chart ch = ws.Charts[0];

            //Calculate chart data.
            ch.Calculate();

            //Access first chart point in the first series.
            ChartPoint pnt = ch.NSeries[0].Points[0];

            //Print the types of X and Y values of chart point.
            Console.WriteLine("X Value Type: " + pnt.XValueType);
            Console.WriteLine("Y Value Type: " + pnt.YValueType);

            Console.WriteLine("FindTypeOfXandYValuesOfPointsInChartSeries executed successfully.");
        }
    }
}

```
