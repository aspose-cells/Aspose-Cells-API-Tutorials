---
title: Refresh and Calculate Items in Pivot Table  in .NET
linktitle: Refresh and Calculate Items in Pivot Table  in .NET
second_title: Aspose.Cells .NET Excel Processing API
description: 
type: docs
weight: 17
url: /net/creating-and-configuring-pivot-tables/refreshing-and-calculating-items/
---

## Complete Source Code
```csharp
using System.IO;
using Aspose.Cells.Pivot;
using Aspose.Cells;
using System.Drawing;

namespace Aspose.Cells.Examples.CSharp.PivotTableExamples
{
    public class RefreshAndCalculateItems
    {
        public static void Run()
        {
            // ExStart:1
            // The path to the documents directory.
            string dataDir = RunExamples.GetDataDir(System.Reflection.MethodBase.GetCurrentMethod().DeclaringType);

            // Load source excel file containing a pivot table having calculated items
            Workbook wb = new Workbook(dataDir + "sample.xlsx");

            // Access first worksheet
            Worksheet sheet = wb.Worksheets[0];

            // Change the value of cell D2
            sheet.Cells["D2"].PutValue(20);

            // Refresh and calculate all the pivot tables inside this sheet
            foreach (PivotTable pt in sheet.PivotTables)
            {
                pt.RefreshData();
                pt.CalculateData();
            }

            // Save the workbook in output pdf
            wb.Save(dataDir + "RefreshAndCalculateItems_out.pdf", SaveFormat.Pdf);
            // ExEnd:1

        }
    }
}
```
