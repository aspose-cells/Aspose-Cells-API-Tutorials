---
title: Save File in HTML Format
linktitle: Save File in HTML Format
second_title: Aspose.Cells .NET Excel Processing API
description: 
type: docs
weight: 13
url: /net/saving-files-in-different-formats/save-file-in-html-format/
---

## Complete Source Code
```csharp
using System.IO;

using Aspose.Cells;

namespace Aspose.Cells.Examples.CSharp.Files.Handling
{
    public class SaveInHtmlFormat
    {
        public static void Run()
        {
            // ExStart:1
            // The path to the documents directory.
            string dataDir = "Your Document Directory";

            // Creating a Workbook object
            Workbook workbook = new Workbook();
          // Save in Html format
            workbook.Save(dataDir + "output.html", SaveFormat.Html);
            
          // ExEnd:1
          }
     }
 }

```
