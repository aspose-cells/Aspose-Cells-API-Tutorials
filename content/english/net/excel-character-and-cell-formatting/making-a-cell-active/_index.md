---
title: Making a Cell Active Programmatically in Excel
linktitle: Making a Cell Active Programmatically in Excel
second_title: Aspose.Cells .NET Excel Processing API
description: 
type: docs
weight: 11
url: /net/excel-character-and-cell-formatting/making-a-cell-active/
---

## Complete Source Code
```csharp
using System.IO;

using Aspose.Cells;
using System.Drawing;

namespace Aspose.Cells.Examples.CSharp.Formatting
{
    public class MakeCellActive
    {
        public static void Run()
        {
            // ExStart:1
            // The path to the documents directory.
            string dataDir = RunExamples.GetDataDir(System.Reflection.MethodBase.GetCurrentMethod().DeclaringType);

            // Instantiate a new Workbook.
            Workbook workbook = new Workbook();

            // Get the first worksheet in the workbook.
            Worksheet worksheet1 = workbook.Worksheets[0];

            // Get the cells in the worksheet.
            Cells cells = worksheet1.Cells;

            // Input data into B2 cell.
            cells[1, 1].PutValue("Hello World!");

            // Set the first sheet as an active sheet.
            workbook.Worksheets.ActiveSheetIndex = 0;

            // Set B2 cell as an active cell in the worksheet.
            worksheet1.ActiveCell = "B2";

            // Set the B column as the first visible column in the worksheet.
            worksheet1.FirstVisibleColumn = 1;

            // Set the 2nd row as the first visible row in the worksheet.
            worksheet1.FirstVisibleRow = 1;

            // Save the excel file.
            workbook.Save(dataDir + "output.xls");
                     
            // ExEnd:1

        }
    }
}
```
