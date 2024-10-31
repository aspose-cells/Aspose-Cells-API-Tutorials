---
title: Auto-fit Row in Specific Range Aspose.Cells .NET
linktitle: Auto-fit Row in Specific Range Aspose.Cells .NET
second_title: Aspose.Cells .NET Excel Processing API
description: 
type: docs
weight: 12
url: /net/row-column-autofit-conversion/autofit-row-specific-range/
---

## Complete Source Code
```csharp
using System.IO;

using Aspose.Cells;
using System.Drawing;

namespace Aspose.Cells.Examples.CSharp.RowsColumns
{
    public class AutofitRowinSpecificRange
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

            // Auto-fitting the 3rd row of the worksheet
            worksheet.AutoFitRow(1, 0, 5);

            // Saving the modified Excel file
            workbook.Save(dataDir  + "output.xlsx");

            // Closing the file stream to free all resources
            fstream.Close();
            // ExEnd:1

        }
    }
}
```