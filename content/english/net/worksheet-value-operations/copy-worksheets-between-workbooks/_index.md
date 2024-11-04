---
title: Copy Worksheets between Two Workbooks using Aspose.Cells
linktitle: Copy Worksheets between Two Workbooks using Aspose.Cells
second_title: Aspose.Cells .NET Excel Processing API
description: 
type: docs
weight: 14
url: /net/worksheet-value-operations/copy-worksheets-between-workbooks/
---

## Complete Source Code
```csharp
using System.IO;
using Aspose.Cells;
using System;

namespace Aspose.Cells.Examples.CSharp.Worksheets.Value
{
    public class CopyWorksheetsBetweenWorkbooks
    {
        public static void Run()
        {
            // ExStart:1
            // The path to the documents directory.
            string dataDir = "Your Document Directory";

            string InputPath = dataDir + "book1.xls";

            // Create a Workbook.
            // Open a file into the first book.
            Workbook excelWorkbook0 = new Workbook(InputPath);

            // Create another Workbook.
            Workbook excelWorkbook1 = new Workbook();

            // Copy the first sheet of the first book into second book.
            excelWorkbook1.Worksheets[0].Copy(excelWorkbook0.Worksheets[0]);

            // Save the file.
            excelWorkbook1.Save(dataDir + "CopyWorksheetsBetweenWorkbooks_out.xls");
            // ExEnd:1
        }
    }
}

```
