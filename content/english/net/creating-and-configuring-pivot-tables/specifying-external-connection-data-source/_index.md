---
title: Specifying External Connection Data Source in .NET
linktitle: Specifying External Connection Data Source in .NET
second_title: Aspose.Cells .NET Excel Processing API
description: 
type: docs
weight: 24
url: /net/creating-and-configuring-pivot-tables/specifying-external-connection-data-source/
---

## Complete Source Code
```csharp
using System;
using Aspose.Cells.Pivot;

namespace Aspose.Cells.Examples.CSharp.PivotTables
{
    class PivotTableGetExternalConnectionDataSource
    {
        public static void Run()
        {
            // ExStart:1
            // Source directory
            string sourceDir = "Your Document Directory";

            // Load sample file
            Workbook workbook = new Workbook(sourceDir + "SamplePivotTableExternalConnection.xlsx");
        
            Worksheet worksheet = workbook.Worksheets[0];

            // Get the pivot table
            var pivotTable = worksheet.PivotTables[0];

            // Print External Connection Details
            Console.WriteLine("External Connection Data Source");
            Console.WriteLine("Name: " + pivotTable.ExternalConnectionDataSource.Name);
            Console.WriteLine("Type: " + pivotTable.ExternalConnectionDataSource.Type);
            //ExEnd: 1

            Console.WriteLine("PivotTableGetExternalConnectionDataSource executed successfully.");
        }
    }
}

```
