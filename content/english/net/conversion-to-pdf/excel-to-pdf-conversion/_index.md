---
title: Excel to PDF Conversion in .NET
linktitle: Excel to PDF Conversion in .NET
second_title: Aspose.Cells .NET Excel Processing API
description: 
type: docs
weight: 10
url: /net/conversion-to-pdf/excel-to-pdf-conversion/
---

## Complete Source Code
```csharp
using System.IO;

using Aspose.Cells;

namespace Aspose.Cells.Examples.CSharp.Files.Utility
{
    public class Excel2PDFConversion
    {
        public static void Run()
        {
            // ExStart:1
            // The path to the documents directory.
            string dataDir = "Your Document Directory";

            // Instantiate the Workbook object
            // Open an Excel file
            Workbook workbook = new Workbook(dataDir + "abc.xlsx");

            // Save the document in PDF format
            workbook.Save(dataDir + "outBook2.out.pdf", SaveFormat.Pdf);

            // Display result, so that user knows the processing has finished.
            System.Console.WriteLine("Conversion completed.");
            // ExEnd:1
        }
    }
}

```
