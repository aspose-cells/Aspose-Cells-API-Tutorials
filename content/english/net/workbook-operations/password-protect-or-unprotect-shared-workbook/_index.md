---
title: Password Protect or Unprotect Shared Workbook
linktitle: Password Protect or Unprotect Shared Workbook
second_title: Aspose.Cells .NET Excel Processing API
description: 
type: docs
weight: 22
url: /net/workbook-operations/password-protect-or-unprotect-shared-workbook/
---

## Complete Source Code
```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;

namespace Aspose.Cells.Examples.CSharp._Workbook
{
    class PasswordProtectOrUnprotectSharedWorkbook 
    {
        public static void Run()
        {
            //Output directory
            string outputDir = "Your Document Directory";

            //Create empty Excel file
            Workbook wb = new Workbook();

            //Protect the Shared Workbook with Password
            wb.ProtectSharedWorkbook("1234");

            //Uncomment this line to Unprotect the Shared Workbook
            //wb.UnprotectSharedWorkbook("1234");

            //Save the output Excel file
            wb.Save(outputDir + "outputProtectSharedWorkbook.xlsx");

            Console.WriteLine("PasswordProtectOrUnprotectSharedWorkbook executed successfully.\r\n");
        }
    }
}

```
