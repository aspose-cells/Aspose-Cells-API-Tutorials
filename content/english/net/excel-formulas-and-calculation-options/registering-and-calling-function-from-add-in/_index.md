---
title: Registering and Calling Function from Add-In in Excel
linktitle: Registering and Calling Function from Add-In in Excel
second_title: Aspose.Cells .NET Excel Processing API
description: 
type: docs
weight: 20
url: /net/excel-formulas-and-calculation-options/registering-and-calling-function-from-add-in/
---

## Complete Source Code
```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;

namespace Aspose.Cells.Examples.CSharp.Formulas
{
    class RegisterAndCallFuncFromAddIn
    {
        // Source directory
        static string sourceDir = "Your Document Directory";

        // Output directory
        static string outputDir = "Your Document Directory";

        public static void Main()
        {
            // ExStart:1
            // Create empty workbook
            Workbook workbook = new Workbook();

            // Register macro enabled add-in along with the function name
            int id = workbook.Worksheets.RegisterAddInFunction(sourceDir + @"TESTUDF.xlam", "TEST_UDF", false);

            // Register more functions in the file (if any)
            workbook.Worksheets.RegisterAddInFunction(id, "TEST_UDF1"); //in this way you can add more functions that are in the same file

            // Access first worksheet
            Worksheet worksheet = workbook.Worksheets[0];

            // Access first cell
            var cell = worksheet.Cells["A1"];

            // Set formula name present in the add-in
            cell.Formula = "=TEST_UDF()";

            // Save workbook to output XLSX format.
            workbook.Save(outputDir +  @"test_udf.xlsx", Aspose.Cells.SaveFormat.Xlsx);
            // ExEnd:1

            Console.WriteLine("RegisterAndCallFuncFromAddIn executed successfully.");
        }

    }
}

```
