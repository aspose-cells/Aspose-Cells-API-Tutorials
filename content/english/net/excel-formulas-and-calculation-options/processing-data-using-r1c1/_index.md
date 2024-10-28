---
title: Processing Data Using R1C1 in Excel
linktitle: Processing Data Using R1C1 in Excel
second_title: Aspose.Cells .NET Excel Processing API
description: 
type: docs
weight: 19
url: /net/excel-formulas-and-calculation-options/processing-data-using-r1c1/
---

## Complete Source Code
```csharp
using System.IO;

using Aspose.Cells;

namespace Aspose.Cells.Examples.CSharp.Formulas
{
    public class ProcessDataUsingR1C1
    {
        public static void Run()
        {
            // ExStart:1
            // The path to the documents directory.
            string dataDir = "Your Document Directory";

            // Instantiating a Workbook object
            Workbook workbook = new Workbook(dataDir + "Book1.xls");

            Worksheet worksheet = workbook.Worksheets[0];

            // Setting an R1C1 formula on the "A11" cell, 
            // Row and Column indeces are relative to destination index
            worksheet.Cells["A11"].R1C1Formula = "=SUM(R[-10]C[0]:R[-7]C[0])";

            // Saving the Excel file
            workbook.Save(dataDir + "output.xls");
            // ExEnd:1

        }
    }
}

```
