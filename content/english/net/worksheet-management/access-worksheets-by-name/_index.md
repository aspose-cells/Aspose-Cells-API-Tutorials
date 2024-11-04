---
title: Access Worksheets by Name using Aspose.Cells
linktitle: Access Worksheets by Name using Aspose.Cells
second_title: Aspose.Cells .NET Excel Processing API
description: 
type: docs
weight: 10
url: /net/worksheet-management/access-worksheets-by-name/
---

## Complete Source Code
```csharp
using System.IO;

using Aspose.Cells;
using System;

namespace Aspose.Cells.Examples.CSharp.Worksheets.Management
{
    public class AccessingWorksheetsusingSheetName
    {
        public static void Run()
        {
            // ExStart:1
            // The path to the documents directory.
            string dataDir = "Your Document Directory";

            string InputPath = dataDir + "book1.xlsx";

            // Creating a file stream containing the Excel file to be opened
            FileStream fstream = new FileStream(InputPath, FileMode.Open);

            // Instantiating a Workbook object
            // Opening the Excel file through the file stream
            Workbook workbook = new Workbook(fstream);

            // Accessing a worksheet using its sheet name
            Worksheet worksheet = workbook.Worksheets["Sheet1"];
            Cell cell = worksheet.Cells["A1"];
            Console.WriteLine(cell.Value);
            // ExEnd:1
        }
    }
}

```
