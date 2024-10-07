---
title: Autofilter Begins With in Excel
linktitle: Autofilter Begins With in Excel
second_title: Aspose.Cells .NET Excel Processing API
description: 
type: docs
weight: 10
url: /net/excel-autofilter-validation/autofilter-begins-with-in-excel/
---

## Complete Source Code
```csharp
using System.IO;

using Aspose.Cells;
using System;

namespace Aspose.Cells.Examples.CSharp.Data.Processing.FilteringAndValidation
{
    public class AutofilterBeginsWith
    {
        //Source directory
        static string sourceDir = "Your Document Directory"();

        //Output directory
        static string outputDir = "Your Document Directory"();

        public static void Main()
        {
            // ExStart:1
            // Instantiating a Workbook object containing sample data
            Workbook workbook = new Workbook(sourceDir + "sourseSampleCountryNames.xlsx");

            // Accessing the first worksheet in the Excel file
            Worksheet worksheet = workbook.Worksheets[0];

            // Creating AutoFilter by giving the cells range
            worksheet.AutoFilter.Range = "A1:A18";

            // Initialize filter for rows starting with string "Ba"
            worksheet.AutoFilter.Custom(0, FilterOperatorType.BeginsWith, "Ba");

            //Refresh the filter to show/hide filtered rows
            worksheet.AutoFilter.Refresh();

            // Saving the modified Excel file
            workbook.Save(outputDir +  "outSourseSampleCountryNames.xlsx");
            // ExEnd:1

            Console.WriteLine("AutofilterBeginsWith executed successfully.\r\n");
        }
    }
}

```
