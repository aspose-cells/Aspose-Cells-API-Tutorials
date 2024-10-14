---
title: Add a Label to Worksheet in Excel
linktitle: Add a Label to Worksheet in Excel
second_title: Aspose.Cells .NET Excel Processing API
description: 
type: docs
weight: 13
url: /net/excel-shapes-controls/add-label-to-worksheet-excel/
---

## Complete Source Code
```csharp
using System.IO;

using Aspose.Cells;
using Aspose.Cells.Drawing;
using System.Drawing;

namespace Aspose.Cells.Examples.CSharp.DrawingObjects.Controls
{
    public class AddingLabelControl
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

            // Create a new Workbook.
            Workbook workbook = new Workbook();

            // Get the first worksheet in the workbook.
            Worksheet sheet = workbook.Worksheets[0];

            // Add a new label to the worksheet.
            Aspose.Cells.Drawing.Label label = sheet.Shapes.AddLabel(2, 0, 2, 0, 60, 120);

            // Set the caption of the label.
            label.Text = "This is a Label";

            // Set the Placement Type, the way the
            // Label is attached to the cells.
            label.Placement = PlacementType.FreeFloating;

            // Saves the file.
            workbook.Save(dataDir + "book1.out.xls");
            // ExEnd:1

        }
    }
}

```
