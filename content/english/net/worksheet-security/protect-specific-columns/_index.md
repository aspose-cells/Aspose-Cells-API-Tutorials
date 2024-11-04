---
title: Protect Specific Columns in Worksheet using Aspose.Cells
linktitle: Protect Specific Columns in Worksheet using Aspose.Cells
second_title: Aspose.Cells .NET Excel Processing API
description: 
type: docs
weight: 15
url: /net/worksheet-security/protect-specific-columns/
---

## Complete Source Code
```csharp
using System.IO;

using Aspose.Cells;

namespace Aspose.Cells.Examples.CSharp.Worksheets.Security
{
    public class ProtectingSpecificColumnInWorksheet
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

            // Define the styleflag object.
            StyleFlag flag;

            // Loop through all the columns in the worksheet and unlock them.
            for (int i = 0; i <= 255; i++)
            {
                style = sheet.Cells.Columns[(byte)i].Style;
                style.IsLocked = false;
                flag = new StyleFlag();
                flag.Locked = true;
                sheet.Cells.Columns[(byte)i].ApplyStyle(style, flag);

            }

            // Get the first column style.
            style = sheet.Cells.Columns[0].Style;

            // Lock it.
            style.IsLocked = true;

            // Instantiate the flag.
            flag = new StyleFlag();

            // Set the lock setting.
            flag.Locked = true;

            // Apply the style to the first column.
            sheet.Cells.Columns[0].ApplyStyle(style, flag);

            // Protect the sheet.
            sheet.Protect(ProtectionType.All);

            // Save the excel file.
            wb.Save(dataDir + "output.out.xls", SaveFormat.Excel97To2003);
            // ExEnd:1

            
        }
    }
}

```
