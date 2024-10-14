---
title: Setting Image Preferences for HTML in .NET
linktitle: Setting Image Preferences for HTML in .NET
second_title: Aspose.Cells .NET Excel Processing API
description: 
type: docs
weight: 11
url: /net/worksheet-operations/setting-image-preferences-for-html/
---

## Complete Source Code
```csharp
using System.IO;

using Aspose.Cells;

namespace Aspose.Cells.Examples.CSharp.Files.Utility
{
    public class SettingImagePrefrencesforHTML
    {
        public static void Run()
        {
            // ExStart:1
            // The path to the documents directory.
            string dataDir = "Your Document Directory";
            // Specify the file path
            string filePath = dataDir + "Book1.xlsx";

            // Load a spreadsheet to be converted
            Workbook book = new Workbook(filePath);

            // Create an instance of HtmlSaveOptions
            HtmlSaveOptions saveOptions = new HtmlSaveOptions(SaveFormat.Html);

            // Set the ImageFormat to PNG
            saveOptions.ImageOptions.ImageType = Drawing.ImageType.Png;

            // Set SmoothingMode to AntiAlias
            saveOptions.ImageOptions.SmoothingMode = System.Drawing.Drawing2D.SmoothingMode.AntiAlias;

            // Set TextRenderingHint to AntiAlias
            saveOptions.ImageOptions.TextRenderingHint = System.Drawing.Text.TextRenderingHint.AntiAlias;

            // Save spreadsheet to HTML while passing object of HtmlSaveOptions
            book.Save( dataDir + "output.html", saveOptions);

            // ExEnd:1
        }
    }
}

```
