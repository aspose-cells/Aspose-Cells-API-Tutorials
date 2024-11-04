---
title: Read and Write Table with Query Data Source
linktitle: Read and Write Table with Query Data Source
second_title: Aspose.Cells .NET Excel Processing API
description: 
type: docs
weight: 15
url: /net/tables-and-lists/reading-and-writing-table-with-query-data-source/
---

## Complete Source Code
```csharp
using System;
using Aspose.Cells.Tables;

namespace Aspose.Cells.Examples.CSharp.Tables
{
    public class ReadAndWriteTableWithQueryTableDataSource
    {
        public static void Run()
        {
            // ExStart:1
            // The path to the source directory.
            string sourceDir = "Your Document Directory";
            string outputDir = "Your Document Directory";

            // Load workbook object
            Workbook workbook = new Workbook(sourceDir + "SampleTableWithQueryTable.xls");

            Worksheet worksheet = workbook.Worksheets[0];

            ListObject table = worksheet.ListObjects[0];

            // Check the data source type if it is query table
            if (table.DataSourceType == TableDataSourceType.QueryTable)
            {
                table.ShowTotals = true;
            }

            // Save the file
            workbook.Save(outputDir + "SampleTableWithQueryTable_out.xls");
            // ExEnd:1

            Console.WriteLine("ReadAndWriteTableWithQueryTableDataSource executed successfully.");

        }
    }
}

```
