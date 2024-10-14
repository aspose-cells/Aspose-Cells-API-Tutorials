---
title: Save File in SpreadsheetML Format
linktitle: Save File in SpreadsheetML Format
second_title: Aspose.Cells .NET Excel Processing API
description: 
type: docs
weight: 16
url: /net/saving-files-in-different-formats/save-file-in-spreadsheetml-format/
---

## Complete Source Code
```csharp
using System.IO;

using Aspose.Cells;

namespace Aspose.Cells.Examples.CSharp.Files.Handling
{
    public class SaveInSpreadsheetMLFormat
    {
        public static void Run()
        {
            // ExStart:1
            // The path to the documents directory.
            string dataDir = "Your Document Directory";

            // Creating a Workbook object
            Workbook workbook = new Workbook();
            // Save in SpreadsheetML format
            workbook.Save(dataDir + "output.xml", SaveFormat.SpreadsheetML); 
            // ExEnd:1
        }
    }
}

```
