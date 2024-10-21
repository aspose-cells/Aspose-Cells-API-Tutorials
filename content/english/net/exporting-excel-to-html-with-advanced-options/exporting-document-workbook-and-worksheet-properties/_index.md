---
title: Exporting Document Workbook and Worksheet Properties in HTML
linktitle: Exporting Document Workbook and Worksheet Properties in HTML
second_title: Aspose.Cells .NET Excel Processing API
description: 
type: docs
weight: 11
url: /net/exporting-excel-to-html-with-advanced-options/exporting-document-workbook-and-worksheet-properties/
---

## Complete Source Code
```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;

namespace Aspose.Cells.Examples.CSharp.HTML
{
    class ExportDocumentWorkbookAndWorksheetPropertiesInHTML
    {
        public static void Run()
        {
            //Source directory
            string sourceDir = RunExamples.Get_SourceDirectory();

            //Output directory
            string outputDir = RunExamples.Get_OutputDirectory();

            //Load the sample Excel file
            Workbook workbook = new Workbook(sourceDir + "sampleExportDocumentWorkbookAndWorksheetPropertiesInHTML.xlsx");

            //Specify Html Save Options
            HtmlSaveOptions options = new HtmlSaveOptions();

            //We do not want to export document, workbook and worksheet properties
            options.ExportDocumentProperties = false;
            options.ExportWorkbookProperties = false;
            options.ExportWorksheetProperties = false;

            //Export the Excel file to Html with Html Save Options
            workbook.Save(outputDir + "outputExportDocumentWorkbookAndWorksheetPropertiesInHTML.html", options);

            Console.WriteLine("ExportDocumentWorkbookAndWorksheetPropertiesInHTML executed successfully.");
        }
    }
}

```
