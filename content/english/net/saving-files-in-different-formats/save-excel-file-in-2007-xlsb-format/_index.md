---
title: Save Excel File in 2007 xlsb Format
linktitle: Save Excel File in 2007 xlsb Format
second_title: Aspose.Cells .NET Excel Processing API
description: 
type: docs
weight: 11
url: /net/saving-files-in-different-formats/save-excel-file-in-2007-xlsb-format/
---

## Complete Source Code
```csharp
using System.IO;

using Aspose.Cells;

namespace Aspose.Cells.Examples.CSharp.Files.Handling
{
    public class SaveInExcel2007xlsbFormat
    {
        public static void Run()
        {
            // ExStart:1
            // The path to the documents directory.
            string dataDir = "Your Document Directory";

            // Creating a Workbook object
            Workbook workbook = new Workbook();
            // Save in Excel2007 xlsb format
            workbook.Save(dataDir + "output.xlsb", SaveFormat.Xlsb);
            // ExEnd:1
        }
    }
  }

```
