---
title: Copy Named Ranges in Excel
linktitle: Copy Named Ranges in Excel
second_title: Aspose.Cells .NET Excel Processing API
description: 
type: docs
weight: 10
url: /net/excel-managing-named-ranges/copy-named-ranges/
---

## Complete Source Code
```csharp
using System;
using System.IO;

using Aspose.Cells;
using System.Drawing;

namespace Aspose.Cells.Examples.CSharp.Data
{
    public class CopyNamedRanges
    {
        //Output directory
        static string outputDir = RunExamples.Get_OutputDirectory();

        public static void Run()
        {
            // Instantiate a new Workbook.
            Workbook workbook = new Workbook();

            // Get all the worksheets in the book.
            WorksheetCollection worksheets = workbook.Worksheets;

            // Get the first worksheet in the worksheets collection.
            Worksheet worksheet = workbook.Worksheets[0];

            // Create a range of cells.
            Range range1 = worksheet.Cells.CreateRange("E12", "I12");

            // Name the range.
            range1.Name = "MyRange";

            // Set the outline border to the range.
            range1.SetOutlineBorder(BorderType.TopBorder, CellBorderType.Medium, Color.FromArgb(0, 0, 128));
            range1.SetOutlineBorder(BorderType.BottomBorder, CellBorderType.Medium, Color.FromArgb(0, 0, 128));
            range1.SetOutlineBorder(BorderType.LeftBorder, CellBorderType.Medium, Color.FromArgb(0, 0, 128));
            range1.SetOutlineBorder(BorderType.RightBorder, CellBorderType.Medium, Color.FromArgb(0, 0, 128));

            // Input some data with some formattings into
            // A few cells in the range.
            range1[0, 0].PutValue("Test");
            range1[0, 4].PutValue("123");

            // Create another range of cells.
            Range range2 = worksheet.Cells.CreateRange("B3", "F3");

            // Name the range.
            range2.Name = "testrange";

            // Copy the first range into second range.
            range2.Copy(range1);

            // Save the excel file.
            workbook.Save(outputDir + "outputCopyNamedRanges.xlsx");

            Console.WriteLine("CopyNamedRanges executed successfully.");
        }
    }
}

```
