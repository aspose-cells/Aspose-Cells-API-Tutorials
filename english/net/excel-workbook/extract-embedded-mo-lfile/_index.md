---
title: Extract Embedded Mo Lfile
linktitle: Extract Embedded Mo Lfile
second_title: Aspose.Cells for .NET API Reference
description: 
type: docs
weight: 90
url: /net/excel-workbook/extract-embedded-mo-lfile/
---
### Sample source code for Extract Embedded Mo Lfile using Aspose.Cells for .NET 
```csharp
            //directories
            string SourceDir = RunExamples.Get_SourceDirectory();
            string outputDir = RunExamples.Get_OutputDirectory();
            Workbook workbook = new Workbook(SourceDir + "EmbeddedMolSample.xlsx");
            var index = 1;
            foreach (Worksheet sheet in workbook.Worksheets)
            {
                OleObjectCollection oles = sheet.OleObjects;
                foreach (OleObject ole in oles)
                {
                    string fileName = outputDir + "OleObject" + index + ".mol ";
                    FileStream fs = File.Create(fileName);
                    fs.Write(ole.ObjectData, 0, ole.ObjectData.Length);
                    fs.Close();
                    index++;
                }
            }
            Console.WriteLine("ExtractEmbeddedMolFile executed successfully.");
```