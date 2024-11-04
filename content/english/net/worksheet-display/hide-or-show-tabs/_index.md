---
title: Hide or Show Tabs in Worksheet using Aspose.Cells
linktitle: Hide or Show Tabs in Worksheet using Aspose.Cells
second_title: Aspose.Cells .NET Excel Processing API
description: 
type: docs
weight: 17
url: /net/worksheet-display/hide-or-show-tabs/
---

## Complete Source Code
```csharp
using System.IO;

using Aspose.Cells;

namespace Aspose.Cells.Examples.CSharp.Worksheets.Display
{
    public class HideTabs
    {
        public static void Run()
        {
            // ExStart:1
            // The path to the documents directory.
            string dataDir = "Your Document Directory";

            // Opening the Excel file
            Workbook workbook = new Workbook(dataDir + "book1.xls");

            // Hiding the tabs of the Excel file
            workbook.Settings.ShowTabs = false;

            // Shows the tabs of the Excel file
            //workbook.Settings.ShowTabs = true;

            // Saving the modified Excel file
            workbook.Save(dataDir + "output.xls");
            // ExEnd:1
        }
    }
}

```
