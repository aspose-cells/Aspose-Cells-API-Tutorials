---
title: Consolidation Functions Programmatically in .NET
linktitle: Consolidation Functions Programmatically in .NET
second_title: Aspose.Cells .NET Excel Processing API
description: 
type: docs
weight: 12
url: /net/creating-and-configuring-pivot-tables/consolidation-functions/
---

## Complete Source Code
```csharp
using System.IO;

using Aspose.Cells;
using System.Drawing;
using Aspose.Cells.Pivot;

namespace Aspose.Cells.Examples.CSharp.PivotTableExamples
{
    public class ConsolidationFunctions
    {
               public static void Run()
        {
            // ExStart:1
            // The path to the documents directory.
            string dataDir = "Your Document Directory";
                   
            // Create workbook from source excel file
            Workbook workbook = new Workbook(dataDir + "Book.xlsx");

            // Access the first worksheet of the workbook
            Worksheet worksheet = workbook.Worksheets[0];

            // Access the first pivot table of the worksheet
            PivotTable pivotTable = worksheet.PivotTables[0];

            // Apply Average consolidation function to first data field
            pivotTable.DataFields[0].Function = ConsolidationFunction.Average;

            // Apply DistinctCount consolidation function to second data field
            pivotTable.DataFields[1].Function = ConsolidationFunction.DistinctCount;

            // Calculate the data to make changes affect
            pivotTable.CalculateData();
                  
            // Saving the Excel file
            workbook.Save(dataDir + "output.xlsx");

            // ExEnd:1

        }
    }
}
```
