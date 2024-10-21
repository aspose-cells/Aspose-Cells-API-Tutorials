---
title: Changing Font Size in Excel
linktitle: Changing Font Size in Excel
second_title: Aspose.Cells .NET Excel Processing API
description: 
type: docs
weight: 12
url: /net/working-with-fonts-in-excel/changing-font-size/
---

## Complete Source Code
```csharp
using System.IO;

using Aspose.Cells;

namespace Aspose.Cells.Examples.CSharp.Formatting.DealingWithFontSettings
{
    public class SettingFontSize
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

            // Adding a new worksheet to the Excel object
            int i = workbook.Worksheets.Add();

            // Obtaining the reference of the newly added worksheet by passing its sheet index
            Worksheet worksheet = workbook.Worksheets[i];

            // Accessing the "A1" cell from the worksheet
            Aspose.Cells.Cell cell = worksheet.Cells["A1"];

            // Adding some value to the "A1" cell
            cell.PutValue("Hello Aspose!");

            // Obtaining the style of the cell
            Style style = cell.GetStyle();
            // ExStart:SetFontSize
            // Setting the font size to 14
            style.Font.Size = 14;
            // ExEnd:SetFontSize
            // Applying the style to the cell
            cell.SetStyle(style);

            // Saving the Excel file
            workbook.Save(dataDir + "book1.out.xls", SaveFormat.Excel97To2003);
            // ExEnd:1

        }
    }
}

```
