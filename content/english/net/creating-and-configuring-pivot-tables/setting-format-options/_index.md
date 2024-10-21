---
title: Setting Format Options of Pivot Table in .NET
linktitle: Setting Format Options of Pivot Table in .NET
second_title: Aspose.Cells .NET Excel Processing API
description: 
type: docs
weight: 20
url: /net/creating-and-configuring-pivot-tables/setting-format-options/
---

## Complete Source Code
```csharp
using System.IO;

using Aspose.Cells;
using System.Drawing;
using Aspose.Cells.Pivot;

namespace Aspose.Cells.Examples.CSharp.PivotTableExamples
{
    public class SettingFormatOptions
    {
        public static void Run()
        {
            // ExStart:1
            // The path to the documents directory.
            string dataDir = RunExamples.GetDataDir(System.Reflection.MethodBase.GetCurrentMethod().DeclaringType);

            // Load a template file
            Workbook workbook = new Workbook(dataDir + "Book1.xls");

            // Get the first worksheet
            Worksheet worksheet = workbook.Worksheets[0];
            int pivotindex = 0;

            // Accessing the PivotTable
            PivotTable pivotTable = worksheet.PivotTables[pivotindex];

            // Setting the PivotTable report shows grand totals for rows.
            pivotTable.RowGrand = true;

            // Setting the PivotTable report shows grand totals for columns.
            pivotTable.ColumnGrand = true;

            // Setting the PivotTable report displays a custom string in cells that contain null values.
            pivotTable.DisplayNullString = true;
            pivotTable.NullString = "null";

            // Setting the PivotTable report's layout
            pivotTable.PageFieldOrder = PrintOrderType.DownThenOver;

            // Saving the Excel file
            workbook.Save(dataDir + "output.xls");

            // ExEnd:1

        }
    }
}
```
