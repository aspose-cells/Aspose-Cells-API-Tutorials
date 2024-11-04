---
title: Display or Hide Row and Column Headers in Worksheet
linktitle: Display or Hide Row and Column Headers in Worksheet
second_title: Aspose.Cells .NET Excel Processing API
description: 
type: docs
weight: 12
url: /net/worksheet-display/display-hide-row-column-headers/
---

## Complete Source Code
```csharp
using System.IO;

using Aspose.Cells;

namespace Aspose.Cells.Examples.CSharp.Worksheets.Display
{
    public class DisplayHideRowColumnHeaders
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

            // Accessing the first worksheet in the Excel file
            Worksheet worksheet = workbook.Worksheets[0];

            // Hiding the headers of rows and columns
            worksheet.IsRowColumnHeadersVisible = false;

            // Saving the modified Excel file
            workbook.Save(dataDir + "output.xls");

            // Closing the file stream to free all resources
            fstream.Close(); 
            // ExEnd:1
        }
    }
}

```
