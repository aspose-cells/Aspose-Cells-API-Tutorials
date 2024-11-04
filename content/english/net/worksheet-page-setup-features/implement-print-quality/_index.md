---
title: Implement Print Quality of Worksheet
linktitle: Implement Print Quality of Worksheet
second_title: Aspose.Cells .NET Excel Processing API
description: 
type: docs
weight: 26
url: /net/worksheet-page-setup-features/implement-print-quality/
---

## Complete Source Code
```csharp
using System.IO;
using Aspose.Cells;
using System;

namespace Aspose.Cells.Examples.CSharp.Worksheets.PageSetupFeatures
{
    public class SetPrintQuality
    {
        public static void Run()
        {
            // ExStart:1
            // The path to the documents directory.
            string dataDir = "Your Document Directory";

            // Instantiating a Workbook object
            Workbook workbook = new Workbook();

            // Accessing the first worksheet in the Excel file
            Worksheet worksheet = workbook.Worksheets[0];

            // Setting the print quality of the worksheet to 180 dpi
            worksheet.PageSetup.PrintQuality = 180;

            // Save the Workbook.
            workbook.Save(dataDir + "SetPrintQuality_out.xls");
            // ExEnd:1
        }
    }
}

```
