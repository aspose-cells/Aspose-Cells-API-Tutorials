---
title: Save XLSX File
linktitle: Save XLSX File
second_title: Aspose.Cells .NET Excel Processing API
description: 
type: docs
weight: 19
url: /net/saving-files-in-different-formats/save-xlsx-file/
---

## Complete Source Code
```csharp
using System.IO;
using System.Web;
using Aspose.Cells;
using System;

namespace Aspose.Cells.Examples.CSharp.Files.Handling
{
    public class SaveXLSXFile
    {
        public static void Run()
        {
            // ExStart:1
            // The path to the documents directory.
            string dataDir = "Your Document Directory";
            HttpResponse Respose = null;
            // Load your source workbook
            Workbook workbook = new Workbook();
            if (Respose != null)
            {
                // Save in Excel2007 xlsx format
                workbook.Save(Respose, dataDir + "output.xlsx", ContentDisposition.Attachment, new OoxmlSaveOptions());
                Respose.End();
            }
            // ExEnd:1
        }
    }
}

```
