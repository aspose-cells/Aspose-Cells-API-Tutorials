---
title: Working with Excel Colors Programmatically
linktitle: Working with Excel Colors Programmatically
second_title: Aspose.Cells .NET Excel Processing API
description: 
type: docs
weight: 10
url: /net/excel-colors-and-background-settings/working-with-excel-colors/
---

## Complete Source Code
```csharp
using System.IO;

using Aspose.Cells;
using System.Drawing;

namespace Aspose.Cells.Examples.CSharp.Formatting
{
    public class ColorsAndBackground
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

            // Instantiating a Workbook object
            Workbook workbook = new Workbook();

            // Adding a new worksheet to the Workbook object
            int i = workbook.Worksheets.Add();

            // Obtaining the reference of the newly added worksheet by passing its sheet index
            Worksheet worksheet = workbook.Worksheets[i];

            // Define a Style and get the A1 cell style
            Style style = worksheet.Cells["A1"].GetStyle();

            // Setting the foreground color to yellow
            style.ForegroundColor = Color.Yellow;

            // Setting the background pattern to vertical stripe
            style.Pattern = BackgroundType.VerticalStripe;

            // Apply the style to A1 cell
            worksheet.Cells["A1"].SetStyle(style);

            // Get the A2 cell style
            style = worksheet.Cells["A2"].GetStyle();

            // Setting the foreground color to blue
            style.ForegroundColor = Color.Blue;

            // Setting the background color to yellow
            style.BackgroundColor = Color.Yellow;

            // Setting the background pattern to vertical stripe
            style.Pattern = BackgroundType.VerticalStripe;

            // Apply the style to A2 cell
            worksheet.Cells["A2"].SetStyle(style);

            // Saving the Excel file
            workbook.Save(dataDir + "book1.out.xls", SaveFormat.Excel97To2003);
            // ExEnd:1

        }
    }
}

```
