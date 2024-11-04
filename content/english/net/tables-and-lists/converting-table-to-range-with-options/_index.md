---
title: Convert Table to Range with Options
linktitle: Convert Table to Range with Options
second_title: Aspose.Cells .NET Excel Processing API
description: 
type: docs
weight: 14
url: /net/tables-and-lists/converting-table-to-range-with-options/
---

## Complete Source Code
```csharp
using System;
using System.IO;

using Aspose.Cells;
using Aspose.Cells.Tables;

namespace Aspose.Cells.Examples.CSharp.Tables
{
    public class ConvertTableToRangeWithOptions
    {
        public static void Run()
        {
            // ExStart:1
            // The path to the documents directory.
            string dataDir = "Your Document Directory";

            // Open an existing file that contains a table/list object in it
            Workbook workbook = new Workbook(dataDir + "book1.xlsx");

            TableToRangeOptions options = new TableToRangeOptions();
            options.LastRow = 5;

            // Convert the first table/list object (from the first worksheet) to normal range
            workbook.Worksheets[0].ListObjects[0].ConvertToRange(options);

            // Save the file
            workbook.Save(dataDir + "output.xlsx");
            // ExEnd:1

            Console.WriteLine("ConvertTableToRangeWithOptions executed successfully.\r\n");
        }
    }
}

```
