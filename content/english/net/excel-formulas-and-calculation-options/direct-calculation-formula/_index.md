---
title: Direct Calculation Formula in Excel Programmatically
linktitle: Direct Calculation Formula in Excel Programmatically
second_title: Aspose.Cells .NET Excel Processing API
description: 
type: docs
weight: 14
url: /net/excel-formulas-and-calculation-options/direct-calculation-formula/
---

## Complete Source Code
```csharp
using System.IO;

using Aspose.Cells;

namespace Aspose.Cells.Examples.CSharp.Formulas
{
    public class DirectCalculationFormula
    {
        public static void Run()
        {
            // ExStart:1
            // The path to the documents directory.
            string dataDir = "Your Document Directory";

            // Create directory if it is not already present.
            bool IsExists = System.IO.Directory.Exists(dataDir);
            if (!IsExists)
                System.IO.Directory.CreateDirectory(dataDir);

            // Create a workbook
            Workbook workbook = new Workbook();

            // Access first worksheet
            Worksheet worksheet = workbook.Worksheets[0];

            // Put 20 in cell A1
            Cell cellA1 = worksheet.Cells["A1"];
            cellA1.PutValue(20);

            // Put 30 in cell A2
            Cell cellA2 = worksheet.Cells["A2"];
            cellA2.PutValue(30);

            // Calculate the Sum of A1 and A2
            var results = worksheet.CalculateFormula("=Sum(A1:A2)");

            // Print the output
            System.Console.WriteLine("Value of A1: " + cellA1.StringValue);
            System.Console.WriteLine("Value of A2: " + cellA2.StringValue);
            System.Console.WriteLine("Result of Sum(A1:A2): " + results.ToString());
            // ExEnd:1

        }
    }
}

```
