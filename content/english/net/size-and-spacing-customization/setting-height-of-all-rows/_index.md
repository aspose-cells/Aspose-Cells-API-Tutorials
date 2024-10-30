---
title: Set Height of All Rows in Excel with Aspose.Cells
linktitle: Set Height of All Rows in Excel with Aspose.Cells
second_title: Aspose.Cells .NET Excel Processing API
description: 
type: docs
weight: 12
url: /net/size-and-spacing-customization/setting-height-of-all-rows/
---

## Complete Source Code
```csharp
using System.IO;

using Aspose.Cells;

namespace Aspose.Cells.Examples.CSharp.RowsColumns.HeightAndWidth
{
    public class SettingHeightAllRows
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

            // Setting the height of all rows in the worksheet to 15
            worksheet.Cells.StandardHeight = 15;

            // Saving the modified Excel file
            workbook.Save(dataDir + "output.out.xls");

            // Closing the file stream to free all resources
            fstream.Close();
            // ExEnd:1
            
        }
    }
}

```
