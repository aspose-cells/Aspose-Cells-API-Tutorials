---
title: Import Data to Excel with Custom DB Num Pattern Formatting
linktitle: Import Data to Excel with Custom DB Num Pattern Formatting
second_title: Aspose.Cells .NET Excel Processing API
description: 
type: docs
weight: 10
url: /net/excel-data-import-export/import-data-to-worksheet-in-excel-with-specified-db-num-custom-pattern-formatting/
---

## Complete Source Code
```csharp
using System;
using System.IO;

using Aspose.Cells;
using System.Drawing;

namespace Aspose.Cells.Examples.CSharp.Data
{
    public class SpecifyingDBNumCustomPatternFormatting
    {
        public static void Run()
        {
            //ExStart:SpecifyingDBNumCustomPatternFormatting

            //The path to the documents directory.
            string dataDir = RunExamples.GetDataDir(System.Reflection.MethodBase.GetCurrentMethod().DeclaringType);
			
			//Create a workbook.
			Workbook wb = new Workbook();
			 
			//Access first worksheet.
			Worksheet ws = wb.Worksheets[0];
			 
			//Access cell A1 and put value 123.
			Cell cell = ws.Cells["A1"];
			cell.PutValue(123);
			 
			//Access cell style.
			Style st = cell.GetStyle();
			 
			//Specifying DBNum custom pattern formatting.
			st.Custom = "[DBNum2][$-804]General";
			 
			//Set the cell style.
			cell.SetStyle(st);
			 
			//Set the first column width.
			ws.Cells.SetColumnWidth(0, 30);
			 
			//Save the workbook in output pdf format.
			wb.Save(dataDir + "outputDBNumCustomFormatting.pdf", SaveFormat.Pdf);

            //ExEnd:SpecifyingDBNumCustomPatternFormatting
        }
    }
}
```
