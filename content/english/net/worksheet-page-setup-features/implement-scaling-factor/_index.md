---
title: Implement Scaling Factor in Worksheet
linktitle: Implement Scaling Factor in Worksheet
second_title: Aspose.Cells .NET Excel Processing API
description: 
type: docs
weight: 20
url: /net/worksheet-page-setup-features/implement-scaling-factor/
---

## Complete Source Code
```csharp
using System.IO;
using Aspose.Cells;
using System;

namespace Aspose.Cells.Examples.CSharp.Worksheets.PageSetupFeatures
{
    public class ScalingFactor
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

            // Setting the scaling factor to 100
            worksheet.PageSetup.Zoom = 100;

            // Save the workbook.
            workbook.Save(dataDir + "ScalingFactor_out.xls");
            // ExEnd:1
        }
    }
}

```
