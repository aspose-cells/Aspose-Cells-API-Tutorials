---
title: Pivot Table Data Display Format Ranking in .NET
linktitle: Pivot Table Data Display Format Ranking in .NET
second_title: Aspose.Cells .NET Excel Processing API
description: 
type: docs
weight: 30
url: /net/creating-and-configuring-pivot-tables/pivot-table-data-display-format-ranking/
---

## Complete Source Code
```csharp
using System;
using Aspose.Cells.Pivot;

namespace Aspose.Cells.Examples.CSharp.PivotTables
{
    class PivotTableDataDisplayFormatRanking
    {
        public static void Run()
        {
            // ExStart:1
            // directories
            string sourceDir = "Your Document Directory";
            string outputDir = "Your Document Directory";

            // Load a template file
            Workbook workbook = new Workbook(sourceDir + "PivotTableSample.xlsx");

            // Get the first worksheet
            Worksheet worksheet = workbook.Worksheets[0];
            int pivotIndex = 0;

            // Accessing the PivotTable
            PivotTable pivotTable = worksheet.PivotTables[pivotIndex];
            // Accessing the data fields.
            PivotFieldCollection pivotFields = pivotTable.DataFields;

            // Accessing the first data field in the data fields.
            PivotField pivotField = pivotFields[0];

            // Setting data display format
            pivotField.DataDisplayFormat = PivotFieldDataDisplayFormat.RankLargestToSmallest;

            pivotTable.CalculateData();
            // Saving the Excel file
            workbook.Save(outputDir + "PivotTableDataDisplayFormatRanking_out.xlsx");
            // ExEnd:1

            Console.WriteLine("PivotTableDataDisplayFormatRanking executed successfully.");
        }
    }
}

```
