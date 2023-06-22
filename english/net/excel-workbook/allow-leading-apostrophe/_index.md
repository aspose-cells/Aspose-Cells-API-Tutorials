---
title: Allow Leading Apostrophe
linktitle: Allow Leading Apostrophe
second_title: Aspose.Cells for .NET API Reference
description: 
type: docs
weight: 60
url: /net/excel-workbook/allow-leading-apostrophe/
---
### Sample source code for Allow Leading Apostrophe using Aspose.Cells for .NET 
```csharp
            //Source directory
            string sourceDir = RunExamples.Get_SourceDirectory();
            string outputDir = RunExamples.Get_OutputDirectory();
            // Instantiating a WorkbookDesigner object
            WorkbookDesigner designer = new WorkbookDesigner();
            Workbook workbook = new Workbook(sourceDir + "AllowLeadingApostropheSample.xlsx");
            workbook.Settings.QuotePrefixToStyle = false;
            // Open a designer spreadsheet containing smart markers
            designer.Workbook = workbook;
            List<DataObject> list = new List<DataObject>
            {
                new DataObject
                {
                     Id =1,
                     Name = "demo"
                },
                new DataObject
                {
                    Id=2,
                    Name = "'demo"
                }
            };
            // Set the data source for the designer spreadsheet
            designer.SetDataSource("sampleData", list);
            // Process the smart markers
            designer.Process();
            designer.Workbook.Save(outputDir + "AllowLeadingApostropheSample_out.xlsx");
            Console.WriteLine("AllowLeadingApostrophe executed successfully.");
```