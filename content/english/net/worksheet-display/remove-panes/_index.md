---
title: Remove Panes from Worksheet using Aspose.Cells
linktitle: Remove Panes from Worksheet using Aspose.Cells
second_title: Aspose.Cells .NET Excel Processing API
description: 
type: docs
weight: 20
url: /net/worksheet-display/remove-panes/
---

## Complete Source Code
```csharp
using System.IO;

using Aspose.Cells;

namespace Aspose.Cells.Examples.CSharp.Worksheets.Display
{
    public class RemovePanes
    {
        public static void Run()
        {
            // ExStart:1
            // The path to the documents directory.
            string dataDir = "Your Document Directory";

            // Instantiate a new workbook and Open a template file
            Workbook book = new Workbook(dataDir + "Book1.xls");

            // Set the active cell
            book.Worksheets[0].ActiveCell = "A20";

            // Split the worksheet window
            book.Worksheets[0].RemoveSplit();

            // Save the excel file
            book.Save(dataDir + "output.xls");
            // ExEnd:1
        }
    }
}

```
