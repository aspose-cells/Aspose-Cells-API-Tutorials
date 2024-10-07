---
title: Access Specific Named Range in Excel
linktitle: Access Specific Named Range in Excel
second_title: Aspose.Cells .NET Excel Processing API
description: 
type: docs
weight: 11
url: /net/excel-working-with-named-ranges/access-specific-named-range/
---

## Complete Source Code
```csharp
using System.IO;
using System;
using Aspose.Cells;

namespace Aspose.Cells.Examples.CSharp.Data
{
    public class AccessSpecificNamedRange
    {
        //Source directory
        static string sourceDir = "Your Document Directory"();

        public static void Run()
        {
            // Opening the Excel file through the file stream
            Workbook workbook = new Workbook(sourceDir + "sampleAccessSpecificNamedRange.xlsx");

            // Getting the specified named range
            Range range = workbook.Worksheets.GetRangeByName("MyRangeTwo");

            if (range != null)
                Console.WriteLine("Named Range : " + range.RefersTo);

            Console.WriteLine("AccessSpecificNamedRange executed successfully.");
        }
    }
}

```
