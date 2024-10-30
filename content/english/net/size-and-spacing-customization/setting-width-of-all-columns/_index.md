---
title: Set Width of All Columns with Aspose.Cells for .NET
linktitle: Set Width of All Columns with Aspose.Cells for .NET
second_title: Aspose.Cells .NET Excel Processing API
description: 
type: docs
weight: 17
url: /net/size-and-spacing-customization/setting-width-of-all-columns/
---

## Complete Source Code
```csharp
using System.IO;

using Aspose.Cells;

namespace Aspose.Cells.Examples.CSharp.RowsColumns.HeightAndWidth
{
    public class SetWidthAllColumns
    {
        public static void Run()
        {
            // ExStart:1
            // The path to the documents directory.
            string dataDir = "Your Document Directory";
            
           // Create directory if it is not already present.
            bool IsExists = System.IO.Directory.Exists(dataDir);
            if (!IsExists)
                System.IO.Directory.CreateDirectory(dataDir);

            // Creating a file stream containing the Excel file to be opened
            FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);

            // Instantiating a Workbook object
            // Opening the Excel file through the file stream
            Workbook workbook = new Workbook(fstream);

            // Accessing the first worksheet in the Excel file
            Worksheet worksheet = workbook.Worksheets[0];

            // Setting the width of all columns in the worksheet to 20.5
            worksheet.Cells.StandardWidth = 20.5;

            // Saving the modified Excel file
            workbook.Save(dataDir + "output.out.xls");

            // Closing the file stream to free all resources
            fstream.Close(); 
            // ExEnd:1
        }
    }
}

```
