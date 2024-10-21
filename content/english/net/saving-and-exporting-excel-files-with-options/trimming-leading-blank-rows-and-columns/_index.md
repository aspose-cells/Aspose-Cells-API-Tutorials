---
title: Trimming Leading Blank Rows and Columns while Exporting
linktitle: Trimming Leading Blank Rows and Columns while Exporting
second_title: Aspose.Cells .NET Excel Processing API
description: 
type: docs
weight: 13
url: /net/saving-and-exporting-excel-files-with-options/trimming-leading-blank-rows-and-columns/
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
    public class TrimLeadingBlankRowsAndColumnsWhileExportingSpreadsheetsToCSVFormat
    {
        public static void Run()
        {
            // ExStart:TrimLeadingBlankRowsAndColumnsWhileExportingSpreadsheetsToCSVFormat
            // The path to the documents directory.
            string dataDir = RunExamples.GetDataDir(System.Reflection.MethodBase.GetCurrentMethod().DeclaringType);

            //Load source worbook
            Workbook wb = new Workbook(dataDir + "sampleTrimBlankColumns.xlsx");

            //Save in csv format
            wb.Save(dataDir + "outputWithoutTrimBlankColumns.csv");

            //Now save again with TrimLeadingBlankRowAndColumn as true
            TxtSaveOptions opts = new TxtSaveOptions();
            opts.TrimLeadingBlankRowAndColumn = true;

            //Save in csv format
            wb.Save(dataDir + "outputTrimBlankColumns.csv", opts);

            // ExEnd:TrimLeadingBlankRowsAndColumnsWhileExportingSpreadsheetsToCSVFormat
        }
    }
}

```
