---
title: Interrupt or Cancel Formula Calculation of Workbook
linktitle: Interrupt or Cancel Formula Calculation of Workbook
second_title: Aspose.Cells .NET Excel Processing API
description: 
type: docs
weight: 15
url: /net/excel-formulas-and-calculation-options/interrupt-or-cancel-formula-calculation-of-workbook/
---

## Complete Source Code
```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;

namespace Aspose.Cells.Examples.CSharp.Formulas
{
    class InterruptOrCancelFormulaCalculationOfWorkbook
    {
        //Implement calculation monitor class
        class clsCalculationMonitor : AbstractCalculationMonitor
        {
            public override void BeforeCalculate(int sheetIndex, int rowIndex, int colIndex)
            {
                //Find the cell name
                string cellName = CellsHelper.CellIndexToName(rowIndex, colIndex);

                //Print the sheet, row and column index as well as cell name
                System.Diagnostics.Debug.WriteLine(sheetIndex + "----" + rowIndex + "----" + colIndex + "----" + cellName);

                //If cell name is B8, interrupt/cancel the formula calculation
                if (cellName == "B8")
                {
                    this.Interrupt("Interrupt/Cancel the formula calculation");
                }//if

            }//BeforeCalculate

        }//clsCalculationMonitor

        public static void Run()
        {
            //Source directory
            string sourceDir = "Your Document Directory";

            //Load the sample Excel file
            Workbook wb = new Workbook(sourceDir + "sampleCalculationMonitor.xlsx");

            //Create calculation options and assign instance of calculation monitor class
            CalculationOptions opts = new CalculationOptions();
            opts.CalculationMonitor = new clsCalculationMonitor();

            //Calculate formula with calculation options
            wb.CalculateFormula(opts);

            Console.WriteLine("InterruptOrCancelFormulaCalculationOfWorkbook executed successfully.\r\n");
        }
    }
}

```
