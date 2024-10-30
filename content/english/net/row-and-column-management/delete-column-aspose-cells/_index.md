---
title: Delete a Column in Aspose.Cells .NET
linktitle: Delete a Column in Aspose.Cells .NET
second_title: Aspose.Cells .NET Excel Processing API
description: 
type: docs
weight: 19
url: /net/row-and-column-management/delete-column-aspose-cells/
---

## Complete Source Code
```csharp
using System.IO;

using Aspose.Cells;

namespace Aspose.Cells.Examples.CSharp.RowsColumns.InsertingAndDeleting
{
    public class DeletingAColumn
    {
        public static void Run()
        {
            // ExStart:1
            // The path to the documents directory.
            string dataDir = "Your Document Directory";

            // Creating a file stream containing the Excel file to be opened
            FileStream fstream = new FileStream(dataDir + "Book1.xlsx", FileMode.Open);

            // Instantiating a Workbook object
            // Opening the Excel file through the file stream
            Workbook workbook = new Workbook(fstream);

            // Accessing the first worksheet in the Excel file
            Worksheet worksheet = workbook.Worksheets[0];

            // Deleting a column from the worksheet at 5th position
            worksheet.Cells.DeleteColumn(4);

            // Saving the modified Excel file
            workbook.Save(dataDir + "output.xlsx");

            // Closing the file stream to free all resources
            fstream.Close();
            // ExEnd:1

        }
    }
}

```
