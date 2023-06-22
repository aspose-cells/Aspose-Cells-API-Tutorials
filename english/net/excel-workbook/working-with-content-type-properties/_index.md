---
title: Working With Content Type Properties
linktitle: Working With Content Type Properties
second_title: Aspose.Cells for .NET API Reference
description: 
type: docs
weight: 180
url: /net/excel-workbook/working-with-content-type-properties/
---
### Sample source code for Working With Content Type Properties using Aspose.Cells for .NET 
```csharp
            //source directory
            string outputDir = RunExamples.Get_OutputDirectory();
            Workbook workbook = new Workbook(FileFormatType.Xlsx);
            int index = workbook.ContentTypeProperties.Add("MK31", "Simple Data");
            workbook.ContentTypeProperties[index].IsNillable = false;
            index = workbook.ContentTypeProperties.Add("MK32", DateTime.Now.ToString("yyyy-MM-dd'T'hh:mm:ss"), "DateTime");
            workbook.ContentTypeProperties[index].IsNillable = true;
            workbook.Save(outputDir + "WorkingWithContentTypeProperties_out.xlsx");
            Console.WriteLine("WorkingWithContentTypeProperties executed successfully.");
```