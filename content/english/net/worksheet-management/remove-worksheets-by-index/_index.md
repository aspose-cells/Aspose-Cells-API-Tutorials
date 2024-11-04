---
title: Remove Worksheets by Index using Aspose.Cells
linktitle: Remove Worksheets by Index using Aspose.Cells
second_title: Aspose.Cells .NET Excel Processing API
description: 
type: docs
weight: 14
url: /net/worksheet-management/remove-worksheets-by-index/
---

## Complete Source Code
```csharp
using System.IO;

using Aspose.Cells;

namespace Aspose.Cells.Examples.CSharp.Worksheets.Management
{
    public class RemovingWorksheetsUsingSheetIndex
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

            // Removing a worksheet using its sheet index
            workbook.Worksheets.RemoveAt(0);

            // Save workbook
            workbook.Save(dataDir + "output.out.xls");
            // ExEnd:1
            
        }
    }
}

```
