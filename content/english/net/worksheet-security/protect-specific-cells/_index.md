---
title: Protect Specific Cells in Worksheet using Aspose.Cells
linktitle: Protect Specific Cells in Worksheet using Aspose.Cells
second_title: Aspose.Cells .NET Excel Processing API
description: 
type: docs
weight: 14
url: /net/worksheet-security/protect-specific-cells/
---

## Complete Source Code
```csharp
using System.IO;

using Aspose.Cells;

namespace Aspose.Cells.Examples.CSharp.Worksheets.Security
{
    public class ProtectingSpecificCellsinaWorksheet
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

            // Create a new workbook.
            Workbook wb = new Workbook();

            // Create a worksheet object and obtain the first sheet.
            Worksheet sheet = wb.Worksheets[0];

            // Define the style object.
            Style style;

            // Define the styleflag object
            StyleFlag styleflag;

            // Loop through all the columns in the worksheet and unlock them.
            for (int i = 0; i <= 255; i++)
            {

                style = sheet.Cells.Columns[(byte)i].Style;
                style.IsLocked = false;
                styleflag = new StyleFlag();
                styleflag.Locked = true;
                sheet.Cells.Columns[(byte)i].ApplyStyle(style, styleflag);

            }

            // Lock the three cells...i.e. A1, B1, C1.
            style = sheet.Cells["A1"].GetStyle();
            style.IsLocked = true;
            sheet.Cells["A1"].SetStyle(style);
            style = sheet.Cells["B1"].GetStyle();
            style.IsLocked = true;
            sheet.Cells["B1"].SetStyle(style);
            style = sheet.Cells["C1"].GetStyle();
            style.IsLocked = true;
            sheet.Cells["C1"].SetStyle(style);

            // Finally, Protect the sheet now.
            sheet.Protect(ProtectionType.All);

            // Save the excel file.
            wb.Save(dataDir + "output.out.xls", SaveFormat.Excel97To2003);
            // ExEnd:1

        }
    }
}

```
