---
title: Copy Rows using Aspose.Cells for .NET
linktitle: Copy Rows using Aspose.Cells for .NET
second_title: Aspose.Cells .NET Excel Processing API
description: 
type: docs
weight: 11
url: /net/row-and-column-management/copying-rows/
---

## Complete Source Code
```csharp
using System.IO;

using Aspose.Cells;

namespace Aspose.Cells.Examples.CSharp.RowsColumns.Copying
{
    public class CopyingRows
    {
        public static void Run()
        {
            // ExStart:1
            // The path to the documents directory.
            string dataDir = "Your Document Directory";

            // Open the existing excel file.
            Workbook excelWorkbook1 = new Workbook(dataDir + "book1.xls");

            // Get the first worksheet in the workbook.
            Worksheet wsTemplate = excelWorkbook1.Worksheets[0];

            // Copy the second row with data, formattings, images and drawing objects
            // To the 16th row in the worksheet.
            wsTemplate.Cells.CopyRow(wsTemplate.Cells, 1, 15);

            // Save the excel file.
            excelWorkbook1.Save(dataDir + "output.xls");
            // ExEnd:1

        }
    }
}

```
