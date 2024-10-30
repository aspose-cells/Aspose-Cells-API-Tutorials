---
title: Delete Multiple Rows in Aspose.Cells .NET
linktitle: Delete Multiple Rows in Aspose.Cells .NET
second_title: Aspose.Cells .NET Excel Processing API
description: 
type: docs
weight: 21
url: /net/row-and-column-management/delete-multiple-rows-aspose-cells/
---

## Complete Source Code
```csharp
using System.IO;

using Aspose.Cells;

namespace Aspose.Cells.Examples.CSharp.RowsColumns.InsertingAndDeleting
{
    public class DeletingMultipleRows
    {
        public static void Run()
        {
            // ExStart:1
            // The path to the documents directory.
            string dataDir = "Your Document Directory";

            // Creating a file stream containing the Excel file to be opened
            FileStream fstream = new FileStream(dataDir + "Book1.xlsx", FileMode.OpenOrCreate);

            // Instantiating a Workbook object
            // Opening the Excel file through the file stream
            Workbook workbook = new Workbook(fstream);

            // Accessing the first worksheet in the Excel file
            Worksheet worksheet = workbook.Worksheets[0];

            // Deleting 10 rows from the worksheet starting from 3rd row
            worksheet.Cells.DeleteRows(2, 10);

            // Saving the modified Excel file
            workbook.Save(dataDir + "output.xlsx");

            // Closing the file stream to free all resources
            fstream.Close();
            // ExEnd:1
 
        }
    }
}

```
