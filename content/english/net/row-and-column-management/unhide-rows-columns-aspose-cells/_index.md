---
title: Unhide Rows and Columns in Aspose.Cells .NET
linktitle: Unhide Rows and Columns in Aspose.Cells .NET
second_title: Aspose.Cells .NET Excel Processing API
description: 
type: docs
weight: 18
url: /net/row-and-column-management/unhide-rows-columns-aspose-cells/
---

## Complete Source Code
```csharp
using System.IO;

using Aspose.Cells;

namespace Aspose.Cells.Examples.CSharp.RowsColumns.Hiding
{
    public class UnhidingRowsAndColumns
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

            // Unhiding the 3rd row and setting its height to 13.5
            worksheet.Cells.UnhideRow(2, 13.5);

            // Unhiding the 2nd column and setting its width to 8.5
            worksheet.Cells.UnhideColumn(1, 8.5);

            // Saving the modified Excel file
            workbook.Save(dataDir + "output.xls");

            // Closing the file stream to free all resources
            fstream.Close();
            // ExEnd:1

        }
    }
}

```
