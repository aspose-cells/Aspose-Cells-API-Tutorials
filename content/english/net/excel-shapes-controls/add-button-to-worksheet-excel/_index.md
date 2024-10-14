---
title: Add a Button to Worksheet in Excel
linktitle: Add a Button to Worksheet in Excel
second_title: Aspose.Cells .NET Excel Processing API
description: 
type: docs
weight: 12
url: /net/excel-shapes-controls/add-button-to-worksheet-excel/
---

## Complete Source Code
```csharp
using System.IO;

using Aspose.Cells;
using Aspose.Cells.Drawing;
using System.Drawing;

namespace Aspose.Cells.Examples.CSharp.DrawingObjects.Controls
{
    public class AddingButtonControl
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

            // Add a new button to the worksheet.
            Aspose.Cells.Drawing.Button button = sheet.Shapes.AddButton(2, 0, 2, 0, 28, 80);

            // Set the caption of the button.
            button.Text = "Aspose";

            // Set the Placement Type, the way the
            // Button is attached to the cells.
            button.Placement = PlacementType.FreeFloating;

            // Set the font name.
            button.Font.Name = "Tahoma";

            // Set the caption string bold.
            button.Font.IsBold = true;

            // Set the color to blue.
            button.Font.Color = Color.Blue;

            // Set the hyperlink for the button.
            button.AddHyperlink("http:// Www.aspose.com/");

            // Saves the file.
            workbook.Save(dataDir + "book1.out.xls");
            // ExEnd:1

        }
    }
}

```
