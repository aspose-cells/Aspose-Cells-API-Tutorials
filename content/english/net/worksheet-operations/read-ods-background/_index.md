---
title: Read ODS Background Image
linktitle: Read ODS Background Image
second_title: Aspose.Cells .NET Excel Processing API
description: 
type: docs
weight: 20
url: /net/worksheet-operations/read-ods-background/
---

## Complete Source Code
```csharp
using Aspose.Cells.Ods;
using System;
using System.Drawing;
using System.IO;

namespace Aspose.Cells.Examples.CSharp.Worksheets
{
    class ReadODSBackground
    {
        public static void Run()
        {
            // ExStart:1
            //Source directory
            string sourceDir = "Your Document Directory";
            //Output directory
            string outputDir = "Your Document Directory";

            //Load source Excel file
            Workbook workbook = new Workbook(sourceDir + "GraphicBackground.ods");

            //Access first worksheet
            Worksheet worksheet = workbook.Worksheets[0];

            OdsPageBackground background = worksheet.PageSetup.ODSPageBackground;

            Console.WriteLine("Background Type: " + background.Type.ToString());
            Console.WriteLine("Backgorund Position: " + background.GraphicPositionType.ToString());

            //Save background image
            Bitmap image = new Bitmap(new MemoryStream(background.GraphicData));
            image.Save(outputDir + "background.jpg");
            // ExEnd:1

            Console.WriteLine("ReadODSBackground executed successfully.");
        }
    }
}

```
