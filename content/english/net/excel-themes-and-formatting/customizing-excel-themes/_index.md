---
title: Customizing Excel Themes Programmatically
linktitle: Customizing Excel Themes Programmatically
second_title: Aspose.Cells .NET Excel Processing API
description: 
type: docs
weight: 10
url: /net/excel-themes-and-formatting/customizing-excel-themes/
---

## Complete Source Code
```csharp
using System.IO;

using Aspose.Cells;
using System.Drawing;

namespace Aspose.Cells.Examples.CSharp.Formatting.Excel2007Themes
{
    public class CustomizeThemes
    {
        public static void Run()
        {
            // ExStart:1
            // The path to the documents directory.
            string dataDir = "Your Document Directory";
            
            // Define Color array (of 12 colors) for Theme.
            Color[] carr = new Color[12];
            carr[0] = Color.AntiqueWhite; // Background1
            carr[1] = Color.Brown; // Text1
            carr[2] = Color.AliceBlue; // Background2
            carr[3] = Color.Yellow; // Text2
            carr[4] = Color.YellowGreen; // Accent1
            carr[5] = Color.Red; // Accent2
            carr[6] = Color.Pink; // Accent3
            carr[7] = Color.Purple; // Accent4
            carr[8] = Color.PaleGreen; // Accent5
            carr[9] = Color.Orange; // Accent6
            carr[10] = Color.Green; // Hyperlink
            carr[11] = Color.Gray; // Followed Hyperlink

            // Instantiate a Workbook.
            // Open the template file.
            Workbook workbook = new Workbook(dataDir + "book1.xlsx");

            // Set the custom theme with specified colors.
            workbook.CustomTheme("CustomeTheme1", carr);
            
            // Save as the excel file.
            workbook.Save(dataDir + "output.out.xlsx");
            // ExEnd:1

            
        }
    }
}

```
