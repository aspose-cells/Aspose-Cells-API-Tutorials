---
title: Saving Pivot Tables with Custom Sort and Hide in .NET
linktitle: Saving Pivot Tables with Custom Sort and Hide in .NET
second_title: Aspose.Cells .NET Excel Processing API
description: 
type: docs
weight: 26
url: /net/creating-and-configuring-pivot-tables/saving-with-custom-sort-and-hide/
---

## Complete Source Code
```csharp
using System;
using Aspose.Cells.Pivot;

namespace Aspose.Cells.Examples.CSharp.PivotTables
{
    class PivotTableSortAndHide
    {
        public static void Run()
        {
            // ExStart:1
            // directories
            string sourceDir = "Your Document Directory";
            string outputDir = "Your Document Directory";

            Workbook workbook = new Workbook(sourceDir + "PivotTableHideAndSortSample.xlsx");

            Worksheet worksheet = workbook.Worksheets[0];

            var pivotTable = worksheet.PivotTables[0];
            var dataBodyRange = pivotTable.DataBodyRange;
            int currentRow = 3;
            int rowsUsed = dataBodyRange.EndRow;

            // Sorting score in descending
            PivotField field = pivotTable.RowFields[0];
            field.IsAutoSort = true;
            field.IsAscendSort = false;
            field.AutoSortField = 0;

            pivotTable.RefreshData();
            pivotTable.CalculateData();

            // Hiding rows with score less than 60
            while (currentRow < rowsUsed)
            {
                Cell cell = worksheet.Cells[currentRow, 1];
                double score = Convert.ToDouble(cell.Value);
                if (score < 60)
                {
                    worksheet.Cells.HideRow(currentRow);
                }
                currentRow++;
            }

            pivotTable.RefreshData();
            pivotTable.CalculateData();

            // Saving the Excel file
            workbook.Save(outputDir + "PivotTableHideAndSort_out.xlsx");
            // ExEnd:1

            Console.WriteLine("PivotTableSortAndHide executed successfully.");
        }
    }
}

```
