---
title: Copy Data Within Workbook using Aspose.Cells
linktitle: Copy Data Within Workbook using Aspose.Cells
second_title: Aspose.Cells .NET Excel Processing API
description: 
type: docs
weight: 12
url: /net/worksheet-value-operations/copy-data-within-workbook/
---

## Complete Source Code
```csharp
using System.IO;
using Aspose.Cells;
using System;

namespace Aspose.Cells.Examples.CSharp.Worksheets.Value
{
    public class CopyWithinWorkbook
    {
        public static void Run()
        {
            // ExStart:1
            // The path to the documents directory.
            string dataDir = "Your Document Directory";

            string InputPath = dataDir + "book1.xls";

            // Open an existing Excel file.
            Workbook wb = new Workbook(InputPath);

            // Create a Worksheets object with reference to
            // the sheets of the Workbook.
            WorksheetCollection sheets = wb.Worksheets;

            // Copy data to a new sheet from an existing
            // sheet within the Workbook.
            sheets.AddCopy("Sheet1");

            // Save the Excel file.
            wb.Save(dataDir + "CopyWithinWorkbook_out.xls");
            // ExEnd:1
        }
    }
}

```
