---
title: Shrinking Text to Fit Cell Size in Excel
linktitle: Shrinking Text to Fit Cell Size in Excel
second_title: Aspose.Cells .NET Excel Processing API
description: 
type: docs
weight: 19
url: /net/excel-formatting-and-styling/shrinking-text-to-fit-cell-size/
---

## Complete Source Code
```csharp
using System.IO;

using Aspose.Cells;

namespace Aspose.Cells.Examples.CSharp.Formatting.ConfiguringAlignmentSettings
{
    public class ShrinkingToFit
    {
        public static void Run()
        {
            // ExStart:1
            // The path to the documents directory.
            string dataDir = "Your Document Directory";

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

            // Setting the horizontal alignment of the text in the "A1" cell
            Style style = cell.GetStyle();

            // Shrinking the text to fit according to the dimensions of the cell
            style.ShrinkToFit = true;

            cell.SetStyle(style);

            // Saving the Excel file
            workbook.Save(dataDir + "book1.out.xls", SaveFormat.Excel97To2003);
            // ExEnd:1
        }
    }
}

```
