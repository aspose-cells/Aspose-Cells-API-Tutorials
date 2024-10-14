---
title: Worksheet to Image Conversion in .NET
linktitle: Worksheet to Image Conversion in .NET
second_title: Aspose.Cells .NET Excel Processing API
description: 
type: docs
weight: 11
url: /net/image-and-chart-operations/worksheet-to-image-conversion/
---

## Complete Source Code
```csharp
using System.IO;
using System.Drawing;

using Aspose.Cells;
using Aspose.Cells.Rendering;

namespace Aspose.Cells.Examples.CSharp.Files.Utility
{
    public class WorksheetToImage
    {
        public static void Run()
        {
            // ExStart:1
            // The path to the documents directory.
            string dataDir = "Your Document Directory";

            // Open a template Excel file.
            Workbook book = new Workbook(dataDir + "MyTestBook1.xls");
            // Get the first worksheet.
            Worksheet sheet = book.Worksheets[0];

            // Define ImageOrPrintOptions
            ImageOrPrintOptions imgOptions = new ImageOrPrintOptions();
            // Specify the image format
            imgOptions.ImageType = Drawing.ImageType.Jpeg;
            // Only one page for the whole sheet would be rendered
            imgOptions.OnePagePerSheet = true;

            // Render the sheet with respect to specified image/print options
            SheetRender sr = new SheetRender(sheet, imgOptions);
            // Render the image for the sheet
            Bitmap bitmap = sr.ToImage(0);

            // Save the image file specifying its image format.
            bitmap.Save(dataDir + "SheetImage.out.jpg");

            // Display result, so that user knows the processing has finished.
            System.Console.WriteLine("Conversion to Image(s) completed.");
            // ExEnd:1
        }
    }
}

```
