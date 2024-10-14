---
title: Converting Excel to MHTML in .NET
linktitle: Converting Excel to MHTML in .NET
second_title: Aspose.Cells .NET Excel Processing API
description: 
type: docs
weight: 12
url: /net/conversion-and-rendering/converting-excel-to-mhtml/
---

## Complete Source Code
```csharp
using System.IO;

using Aspose.Cells;

namespace Aspose.Cells.Examples.CSharp.Files.Utility
{
    public class ConvertingToMHTMLFiles
    {
        public static void Run()
        {
            // ExStart:1
            // The path to the documents directory.
            string dataDir = "Your Document Directory";

            // Specify the file path
            string filePath = dataDir + "Book1.xlsx";

            // Specify the HTML Saving Options
            HtmlSaveOptions sv = new HtmlSaveOptions(SaveFormat.MHtml);

            // Instantiate a workbook and open the template XLSX file
            Workbook wb = new Workbook(filePath);

            // Save the MHT file
            wb.Save(filePath + ".out.mht", sv);
            // ExEnd:1
        }
    }
}

```
