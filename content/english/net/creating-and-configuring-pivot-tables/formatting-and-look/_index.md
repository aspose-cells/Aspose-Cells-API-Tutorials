---
title: Formatting and Look of Pivot Tables Programmatically in .NET
linktitle: Formatting and Look of Pivot Tables Programmatically in .NET
second_title: Aspose.Cells .NET Excel Processing API
description: 
type: docs
weight: 16
url: /net/creating-and-configuring-pivot-tables/formatting-and-look/
---

## Complete Source Code
```csharp
using System.IO;

using Aspose.Cells;
using System.Drawing;
using Aspose.Cells.Pivot;

namespace Aspose.Cells.Examples.CSharp.PivotTableExamples
{
    public class FormattingLook
    {
        public static void Run()
        {
            // ExStart:1
            // The path to the documents directory.
            string dataDir = "Your Document Directory";

            // Load a template file
            Workbook workbook = new Workbook(dataDir + "Book1.xls");

            // Get the first worksheet
            Worksheet worksheet = workbook.Worksheets[0];
            var pivot = workbook.Worksheets[0].PivotTables[0];

            pivot.PivotTableStyleType = PivotTableStyleType.PivotTableStyleDark1;

            Style style = workbook.CreateStyle();
            style.Font.Name = "Arial Black";
            style.ForegroundColor = Color.Yellow;
            style.Pattern = BackgroundType.Solid;

            pivot.FormatAll(style);

            // Saving the Excel file
            workbook.Save(dataDir + "output.xls");

            // ExEnd:1

        }
    }
}
```
