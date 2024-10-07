---
title: Add Link to URL in Excel
linktitle: Add Link to URL in Excel
second_title: Aspose.Cells .NET Excel Processing API
description: 
type: docs
weight: 12
url: /net/excel-working-with-hyperlinks/add-link-to-url/
---

## Complete Source Code
```csharp
using System;
using System.IO;

using Aspose.Cells;

namespace Aspose.Cells.Examples.CSharp.Data
{
    public class AddingLinkToURL
    {
        //Output directory
        static string outputDir = "Your Document Directory"();

        public static void Run()
        {
            // Instantiating a Workbook object
            Workbook workbook = new Workbook();

            // Obtaining the reference of the first worksheet
            Worksheet worksheet = workbook.Worksheets[0];

            // Adding a hyperlink to a URL at "B4" cell
            worksheet.Hyperlinks.Add("B4", 1, 1, "https://www.aspose.com");
            worksheet.Hyperlinks[0].TextToDisplay = "Aspose - File Format APIs";

            // Saving the Excel file
            workbook.Save(outputDir + "outputAddingLinkToURL.xlsx");

            Console.WriteLine("AddingLinkToURL executed successfully.");
        }
    }
}

```
