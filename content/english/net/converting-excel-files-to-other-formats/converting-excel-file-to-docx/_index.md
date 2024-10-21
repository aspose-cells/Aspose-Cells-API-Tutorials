---
title: Converting Excel File to DOCX Programmatically in .NET
linktitle: Converting Excel File to DOCX Programmatically in .NET
second_title: Aspose.Cells .NET Excel Processing API
description: 
type: docs
weight: 11
url: /net/converting-excel-files-to-other-formats/converting-excel-file-to-docx/
---

## Complete Source Code
```csharp
using System;

namespace Aspose.Cells.Examples.CSharp.LoadingSavingConvertingAndManaging
{
    public class ConvertExcelFileToDocx
    {
        public static void Run()
        {
            //Source directory
            string sourceDir = RunExamples.Get_SourceDirectory();

            //Output directory
            string outputDir = RunExamples.Get_OutputDirectory();

            // ExStart:1
            // Open the template file
            Workbook workbook = new Workbook(sourceDir + "Book1.xlsx");

            // Save as Markdown
            workbook.Save(outputDir + "Book1.docx", SaveFormat.Docx);
            // ExEnd:1

            Console.WriteLine("ConvertExcelFileToDocx executed successfully.");
        }
    }
}

```
