---
title: Save Excel File in 97-2003 Format
linktitle: Save Excel File in 97-2003 Format
second_title: Aspose.Cells .NET Excel Processing API
description: 
type: docs
weight: 10
url: /net/saving-files-in-different-formats/save-excel-file-in-97-2003-format/
---

## Complete Source Code
```csharp
using System.IO;

using Aspose.Cells;

namespace Aspose.Cells.Examples.CSharp.Files.Handling
{
    public class SaveFileInExcel972003format
    {
        public static void Run()
        {
            // ExStart:1
            // The path to the documents directory.
            string dataDir = "Your Document Directory";

            // Creating a Workbook object
            Workbook workbook = new Workbook();

            // Your Code goes here for any workbook related operations

            // Save in Excel 97 – 2003 format
            workbook.Save(dataDir + "output.xls");

            // OR
            workbook.Save(dataDir + "output.xls", SaveFormat.Excel97To2003);
            // ExEnd:1
           }
         }
      }

```
