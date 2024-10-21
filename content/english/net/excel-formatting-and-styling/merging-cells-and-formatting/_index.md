---
title: Merging Cells and Formatting in Excel
linktitle: Merging Cells and Formatting in Excel
second_title: Aspose.Cells .NET Excel Processing API
description: 
type: docs
weight: 17
url: /net/excel-formatting-and-styling/merging-cells-and-formatting/
---

## Complete Source Code
```csharp
using System.IO;

using Aspose.Cells;

namespace Aspose.Cells.Examples.CSharp.Formatting.ConfiguringAlignmentSettings
{
    public class MergingCells
    {
        public static void Run()
        {
            // ExStart:1
            // The path to the documents directory.
            string dataDir = RunExamples.GetDataDir(System.Reflection.MethodBase.GetCurrentMethod().DeclaringType);

            // Create directory if it is not already present.
            bool IsExists = System.IO.Directory.Exists(dataDir);
            if (!IsExists)
                System.IO.Directory.CreateDirectory(dataDir);

            // Instantiating a Workbook object
            Workbook workbook = new Workbook();

            // Obtaining the reference of the worksheet
            Worksheet worksheet = workbook.Worksheets[0];

            // Accessing the "A1" cell from the worksheet
            Aspose.Cells.Cell cell = worksheet.Cells["A1"];

            // Adding some value to the "A1" cell
            cell.PutValue("Visit Aspose!");

            // Merging the first three columns in the first row to create a single cell
            worksheet.Cells.Merge(0, 0, 1, 3);


            // Saving the Excel file
            workbook.Save(dataDir + "book1.out.xls", SaveFormat.Excel97To2003);
            // ExEnd:1
        }
    }
}

```
