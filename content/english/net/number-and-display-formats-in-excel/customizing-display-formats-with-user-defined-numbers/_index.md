---
title: Customizing Display Formats with User-Defined Numbers
linktitle: Customizing Display Formats with User-Defined Numbers
second_title: Aspose.Cells .NET Excel Processing API
description: 
type: docs
weight: 11
url: /net/number-and-display-formats-in-excel/customizing-display-formats-with-user-defined-numbers/
---

## Complete Source Code
```csharp
using System.IO;

using Aspose.Cells;
using System;

namespace Aspose.Cells.Examples.CSharp.Formatting.SettingDisplayFormats
{
    public class UsingCustomNumber
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

            // Adding the current system date to "A1" cell
            worksheet.Cells["A1"].PutValue(DateTime.Now);

            // Getting the style of A1 cell
            Style style = worksheet.Cells["A1"].GetStyle();

            // Setting the custom display format to show date as "d-mmm-yy"
            style.Custom = "d-mmm-yy";

            // Applying the style to A1 cell
            worksheet.Cells["A1"].SetStyle(style);

            // Adding a numeric value to "A2" cell
            worksheet.Cells["A2"].PutValue(20);

            // Getting the style of A2 cell
            style = worksheet.Cells["A2"].GetStyle();

            // Setting the custom display format to show value as percentage
            style.Custom = "0.0%";

            // Applying the style to A2 cell
            worksheet.Cells["A2"].SetStyle(style);

            // Adding a numeric value to "A3" cell
            worksheet.Cells["A3"].PutValue(2546);

            // Getting the style of A3 cell
            style = worksheet.Cells["A3"].GetStyle();

            // Setting the custom display format to show value as currency
            style.Custom = "£#,##0;[Red]$-#,##0";

            // Applying the style to A3 cell
            worksheet.Cells["A3"].SetStyle(style);

            // Saving the Excel file
            workbook.Save(dataDir + "book1.out.xls", SaveFormat.Excel97To2003);
            // ExEnd:1
 
        }
    }
}

```
