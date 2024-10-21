---
title: Calculating Formulas Once Programmatically in Excel
linktitle: Calculating Formulas Once Programmatically in Excel
second_title: Aspose.Cells .NET Excel Processing API
description: 
type: docs
weight: 12
url: /net/excel-formulas-and-calculation-options/calculating-formulas-once/
---

## Complete Source Code
```csharp
using System.IO;

using Aspose.Cells;
using System;

namespace Aspose.Cells.Examples.CSharp.Formulas
{
    public class CalculatingFormulasOnce
    {
        public static void Run()
        {
            // ExStart:1
            // The path to the documents directory.
            string dataDir = RunExamples.GetDataDir(System.Reflection.MethodBase.GetCurrentMethod().DeclaringType);

          

            // Load the template workbook
            Workbook workbook = new Workbook(dataDir + "book1.xls");

            // Print the time before formula calculation
            Console.WriteLine(DateTime.Now);

            // Set the CreateCalcChain as false
            workbook.Settings.CreateCalcChain = false;

            // Calculate the workbook formulas
            workbook.CalculateFormula();

            // Print the time after formula calculation
            Console.WriteLine(DateTime.Now);
            // ExEnd:1

        }
    }
}

```
