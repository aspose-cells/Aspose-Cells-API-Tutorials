---
title: Convert Table to ODS using Aspose.Cells
linktitle: Convert Table to ODS using Aspose.Cells
second_title: Aspose.Cells .NET Excel Processing API
description: 
type: docs
weight: 12
url: /net/tables-and-lists/converting-table-to-ods/
---

## Complete Source Code
```csharp
using System;
using System.IO;

using Aspose.Cells;

namespace Aspose.Cells.Examples.CSharp.Tables
{
    public class ConvertTableToOds
    {
        public static void Run()
        {
            // ExStart:1
            //Source directory
            string sourceDir = "Your Document Directory";

            //Output directory
            string outputDir = "Your Document Directory";

            // Open an existing file that contains a table/list object in it
            Workbook wb = new Workbook(sourceDir + "SampleTable.xlsx");

            // Save the file
            wb.Save(outputDir + "ConvertTableToOds_out.ods");
            // ExEnd:1

            Console.WriteLine("ConvertTableToOds executed successfully.");
        }
    }
}

```
