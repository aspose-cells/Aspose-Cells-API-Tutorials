---
title: Auto-Fit Columns and Rows while Loading HTML in Workbook
linktitle: Auto-Fit Columns and Rows while Loading HTML in Workbook
second_title: Aspose.Cells .NET Excel Processing API
description: 
type: docs
weight: 10
url: /net/loading-and-saving-excel-files-with-options/auto-fitting-columns-and-rows/
---

## Complete Source Code
```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.IO;

namespace Aspose.Cells.Examples.CSharp.LoadingSavingConvertingAndManaging
{
    public class AutoFitColumnsandRowsWhileLoadingHTMLInWorkbook
    {
        public static void Run()
        {
            // ExStart:1
            // The path to the documents directory.
            string dataDir = "Your Document Directory";

            //Sample HTML.
            string sampleHtml = "<html><body><table><tr><td>This is sample text.</td><td>Some text.</td></tr><tr><td>This is another sample text.</td><td>Some text.</td></tr></table></body></html>";

            //Load html string into memory stream.
            MemoryStream ms = new MemoryStream(Encoding.UTF8.GetBytes(sampleHtml));

            //Load memory stream into workbook.
            Workbook wb = new Workbook(ms);

            //Save the workbook in xlsx format.
            wb.Save(dataDir + "outputWithout_AutoFitColsAndRows.xlsx");

            //Specify the HTMLLoadOptions and set AutoFitColsAndRows = true.
            HtmlLoadOptions opts = new HtmlLoadOptions();
            opts.AutoFitColsAndRows = true;

            //Load memory stream into workbook with the above HTMLLoadOptions.
            wb = new Workbook(ms, opts);

            //Save the workbook in xlsx format.
            wb.Save(dataDir + "outputWith_AutoFitColsAndRows.xlsx");
            // ExEnd:1
        }
    }
}

```
