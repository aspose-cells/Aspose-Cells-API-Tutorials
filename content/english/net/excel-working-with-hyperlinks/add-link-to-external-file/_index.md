---
title: Add Link to External File in Excel
linktitle: Add Link to External File in Excel
second_title: Aspose.Cells .NET Excel Processing API
description: 
type: docs
weight: 10
url: /net/excel-working-with-hyperlinks/add-link-to-external-file/
---

## Complete Source Code
```csharp
using System;
using System.IO;

using Aspose.Cells;

namespace Aspose.Cells.Examples.CSharp.Data
{
    public class AddingLinkToExternalFile
    {
        //Output directory
        static string outputDir = "Your Document Directory"();

        public static void Run()
        {
            // Instantiating a Workbook object
            Workbook workbook = new Workbook();

            // Obtaining the reference of the newly added worksheet by passing its sheet index
            Worksheet worksheet = workbook.Worksheets[0];

            worksheet.Hyperlinks.Add("A5", 1, 1, outputDir + "SomeExcelFile.xlsx");
            worksheet.Hyperlinks[0].TextToDisplay = "Link To External File";

            // Saving the Excel file
            workbook.Save(outputDir + "outputAddingLinkToExternalFile.xlsx");

            workbook = new Workbook();
            workbook.Save(outputDir + "SomeExcelFile.xlsx");

            Console.WriteLine("AddingLinkToExternalFile executed successfully.");
        }
    }
}

```
