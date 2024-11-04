---
title: Implement Page Orientation in Worksheet
linktitle: Implement Page Orientation in Worksheet
second_title: Aspose.Cells .NET Excel Processing API
description: 
type: docs
weight: 18
url: /net/worksheet-page-setup-features/implement-page-orientation/
---

## Complete Source Code
```csharp
using System.IO;
using Aspose.Cells;
using System;

namespace Aspose.Cells.Examples.CSharp.Worksheets.PageSetupFeatures
{
    public class PageOrientation
    {
        public static void Run()
        {
            // ExStart:1
            // The path to the documents directory.
            string dataDir = "Your Document Directory";

            // Instantiating a Workbook object
            Workbook workbook = new Workbook();

            // Accessing the first worksheet in the Excel file
            Worksheet worksheet = workbook.Worksheets[0];

            // Setting the orientation to Portrait
            worksheet.PageSetup.Orientation = PageOrientationType.Portrait;

            // Save the Workbook.
            workbook.Save(dataDir + "PageOrientation_out.xls");
            // ExEnd:1
        }
    }
}

```
