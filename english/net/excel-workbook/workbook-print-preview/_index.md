---
title: Workbook Print Preview
linktitle: Workbook Print Preview
second_title: Aspose.Cells for .NET API Reference
description: 
type: docs
weight: 170
url: /net/excel-workbook/workbook-print-preview/
---
### Sample source code for Workbook Print Preview using Aspose.Cells for .NET 
```csharp
            //Source directory
            string sourceDir = RunExamples.Get_SourceDirectory();
            Workbook workbook = new Workbook(sourceDir + "Book1.xlsx");
            ImageOrPrintOptions imgOptions = new ImageOrPrintOptions();
            WorkbookPrintingPreview preview = new WorkbookPrintingPreview(workbook, imgOptions);
            Console.WriteLine("Workbook page count: " + preview.EvaluatedPageCount);
            SheetPrintingPreview preview2 = new SheetPrintingPreview(workbook.Worksheets[0], imgOptions);
            Console.WriteLine("Worksheet page count: " + preview2.EvaluatedPageCount);
            Console.WriteLine("PrintPreview executed successfully.");
```