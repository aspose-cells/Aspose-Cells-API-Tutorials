---
title: Group Rows and Columns in Excel with Aspose.Cells
linktitle: Group Rows and Columns in Excel with Aspose.Cells
second_title: Aspose.Cells .NET Excel Processing API
description: 
type: docs
weight: 12
url: /net/row-and-column-management/grouping-rows-and-columns/
---

## Complete Source Code
```csharp
using System.IO;

using Aspose.Cells;

namespace Aspose.Cells.Examples.CSharp.RowsColumns.Grouping
{
    public class GroupingRowsAndColumns
    {
        public static void Run()
        {
            // ExStart:1
            // The path to the documents directory.
            string dataDir = "Your Document Directory";

            // Creating a file stream containing the Excel file to be opened
            FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);

            // Opening the Excel file through the file stream
            Workbook workbook = new Workbook(fstream);

            // Accessing the first worksheet in the Excel file
            Worksheet worksheet = workbook.Worksheets[0];

            // Grouping first six rows (from 0 to 5) and making them hidden by passing true
            worksheet.Cells.GroupRows(0, 5, true);

            // Grouping first three columns (from 0 to 2) and making them hidden by passing true
            worksheet.Cells.GroupColumns(0, 2, true);

            // Saving the modified Excel file
            workbook.Save(dataDir + "output.xls");

            // Closing the file stream to free all resources
            fstream.Close();
            // ExEnd:1

            
        }
    }
}

```
