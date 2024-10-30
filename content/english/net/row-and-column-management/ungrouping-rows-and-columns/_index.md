---
title: Ungroup Rows and Columns in Excel with Aspose.Cells
linktitle: Ungroup Rows and Columns in Excel with Aspose.Cells
second_title: Aspose.Cells .NET Excel Processing API
description: 
type: docs
weight: 15
url: /net/row-and-column-management/ungrouping-rows-and-columns/
---

## Complete Source Code
```csharp
using System.IO;

using Aspose.Cells;

namespace Aspose.Cells.Examples.CSharp.RowsColumns.Grouping
{
    public class UngroupingRowsAndColumns
    {
        public static void Run()
        {
            // ExStart:1
            // The path to the documents directory.
            string dataDir = "Your Document Directory";

            // Creating a file stream containing the Excel file to be opened
            FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);

            // Instantiating a Workbook object
            // Opening the Excel file through the file stream
            Workbook workbook = new Workbook(fstream);

            // Accessing the first worksheet in the Excel file
            Worksheet worksheet = workbook.Worksheets[0];

            // Ungrouping first six rows (from 0 to 5)
            worksheet.Cells.UngroupRows(0, 5);

            // Ungrouping first three columns (from 0 to 2)
            worksheet.Cells.UngroupColumns(0, 2);

            // Saving the modified Excel file
            workbook.Save(dataDir + "output.xls");

            // Closing the file stream to free all resources
            fstream.Close();
            // ExEnd:1
        }
    }
}

```
