---
title: Create Shared Workbook
linktitle: Create Shared Workbook
second_title: Aspose.Cells for .NET API Reference
description: 
type: docs
weight: 70
url: /net/excel-workbook/create-shared-workbook/
---
### Sample source code for Create Shared Workbook using Aspose.Cells for .NET 
```csharp
            //Output directory
            string outputDir = RunExamples.Get_OutputDirectory();
            //Create Workbook object
            Workbook wb = new Workbook();
            //Share the Workbook
            wb.Settings.Shared = true;
            //Save the Shared Workbook
            wb.Save(outputDir + "outputSharedWorkbook.xlsx");
            Console.WriteLine("CreateSharedWorkbook executed successfully.\r\n");
```