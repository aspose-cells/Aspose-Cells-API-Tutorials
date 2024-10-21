---
title: Using Built-In Number Formats in Excel Programmatically
linktitle: Using Built-In Number Formats in Excel Programmatically
second_title: Aspose.Cells .NET Excel Processing API
description: 
type: docs
weight: 10
url: /net/number-and-display-formats-in-excel/using-built-in-number-formats/
---

## Complete Source Code
```csharp
using System.IO;

using Aspose.Cells;
using System;

namespace Aspose.Cells.Examples.CSharp.Formatting.SettingDisplayFormats
{
    public class UsingBuiltInNumberFormats
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

            // Obtaining the reference of first worksheet
            Worksheet worksheet = workbook.Worksheets[0];

            // Adding the current system date to "A1" cell
            worksheet.Cells["A1"].PutValue(DateTime.Now);

            // Getting the Style of the A1 Cell
            Style style = worksheet.Cells["A1"].GetStyle();

            // Setting the display format to number 15 to show date as "d-mmm-yy"
            style.Number = 15;

            // Applying the style to the A1 cell
            worksheet.Cells["A1"].SetStyle(style);

            // Adding a numeric value to "A2" cell
            worksheet.Cells["A2"].PutValue(20);

            // Getting the Style of the A2 Cell
            style = worksheet.Cells["A2"].GetStyle();

            // Setting the display format to number 9 to show value as percentage
            style.Number = 9;

            // Applying the style to the A2 cell
            worksheet.Cells["A2"].SetStyle(style);

            // Adding a numeric value to "A3" cell
            worksheet.Cells["A3"].PutValue(2546);

            // Getting the Style of the A3 Cell
            style = worksheet.Cells["A3"].GetStyle();

            // Setting the display format to number 6 to show value as currency
            style.Number = 6;

            // Applying the style to the A3 cell
            worksheet.Cells["A3"].SetStyle(style);

            // Saving the Excel file
            workbook.Save(dataDir + "book1.out.xls", SaveFormat.Excel97To2003);
            // ExEnd:1
 
        }
    }
}

```
