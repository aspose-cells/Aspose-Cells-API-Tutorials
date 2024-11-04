---
title: Control Tab Bar Width in Worksheet using Aspose.Cells
linktitle: Control Tab Bar Width in Worksheet using Aspose.Cells
second_title: Aspose.Cells .NET Excel Processing API
description: 
type: docs
weight: 10
url: /net/worksheet-display/control-tab-bar-width/
---

## Complete Source Code
```csharp
using System.IO;

using Aspose.Cells;

namespace Aspose.Cells.Examples.CSharp.Worksheets.Display
{
    public class ControlTabBarWidth
    {
        public static void Run()
        {
            // ExStart:1
            // The path to the documents directory.
            string dataDir = "Your Document Directory";

            // Instantiating a Workbook object
            // Opening the Excel file
            Workbook workbook = new Workbook(dataDir + "book1.xls");

            // Hiding the tabs of the Excel file
            workbook.Settings.ShowTabs = true;

            // Adjusting the sheet tab bar width
            workbook.Settings.SheetTabBarWidth = 800;

            // Saving the modified Excel file
            workbook.Save(dataDir + "output.xls");
            // ExEnd:1
        }
    }
}

```
