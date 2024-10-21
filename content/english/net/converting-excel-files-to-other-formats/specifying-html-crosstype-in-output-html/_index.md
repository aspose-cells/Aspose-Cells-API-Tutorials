---
title: Specifying HTML CrossType in Output HTML Programmatically in .NET
linktitle: Specifying HTML CrossType in Output HTML Programmatically in .NET
second_title: Aspose.Cells .NET Excel Processing API
description: 
type: docs
weight: 17
url: /net/converting-excel-files-to-other-formats/specifying-html-crosstype-in-output-html/
---

## Complete Source Code
```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;

namespace Aspose.Cells.Examples.CSharp.LoadingSavingConvertingAndManaging
{
    class SpecifyHtmlCrossTypeInOutputHTML
    {
        public static void Run()
        {
            //Source directory
            string sourceDir = RunExamples.Get_SourceDirectory();

            //Output directory
            string outputDir = RunExamples.Get_OutputDirectory();

            //Load the sample Excel file
            Workbook wb = new Workbook(sourceDir + "sampleHtmlCrossStringType.xlsx");

            //Specify HTML Cross Type
            HtmlSaveOptions opts = new HtmlSaveOptions();
            opts.HtmlCrossStringType = HtmlCrossType.Default;
            opts.HtmlCrossStringType = HtmlCrossType.MSExport;
            opts.HtmlCrossStringType = HtmlCrossType.Cross;
            opts.HtmlCrossStringType = HtmlCrossType.FitToCell;

            //Output Html
            wb.Save(outputDir + "out" + opts.HtmlCrossStringType + ".htm", opts);

            Console.WriteLine("SpecifyHtmlCrossTypeInOutputHTML executed successfully.\r\n");
        }
    }
}

```
