---
title: Show Report Filter Pages Option in .NET
linktitle: Show Report Filter Pages Option in .NET
second_title: Aspose.Cells .NET Excel Processing API
description: 
type: docs
weight: 22
url: /net/creating-and-configuring-pivot-tables/show-report-filter-pages-option/
---

## Complete Source Code
```csharp
using System.IO;

using Aspose.Cells;
using System.Drawing;
using Aspose.Cells.Pivot;
using System;

namespace Aspose.Cells.Examples.CSharp.PivotTableExamples
{
    public class ShowReportFilterPagesOption
    {
        //Source directory
        static string sourceDir = "Your Document Directory";

        //Output directory
        static string outputDir = "Your Document Directory";

        public static void Main()
        {
            // ExStart:1
            // Load template file
            Workbook wb = new Workbook(sourceDir + "samplePivotTable.xlsx");

            // Get first pivot table in the worksheet
            PivotTable pt = wb.Worksheets[1].PivotTables[0];

            // Set pivot field
            pt.ShowReportFilterPage(pt.PageFields[0]);

            // Set position index for showing report filter pages
            pt.ShowReportFilterPageByIndex(pt.PageFields[0].Position);

            // Set the page field name
            pt.ShowReportFilterPageByName(pt.PageFields[0].Name);

            // Save the output file
            wb.Save(outputDir + "outputSamplePivotTable.xlsx");
            // ExEnd:1
            Console.WriteLine("ShowReportFilterPagesOption executed successfully.");
        }
    }
}
```
