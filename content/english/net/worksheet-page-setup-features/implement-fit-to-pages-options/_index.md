---
title: Implement Fit to Pages Options in Worksheet
linktitle: Implement Fit to Pages Options in Worksheet
second_title: Aspose.Cells .NET Excel Processing API
description: 
type: docs
weight: 12
url: /net/worksheet-page-setup-features/implement-fit-to-pages-options/
---

## Complete Source Code
```csharp
using System.IO;
using Aspose.Cells;
using System;

namespace Aspose.Cells.Examples.CSharp.Worksheets.PageSetupFeatures
{
    public class FitToPagesOptions
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

            // Setting the number of pages to which the length of the worksheet will be spanned
            worksheet.PageSetup.FitToPagesTall = 1;

            // Setting the number of pages to which the width of the worksheet will be spanned
            worksheet.PageSetup.FitToPagesWide = 1;

            // Save the workbook.
            workbook.Save(dataDir + "FitToPagesOptions_out.xls");
            // ExEnd:1
        }
    }
}

```
