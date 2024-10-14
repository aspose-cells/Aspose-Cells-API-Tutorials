---
title: Manipulate TextBox Controls in Excel
linktitle: Manipulate TextBox Controls in Excel
second_title: Aspose.Cells .NET Excel Processing API
description: 
type: docs
weight: 15
url: /net/excel-shapes-controls/manipulate-textbox-controls-excel/
---

## Complete Source Code
```csharp
using System.IO;

using Aspose.Cells;

namespace Aspose.Cells.Examples.CSharp.DrawingObjects.Controls
{
    public class ManipulatingTextBoxControls
    {
        public static void Run()
        {
            // ExStart:1
            // The path to the documents directory.
            string dataDir = "Your Document Directory";

            // Instantiate a new Workbook.
            // Open the existing excel file.
            Workbook workbook = new Workbook(dataDir + "book1.xls");

            // Get the first worksheet in the book.
            Worksheet worksheet = workbook.Worksheets[0];

            // Get the first textbox object.
            Aspose.Cells.Drawing.TextBox textbox0 = worksheet.TextBoxes[0];

            // Obtain the text in the first textbox.
            string text0 = textbox0.Text;

            // Get the second textbox object.
            Aspose.Cells.Drawing.TextBox textbox1 = worksheet.TextBoxes[1];

            // Obtain the text in the second textbox.
            string text1 = textbox1.Text;

            // Change the text of the second textbox.
            textbox1.Text = "This is an alternative text";

            // Save the excel file.
            workbook.Save(dataDir + "output.out.xls");
            // ExEnd:1

        }
    }
}

```
