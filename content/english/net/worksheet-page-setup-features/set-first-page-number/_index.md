---
title: Set First Page Number of Worksheet
linktitle: Set First Page Number of Worksheet
second_title: Aspose.Cells .NET Excel Processing API
description: 
type: docs
weight: 21
url: /net/worksheet-page-setup-features/set-first-page-number/
---

## Complete Source Code
```csharp
using System.IO;
using Aspose.Cells;
using System;

namespace Aspose.Cells.Examples.CSharp.Worksheets.PageSetupFeatures
{
    public class SetFirstPageNumber
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

            // Setting the first page number of the worksheet pages
            worksheet.PageSetup.FirstPageNumber = 2;

            // Save the Workbook.
            workbook.Save(dataDir + "SetFirstPageNumber_out.xls");
            // ExEnd:1
        }
    }
}

```
