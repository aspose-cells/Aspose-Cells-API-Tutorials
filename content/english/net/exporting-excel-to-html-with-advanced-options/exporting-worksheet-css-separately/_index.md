---
title: Exporting Worksheet CSS Separately in Output HTML
linktitle: Exporting Worksheet CSS Separately in Output HTML
second_title: Aspose.Cells .NET Excel Processing API
description: 
type: docs
weight: 14
url: /net/exporting-excel-to-html-with-advanced-options/exporting-worksheet-css-separately/
---

## Complete Source Code
```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;

using System.Drawing;

namespace Aspose.Cells.Examples.CSharp.HTML
{
    class ExportWorksheetCSSSeparatelyInOutputHTML 
    {
        public static void Run()
        {
            //Output directory
            string outputDir = RunExamples.Get_OutputDirectory();

            //Create workbook object
            Workbook wb = new Workbook();

            //Access first worksheet
            Worksheet ws = wb.Worksheets[0];

            //Access cell B5 and put value inside it
            Cell cell = ws.Cells["B5"];
            cell.PutValue("This is some text.");

            //Set the style of the cell - font color is Red
            Style st = cell.GetStyle();
            st.Font.Color = Color.Red;
            cell.SetStyle(st);

            //Specify html save options - export worksheet css separately
            HtmlSaveOptions opts = new HtmlSaveOptions();
            opts.ExportWorksheetCSSSeparately = true;

            //Save the workbook in html 
            wb.Save(outputDir + "outputExportWorksheetCSSSeparately.html", opts);

            Console.WriteLine("ExportWorksheetCSSSeparatelyInOutputHTML executed successfully.");
        }
    }
}

```
