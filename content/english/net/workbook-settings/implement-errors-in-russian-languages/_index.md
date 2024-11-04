---
title: Implement Errors and Boolean Value in Russian or Other Languages
linktitle: Implement Errors and Boolean Value in Russian or Other Languages
second_title: Aspose.Cells .NET Excel Processing API
description: 
type: docs
weight: 12
url: /net/workbook-settings/implement-errors-in-russian-languages/
---

## Complete Source Code
```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;

namespace Aspose.Cells.Examples.CSharp.WorkbookSettings
{
    //Russian Globalization
    class RussianGlobalization : GlobalizationSettings
    {
        public override string GetErrorValueString(string err)
        {
            switch (err.ToUpper())
            {
                case "#NAME?":
                    return "#RussianName-имя?";

            }

            return "RussianError-ошибка";
        }

        public override string GetBooleanValueString(bool bv)
        {
            return bv ? "RussianTrue-правда" : "RussianFalse-ложный";
        }
    }

    public class ImplementErrorsAndBooleanValueInRussianOrAnyOtherLanguage 
    {
        public static void Run()
        {
            //Source directory
            string sourceDir = "Your Document Directory";

            //Output directory
            string outputDir = "Your Document Directory";

            //Load the source workbook
            Workbook wb = new Workbook(sourceDir + "sampleRussianGlobalization.xlsx");

            //Set GlobalizationSettings in Russian Language
            wb.Settings.GlobalizationSettings = new RussianGlobalization();

            //Calculate the formula
            wb.CalculateFormula();

            //Save the workbook in pdf format
            wb.Save(outputDir + "outputRussianGlobalization.pdf");

            Console.WriteLine("ImplementErrorsAndBooleanValueInRussianOrAnyOtherLanguage executed successfully.\r\n");
        }
    }
}

```
