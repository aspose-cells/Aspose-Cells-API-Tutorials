---
title: Password Protect Or Unprotect Shared Workbook
linktitle: Password Protect Or Unprotect Shared Workbook
second_title: Aspose.Cells for .NET API Reference
description: 
type: docs
weight: 120
url: /net/excel-workbook/password-protect-or-unprotect-shared-workbook/
---
### Sample source code for Password Protect Or Unprotect Shared Workbook using Aspose.Cells for .NET 
```csharp
            //Output directory
            string outputDir = RunExamples.Get_OutputDirectory();
            //Create empty Excel file
            Workbook wb = new Workbook();
            //Protect the Shared Workbook with Password
            wb.ProtectSharedWorkbook("1234");
            //Uncomment this line to Unprotect the Shared Workbook
            //wb.UnprotectSharedWorkbook("1234");
            //Save the output Excel file
            wb.Save(outputDir + "outputProtectSharedWorkbook.xlsx");
            Console.WriteLine("PasswordProtectOrUnprotectSharedWorkbook executed successfully.\r\n");
```