---
title: Converting Excel File to Markdown Programmatically in .NET
linktitle: Converting Excel File to Markdown Programmatically in .NET
second_title: Aspose.Cells .NET Excel Processing API
description: 
type: docs
weight: 13
url: /net/converting-excel-files-to-other-formats/converting-excel-file-to-markdown/
---

## Complete Source Code
```csharp
using System;

namespace Aspose.Cells.Examples.CSharp.LoadingSavingConvertingAndManaging
{
    public class ConvertExcelFileToMarkdown
    {
        public static void Run()
        {
            //Source directory
            string sourceDir = "Your Document Directory";

            //Output directory
            string outputDir = "Your Document Directory";

            // ExStart:1
            // Open the template file
            Workbook workbook = new Workbook(sourceDir + "Book1.xlsx");

            // Save as Markdown
            workbook.Save(outputDir + "Book1.md", SaveFormat.Markdown);
            // ExEnd:1

            Console.WriteLine("ConvertExcelFileToMarkdown executed successfully.");
        }
    }
}

```
