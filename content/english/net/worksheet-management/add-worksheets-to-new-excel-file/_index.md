---
title: Add Worksheets to New Excel File using Aspose.Cells
linktitle: Add Worksheets to New Excel File using Aspose.Cells
second_title: Aspose.Cells .NET Excel Processing API
description: 
type: docs
weight: 12
url: /net/worksheet-management/add-worksheets-to-new-excel-file/
---

## Complete Source Code
```csharp
using System.IO;

using Aspose.Cells;

namespace Aspose.Cells.Examples.CSharp.Worksheets.Management
{
    public class AddingWorksheetsToNewExcelFile
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

            // Instantiating a Workbook object
            Workbook workbook = new Workbook();

            // Adding a new worksheet to the Workbook object
            int i = workbook.Worksheets.Add();

            // Obtaining the reference of the newly added worksheet by passing its sheet index
            Worksheet worksheet = workbook.Worksheets[i];

            // Setting the name of the newly added worksheet
            worksheet.Name = "My Worksheet";

            // Saving the Excel file
            workbook.Save(dataDir + "output.out.xls");
            // ExEnd:1
        }
    }
}

```
