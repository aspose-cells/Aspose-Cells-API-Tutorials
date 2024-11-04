---
title: Get Cell Validation in ODS File
linktitle: Get Cell Validation in ODS File
second_title: Aspose.Cells .NET Excel Processing API
description: 
type: docs
weight: 16
url: /net/worksheet-operations/get-cell-validation-ods/
---

## Complete Source Code
```csharp
using System;

namespace Aspose.Cells.Examples.CSharp.Worksheets
{
    class GetCellValidationInODS
    {
        public static void Run()
        {
            // ExStart:1
            //Source directory
            string sourceDir = "Your Document Directory";

            //Load source Excel file
            Workbook workbook = new Workbook(sourceDir + "SampleBook1.ods");

            //Access first worksheet
            Worksheet worksheet = workbook.Worksheets[0];

            Cell cell = worksheet.Cells["A9"];

            if (cell.GetValidation() != null)
            {
                Console.WriteLine(cell.GetValidation().Type);
            }
            // ExEnd:1

            Console.WriteLine("GetCellValidationInODS executed successfully.");
        }
    }
}

```
