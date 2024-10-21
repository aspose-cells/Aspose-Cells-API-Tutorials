---
title: Formatting Selected Characters in Excel
linktitle: Formatting Selected Characters in Excel
second_title: Aspose.Cells .NET Excel Processing API
description: 
type: docs
weight: 10
url: /net/excel-character-and-cell-formatting/formatting-selected-characters/
---

## Complete Source Code
```csharp
using System.IO;

using Aspose.Cells;
using System.Drawing;

namespace Aspose.Cells.Examples.CSharp.Formatting
{
    public class FormattingSelectedCharacters
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

            // Obtaining the reference of the first(default) worksheet by passing its sheet index
            Worksheet worksheet = workbook.Worksheets[0];

            // Accessing the "A1" cell from the worksheet
            Cell cell = worksheet.Cells["A1"];

            // Adding some value to the "A1" cell
            cell.PutValue("Visit Aspose!");

            // Setting the font of selected characters to bold
            cell.Characters(6, 7).Font.IsBold = true;

            // Setting the font color of selected characters to blue
            cell.Characters(6, 7).Font.Color = Color.Blue;

            // Saving the Excel file
            workbook.Save(dataDir + "book1.out.xls");
            // ExEnd:1

        }
    }
}

```
