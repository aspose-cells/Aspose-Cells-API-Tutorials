---
title: Specify Author while Write Protecting Workbook using Aspose.Cells
linktitle: Specify Author while Write Protecting Workbook using Aspose.Cells
second_title: Aspose.Cells .NET Excel Processing API
description: 
type: docs
weight: 26
url: /net/worksheet-security/specify-author-write-protect-workbook/
---

## Complete Source Code
```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;

namespace Aspose.Cells.Examples.CSharp.Worksheets.Security
{
    class SpecifyAuthorWhileWriteProtectingWorkbook
    {
        //Source directory
        static string sourceDir = "Your Document Directory";

        //Output directory
        static string outputDir = "Your Document Directory";

        public static void Main()
        {
            // Create empty workbook.
            Workbook wb = new Workbook();

            // Write protect workbook with password.
            wb.Settings.WriteProtection.Password = "1234";

            // Specify author while write protecting workbook.
            wb.Settings.WriteProtection.Author = "SimonAspose";

            // Save the workbook in XLSX format.
            wb.Save(outputDir + "outputSpecifyAuthorWhileWriteProtectingWorkbook.xlsx");

            Console.WriteLine("SpecifyAuthorWhileWriteProtectingWorkbook executed successfully.");
        }
    }
}

```
