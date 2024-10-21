---
title: Get List of Fonts Used in Spreadsheet
linktitle: Get List of Fonts Used in Spreadsheet
second_title: Aspose.Cells .NET Excel Processing API
description: 
type: docs
weight: 10
url: /net/working-with-fonts-in-spreadsheets/get-list-of-fonts-used-in-spreadsheet/
---

## Complete Source Code
```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.IO;

namespace Aspose.Cells.Examples.CSharp.Fonts
{
    public class GetListOfFontsUsedInSpreadsheetOrWorkbook
    {
        public static void Run()
        {
            // ExStart:GetListOfFontsUsedInSpreadsheetOrWorkbook
            // The path to the documents directory.
            string dataDir = "Your Document Directory";

            //Load source workbook
            Workbook wb = new Workbook(dataDir + "sampleGetFonts.xlsx");

            //Get all the fonts inside the workbook
            Aspose.Cells.Font[] fnts = wb.GetFonts();

            //Print all the fonts
            for (int i = 0; i < fnts.Length; i++)
            {
                Console.WriteLine(fnts[i]);
            }

            // ExEnd:GetListOfFontsUsedInSpreadsheetOrWorkbook
        }
    }
}

```
