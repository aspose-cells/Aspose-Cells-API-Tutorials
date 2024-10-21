---
title: Utilizing Theme Colors in Excel Programmatically
linktitle: Utilizing Theme Colors in Excel Programmatically
second_title: Aspose.Cells .NET Excel Processing API
description: 
type: docs
weight: 12
url: /net/excel-themes-and-formatting/utilizing-theme-colors/
---

## Complete Source Code
```csharp
using System.IO;

using Aspose.Cells;

namespace Aspose.Cells.Examples.CSharp.Formatting.Excel2007Themes
{
    public class UtilizeThemeColors
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

            // Instantiate a Workbook.
            Workbook workbook = new Workbook();
            
            // Get cells collection in the first (default) worksheet.
            Cells cells = workbook.Worksheets[0].Cells;
           
            // Get the D3 cell.
            Aspose.Cells.Cell c = cells["D3"];

            // Get the style of the cell.
            Style s = c.GetStyle();
            
            // Set foreground color for the cell from the default theme Accent2 color.
            s.ForegroundThemeColor = new ThemeColor(ThemeColorType.Accent2, 0.5);
           
            // Set the pattern type.
            s.Pattern = BackgroundType.Solid;
            
            // Get the font for the style.
            Aspose.Cells.Font f = s.Font;
            
            // Set the theme color.
            f.ThemeColor = new ThemeColor(ThemeColorType.Accent4, 0.1);

            // Apply style.
            c.SetStyle(s);

            // Put a value.
            c.PutValue("Testing1");

            // Save the excel file.
            workbook.Save(dataDir + "output.out.xlsx");
            // ExEnd:1

        }
    }
}

```
