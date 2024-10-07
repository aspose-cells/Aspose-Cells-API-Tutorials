---
title: Access All Named Ranges in Excel
linktitle: Access All Named Ranges in Excel
second_title: Aspose.Cells .NET Excel Processing API
description: 
type: docs
weight: 10
url: /net/excel-working-with-named-ranges/access-all-named-ranges/
---

## Complete Source Code
```csharp
using System;
using System.IO;

using Aspose.Cells;

namespace Aspose.Cells.Examples.CSharp.Data
{
    public class AccessAllNamedRanges
    {
        //Source directory
        static string sourceDir = "Your Document Directory"();

        public static void Run()
        {
            // Opening the Excel file through the file stream
            Workbook workbook = new Workbook(sourceDir + "sampleAccessAllNamedRanges.xlsx");

            // Getting all named ranges
            Range[] range = workbook.Worksheets.GetNamedRanges();

            Console.WriteLine("Total Number of Named Ranges: " + range.Length);

            Console.WriteLine("AccessAllNamedRanges executed successfully.");
        }
    }
}

```
