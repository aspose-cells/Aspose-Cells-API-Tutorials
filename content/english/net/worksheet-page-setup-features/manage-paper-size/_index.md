---
title: Manage Paper Size of Worksheet
linktitle: Manage Paper Size of Worksheet
second_title: Aspose.Cells .NET Excel Processing API
description: 
type: docs
weight: 16
url: /net/worksheet-page-setup-features/manage-paper-size/
---

## Complete Source Code
```csharp
using System.IO;
using Aspose.Cells;
using System;

namespace Aspose.Cells.Examples.CSharp.Worksheets.PageSetupFeatures
{
    public class ManagePaperSize
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

            // Setting the paper size to A4
            worksheet.PageSetup.PaperSize = PaperSizeType.PaperA4;

            // Save the Workbook.
            workbook.Save(dataDir + "ManagePaperSize_out.xls");
            // ExEnd:1
        }
    }
}

```
