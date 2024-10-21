---
title: Tracking Document Conversion Progress Programmatically in .NET
linktitle: Tracking Document Conversion Progress Programmatically in .NET
second_title: Aspose.Cells .NET Excel Processing API
description: 
type: docs
weight: 20
url: /net/converting-excel-files-to-other-formats/tracking-document-conversion-progress/
---

## Complete Source Code
```csharp
using Aspose.Cells.Rendering;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;

namespace Aspose.Cells.Examples.CSharp.LoadingSavingConvertingAndManaging 
{
    public class DocumentConversionProgress
    {
        public static void Run()
        {
            // ExStart:1
            //Source directory
            string sourceDir = RunExamples.Get_SourceDirectory();

            //Output directory
            string outputDir = RunExamples.Get_OutputDirectory();

            Workbook workbook = new Workbook(sourceDir + "PagesBook1.xlsx");

            PdfSaveOptions pdfSaveOptions = new PdfSaveOptions();
            pdfSaveOptions.PageSavingCallback = new TestPageSavingCallback();

            workbook.Save(outputDir + "DocumentConversionProgress.pdf", pdfSaveOptions);
            // ExEnd:1

            Console.WriteLine("DocumentConversionProgress executed successfully.");
        }
    }

    // ExStart:2
    public class TestPageSavingCallback : IPageSavingCallback
    {
        public void PageStartSaving(PageStartSavingArgs args)
        {
            Console.WriteLine("Start saving page index {0} of pages {1}", args.PageIndex, args.PageCount);

            //don't output pages before page index 2.
            if (args.PageIndex < 2)
            {
                args.IsToOutput = false;
            }
        }

        public void PageEndSaving(PageEndSavingArgs args)
        {
            Console.WriteLine("End saving page index {0} of pages {1}", args.PageIndex, args.PageCount);

            //don't output pages after page index 8.
            if (args.PageIndex >= 8)
            {
                args.HasMorePages = false;
            }
        }
    }
    // ExEnd:2
}

```
