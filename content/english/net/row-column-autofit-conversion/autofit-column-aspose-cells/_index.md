---
title: Auto-fit Column in Aspose.Cells .NET
linktitle: Auto-fit Column in Aspose.Cells .NET
second_title: Aspose.Cells .NET Excel Processing API
description: 
type: docs
weight: 10
url: /net/row-column-autofit-conversion/autofit-column-aspose-cells/
---

## Complete Source Code
```csharp
using System.IO;

using Aspose.Cells;
using System.Drawing;

namespace Aspose.Cells.Examples.CSharp.RowsColumns
{
    public class AutofitColumn
    {
        public static void Run()
        {
            // ExStart:1
            // The path to the documents directory.
            string dataDir = "Your Document Directory";

            string InputPath = dataDir + "Book1.xlsx";

            // Creating a file stream containing the Excel file to be opened
            FileStream fstream = new FileStream(InputPath, FileMode.Open);

            // Opening the Excel file through the file stream
            Workbook workbook = new Workbook(fstream);

            // Accessing the first worksheet in the Excel file
            Worksheet worksheet = workbook.Worksheets[0];

        // Auto-fitting the Column of the worksheet
        worksheet.AutoFitColumn(4);

            // Saving the modified Excel file
            workbook.Save(dataDir  + "output.xlsx");
            // ExEnd:1

        }
    }
}
```
