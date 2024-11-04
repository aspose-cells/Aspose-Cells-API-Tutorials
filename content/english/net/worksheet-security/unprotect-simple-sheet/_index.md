---
title: Unprotect Simple Sheet using Aspose.Cells
linktitle: Unprotect Simple Sheet using Aspose.Cells
second_title: Aspose.Cells .NET Excel Processing API
description: 
type: docs
weight: 22
url: /net/worksheet-security/unprotect-simple-sheet/
---

## Complete Source Code
```csharp
using System.IO;

using Aspose.Cells;

namespace Aspose.Cells.Examples.CSharp.Worksheets.Security.Unprotect
{
    public class UnprotectSimpleSheet
    {
    
        public static void Run()
        {
            // ExStart:1
            // The path to the documents directory.
            string dataDir = "Your Document Directory";

            // Instantiating a Workbook object
            Workbook workbook = new Workbook(dataDir + "book1.xls");

            // Accessing the first worksheet in the Excel file
            Worksheet worksheet = workbook.Worksheets[0];
            
            // Unprotecting the worksheet without a password
            worksheet.Unprotect();

            // Saving the Workbook
            workbook.Save(dataDir + "output.out.xls", SaveFormat.Excel97To2003);
            // ExEnd:1

        }
    }
}

```
