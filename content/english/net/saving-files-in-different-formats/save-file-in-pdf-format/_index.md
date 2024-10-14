---
title: Save File in PDF Format
linktitle: Save File in PDF Format
second_title: Aspose.Cells .NET Excel Processing API
description: 
type: docs
weight: 15
url: /net/saving-files-in-different-formats/save-file-in-pdf-format/
---

## Complete Source Code
```csharp
using System.IO;
using System.Web;
using Aspose.Cells;

namespace Aspose.Cells.Examples.CSharp.Files.Handling
{
    public class SaveInPdfFormat
    {
        public static void Run()
        {
            // ExStart:1
            // The path to the documents directory.
            string dataDir = "Your Document Directory";
            HttpResponse Respose = null;
            // Creating a Workbook object
            Workbook workbook = new Workbook();
            if (Respose != null)
            {
                // Save in Pdf format
                workbook.Save(Respose, dataDir + "output.pdf", ContentDisposition.Attachment, new PdfSaveOptions());
                Respose.End();
            }            
            // ExEnd:1
        }
    }
}

```
