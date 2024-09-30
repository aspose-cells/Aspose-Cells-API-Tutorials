---
title: Get Chart Subtitle for ODS File
linktitle: Get Chart Subtitle for ODS File
second_title: Aspose.Cells .NET Excel Processing API
description: 
type: docs
weight: 12
url: /net/working-with-chart-data/get-chart-subtitle-for-ods-file/
---

## Complete Source Code
```csharp
using System;
using Aspose.Cells.Charts;

namespace Aspose.Cells.Examples.CSharp.Charts
{
    public class GetChartSubTitleForODSFile
    {
        public static void Run()
        {
            // ExStart:1
            //Source directory
            string sourceDir = "Your Document Directory";
            // Load excel file containing charts
            Workbook workbook = new Workbook(sourceDir + "SampleChart.ods");

            // Access first worksheet
            Worksheet worksheet = workbook.Worksheets[0];

            // Access first chart inside the worksheet
            Chart chart = worksheet.Charts[0];

            Console.WriteLine("Chart Subtitle: " + chart.SubTitle.Text);
            // ExEnd:1

            Console.WriteLine("GetChartSubTitleForODSFile executed successfully.");
        }
    }
}

```
