---
title: Copy Columns using Aspose.Cells for .NET
linktitle: Copy Columns using Aspose.Cells for .NET
second_title: Aspose.Cells .NET Excel Processing API
description: 
type: docs
weight: 10
url: /net/row-and-column-management/copying-columns/
---

## Complete Source Code
```csharp
using System.IO;

using Aspose.Cells;

namespace Aspose.Cells.Examples.CSharp.RowsColumns.Copying
{
    public class CopyingColumns
    {
        public static void Run()
        {
            // ExStart:1
            // The path to the documents directory.
            string dataDir = "Your Document Directory";
                       

            // Create another Workbook.
            Workbook excelWorkbook1 = new Workbook(dataDir + "book1.xls");

            // Get the first worksheet in the book.
            Worksheet ws1 = excelWorkbook1.Worksheets[0];

            // Copy the first column from the first worksheet of the first workbook into
            // The first worksheet of the second workbook.
            ws1.Cells.CopyColumn(ws1.Cells, ws1.Cells.Columns[0].Index, ws1.Cells.Columns[2].Index);

            // Autofit the column.
            ws1.AutoFitColumn(2);

            // Save the excel file.
            excelWorkbook1.Save(dataDir + "output.xls");
            // ExEnd:1

        }
    }
}

```
