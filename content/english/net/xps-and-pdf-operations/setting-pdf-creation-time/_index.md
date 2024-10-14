---
title: Setting PDF Creation Time in .NET
linktitle: Setting PDF Creation Time in .NET
second_title: Aspose.Cells .NET Excel Processing API
description: 
type: docs
weight: 11
url: /net/xps-and-pdf-operations/setting-pdf-creation-time/
---

## Complete Source Code
```csharp
using System;
using Aspose.Cells;
using Aspose.Cells.Charts;

namespace Aspose.Cells.Examples.CSharp.Files.Utility
{
    class SetPDFCreationTime
    {
        public static void Run()
        {

            // ExStart:1
            string dataDir = "Your Document Directory";
            string inputPath = dataDir + "Book1.xlsx";
            // Load excel file containing charts
            Workbook workbook = new Workbook(inputPath);

            // Create an instance of PdfSaveOptions and pass SaveFormat to the constructor
            PdfSaveOptions options = new PdfSaveOptions();
            options.CreatedTime = DateTime.Now;

            // Save the workbook to PDF format while passing the object of PdfSaveOptions
            workbook.Save(dataDir + "output.pdf", options);
            // ExEnd:1

        }
    }
}

```
