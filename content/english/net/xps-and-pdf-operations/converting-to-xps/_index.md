---
title: Converting to XPS in .NET
linktitle: Converting to XPS in .NET
second_title: Aspose.Cells .NET Excel Processing API
description: 
type: docs
weight: 10
url: /net/xps-and-pdf-operations/converting-to-xps/
---

## Complete Source Code
```csharp
using System.IO;

using Aspose.Cells;

namespace Aspose.Cells.Examples.CSharp.Files.Utility
{
    public class ConvertingToXPS
    {
        public static void Run()
        {
            // ExStart:1
            // The path to the documents directory.
            string dataDir = "Your Document Directory";

            // Open an Excel file
            Aspose.Cells.Workbook workbook = new Aspose.Cells.Workbook(dataDir + "Book1.xls");

            // Get the first worksheet
            Aspose.Cells.Worksheet sheet = workbook.Worksheets[0];

            // Apply different Image and Print options
            Aspose.Cells.Rendering.ImageOrPrintOptions options = new Aspose.Cells.Rendering.ImageOrPrintOptions();
            
            // Set the Format
            options.SaveFormat = SaveFormat.Xps;
            
            // Render the sheet with respect to specified printing options
            Aspose.Cells.Rendering.SheetRender sr = new Aspose.Cells.Rendering.SheetRender(sheet, options);
            
            // Save
            sr.ToImage(0, dataDir + "out_printingxps.out.xps");

            // Export the whole workbook to xps
            Aspose.Cells.Rendering.WorkbookRender wr = new Aspose.Cells.Rendering.WorkbookRender(workbook, options);
            wr.ToImage(dataDir + "out_whole_printingxps.out.xps");
            // ExEnd:1
        }
    }
}

```
