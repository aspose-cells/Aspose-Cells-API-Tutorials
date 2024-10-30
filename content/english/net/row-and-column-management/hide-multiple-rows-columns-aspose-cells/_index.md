---
title: Hide Multiple Rows and Columns in Aspose.Cells .NET
linktitle: Hide Multiple Rows and Columns in Aspose.Cells .NET
second_title: Aspose.Cells .NET Excel Processing API
description: 
type: docs
weight: 16
url: /net/row-and-column-management/hide-multiple-rows-columns-aspose-cells/
---

## Complete Source Code
```csharp
using System.IO;

using Aspose.Cells;

namespace Aspose.Cells.Examples.CSharp.RowsColumns.Hiding
{
    public class HidingMultipleRowsAndColumns
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

            // Hiding 3,4 and 5 rows in the worksheet
            worksheet.Cells.HideRows(2, 3);

            // Hiding 2 and 3 columns in the worksheet
            worksheet.Cells.HideColumns(1, 2);

            // Saving the modified Excel file
            workbook.Save(dataDir + "outputxls");

            // Closing the file stream to free all resources
            fstream.Close();
            // ExEnd:1

        }
    }
}

```
