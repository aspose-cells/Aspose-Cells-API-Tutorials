---
title: Saving Workbook to Strict Open XML Spreadsheet Format in .NET
linktitle: Saving Workbook to Strict Open XML Spreadsheet Format in .NET
second_title: Aspose.Cells .NET Excel Processing API
description: 
type: docs
weight: 19
url: /net/converting-excel-files-to-other-formats/saving-workbook-to-strict-open-xml-spreadsheet-format/
---

## Complete Source Code
```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;

namespace Aspose.Cells.Examples.CSharp.LoadingSavingConvertingAndManaging
{
    class SaveWorkbookToStrictOpenXMLSpreadsheetFormat 
    {
        //Output directory
        static string outputDir = RunExamples.Get_OutputDirectory();

        public static void Main()
        {
            // Create workbook.
            Workbook wb = new Workbook();

            // Specify - Strict Open XML Spreadsheet - Format.
            wb.Settings.Compliance = OoxmlCompliance.Iso29500_2008_Strict;

            // Add message in cell B4 of first worksheet.
            Cell b4 = wb.Worksheets[0].Cells["B4"];
            b4.PutValue("This Excel file has Strict Open XML Spreadsheet format.");

            // Save to output Excel file.
            wb.Save(outputDir + "outputSaveWorkbookToStrictOpenXMLSpreadsheetFormat.xlsx", SaveFormat.Xlsx);

            Console.WriteLine("SaveWorkbookToStrictOpenXMLSpreadsheetFormat executed successfully.");
        }
    }
}

```
