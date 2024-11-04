---
title: Display or Hide Scroll Bars in Worksheet
linktitle: Display or Hide Scroll Bars in Worksheet
second_title: Aspose.Cells .NET Excel Processing API
description: 
type: docs
weight: 13
url: /net/worksheet-display/display-hide-scroll-bars/
---

## Complete Source Code
```csharp
using System.IO;

using Aspose.Cells;

namespace Aspose.Cells.Examples.CSharp.Worksheets.Display
{
    public class DisplayHideScrollBars
    {
        public static void Run()
        {
            // ExStart:1
            // The path to the documents directory.
            string dataDir = "Your Document Directory";

            // Creating a file stream containing the Excel file to be opened
            FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);

            // Instantiating a Workbook object
            // Opening the Excel file through the file stream
            Workbook workbook = new Workbook(fstream);

            // Hiding the vertical scroll bar of the Excel file
            workbook.Settings.IsVScrollBarVisible = false;

            // Hiding the horizontal scroll bar of the Excel file
            workbook.Settings.IsHScrollBarVisible = false;

            // Saving the modified Excel file
            workbook.Save(dataDir + "output.xls");

            // Closing the file stream to free all resources
            fstream.Close();
            // ExEnd:1
        }
    }
}

```
