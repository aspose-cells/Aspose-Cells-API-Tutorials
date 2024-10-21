---
title: Getting and Setting Theme Colors in Excel
linktitle: Getting and Setting Theme Colors in Excel
second_title: Aspose.Cells .NET Excel Processing API
description: 
type: docs
weight: 11
url: /net/excel-themes-and-formatting/getting-and-setting-theme-colors/
---

## Complete Source Code
```csharp
using System.IO;

using Aspose.Cells;
using System.Drawing;
using System;

namespace Aspose.Cells.Examples.CSharp.Formatting.Excel2007Themes
{
    public class GetSetThemeColors
    {
        public static void Run()
        {
            // ExStart:1
            // The path to the documents directory.
            string dataDir = RunExamples.GetDataDir(System.Reflection.MethodBase.GetCurrentMethod().DeclaringType);

            // Instantiate Workbook object.
            // Open an exiting excel file.
            Workbook workbook = new Workbook(dataDir + "book1.xlsx");

            // Get the Background1 theme color.
            Color c = workbook.GetThemeColor(ThemeColorType.Background1);

            // Print the color.
            Console.WriteLine("theme color Background1: " + c);

            // Get the Accent2 theme color.
            c = workbook.GetThemeColor(ThemeColorType.Accent2);

            // Print the color.
            Console.WriteLine("theme color Accent2: " + c);

            // Change the Background1 theme color.
            workbook.SetThemeColor(ThemeColorType.Background1, Color.Red);

            // Get the updated Background1 theme color.
            c = workbook.GetThemeColor(ThemeColorType.Background1);

            // Print the updated color for confirmation.
            Console.WriteLine("theme color Background1 changed to: " + c);

            // Change the Accent2 theme color.
            workbook.SetThemeColor(ThemeColorType.Accent2, Color.Blue);

            // Get the updated Accent2 theme color.
            c = workbook.GetThemeColor(ThemeColorType.Accent2);

            // Print the updated color for confirmation.
            Console.WriteLine("theme color Accent2 changed to: " + c);

            // Save the updated file.
            workbook.Save(dataDir + "output.out.xlsx");
            // ExEnd:1

        }
    }
}

```
