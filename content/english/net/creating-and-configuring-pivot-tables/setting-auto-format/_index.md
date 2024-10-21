---
title: Setting Auto Format of Pivot Table Programmatically in .NET
linktitle: Setting Auto Format of Pivot Table Programmatically in .NET
second_title: Aspose.Cells .NET Excel Processing API
description: 
type: docs
weight: 18
url: /net/creating-and-configuring-pivot-tables/setting-auto-format/
---

## Complete Source Code
```csharp
using System.IO;

using Aspose.Cells;
using System.Drawing;
using Aspose.Cells.Pivot;

namespace Aspose.Cells.Examples.CSharp.PivotTableExamples
{
    public class SettingAutoFormat
    {
        public static void Run()
        {
            // ExStart:1
            // The path to the documents directory.
            string dataDir = RunExamples.GetDataDir(System.Reflection.MethodBase.GetCurrentMethod().DeclaringType);

            // Load a template file
            Workbook workbook = new Workbook(dataDir + "Book1.xls");

            int pivotindex = 0;

            // Get the first worksheet
            Worksheet worksheet = workbook.Worksheets[0];

            // Accessing the PivotTable
            PivotTable pivotTable = worksheet.PivotTables[pivotindex];

            // Setting the PivotTable report is automatically formatted
            pivotTable.IsAutoFormat = true;

            // Setting the PivotTable atuoformat type.
            pivotTable.AutoFormatType = Aspose.Cells.Pivot.PivotTableAutoFormatType.Report5;
            
            // Saving the Excel file
            workbook.Save(dataDir + "output.xls");

            // ExEnd:1

        }
    }
}
```
