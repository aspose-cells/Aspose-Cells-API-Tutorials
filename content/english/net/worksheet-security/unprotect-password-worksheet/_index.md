---
title: Unprotect Password Protected Worksheet using Aspose.Cells
linktitle: Unprotect Password Protected Worksheet using Aspose.Cells
second_title: Aspose.Cells .NET Excel Processing API
description: 
type: docs
weight: 19
url: /net/worksheet-security/unprotect-password-worksheet/
---

## Complete Source Code
```csharp
using System.IO;
using System;
using Aspose.Cells;

namespace Aspose.Cells.Examples.CSharp.Worksheets.Security.Unprotect
{
    public class UnprotectingPasswordProtectedWorksheet
    {
        public static void Run()
        {
            try
            {
                // ExStart:1
                // The path to the documents directory.
                string dataDir = "Your Document Directory";

                // Instantiating a Workbook object
                Workbook workbook = new Workbook(dataDir + "book1.xls");

                // Accessing the first worksheet in the Excel file
                Worksheet worksheet = workbook.Worksheets[0];

                // Unprotecting the worksheet with a password
                worksheet.Unprotect("");

                // Save Workbook
                workbook.Save(dataDir + "output.out.xls");
                // ExEnd:1
            }
            catch (Exception ex)
            {
                Console.WriteLine(ex.Message);
                Console.ReadLine();
            }

        }
    }
}

```
