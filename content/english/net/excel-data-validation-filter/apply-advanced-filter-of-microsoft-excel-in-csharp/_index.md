---
title: Apply Advanced Filter of Microsoft Excel in C#
linktitle: Apply Advanced Filter of Microsoft Excel in C#
second_title: Aspose.Cells .NET Excel Processing API
description: 
type: docs
weight: 10
url: /net/excel-data-validation-filter/apply-advanced-filter-of-microsoft-excel-in-csharp/
---

## Complete Source Code
```csharp
using System;
using System.IO;

using Aspose.Cells;

namespace Aspose.Cells.Examples.CSharp.Data
{
    public class ApplyAdvancedFilterOfMicrosoftExcel 
    {
        public static void Run()
        {
            //Source directory
            string sourceDir = "Your Document Directory"();

            //Output directory
            string outputDir = "Your Document Directory"();

            //Load your source workbook
            Workbook wb = new Workbook(sourceDir + "sampleAdvancedFilter.xlsx");

            //Access first worksheet
            Worksheet ws = wb.Worksheets[0];

            //Apply advanced filter on range A5:D19 and criteria range is A1:D2
            //Besides, we want to filter in place
            //And, we want all filtered records not just unique records
            ws.AdvancedFilter(true, "A5:D19", "A1:D2", "", false);

            //Save the workbook in xlsx format
            wb.Save(outputDir + "outputAdvancedFilter.xlsx", SaveFormat.Xlsx);

            Console.WriteLine("ApplyAdvancedFilterOfMicrosoftExcel executed successfully.\r\n");
        }
    }
}
```
