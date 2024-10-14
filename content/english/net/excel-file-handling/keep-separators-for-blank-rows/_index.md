---
title: Keep Separators for Blank Rows in Excel
linktitle: Keep Separators for Blank Rows in Excel
second_title: Aspose.Cells .NET Excel Processing API
description: 
type: docs
weight: 11
url: /net/excel-file-handling/keep-separators-for-blank-rows/
---

## Complete Source Code
```csharp
using System.IO;

using Aspose.Cells;
using System;

namespace Aspose.Cells.Examples.CSharp.Files.Handling
{
    public class KeepSeparatorsForBlankRow
    {
        public static void Run()
        {
            // ExStart:1
            // The path to the documents directory.
            string dataDir = "Your Document Directory";
            string filePath = dataDir + "Book1.xlsx";

            // Create a Workbook object and opening the file from its path
            Workbook wb = new Workbook(filePath);

            // Instantiate Text File's Save Options
            TxtSaveOptions options = new TxtSaveOptions();

            // Set KeepSeparatorsForBlankRow to true show separators in blank rows
            options.KeepSeparatorsForBlankRow = true;

            // Save the file with the options
            wb.Save(dataDir + "output.csv", options);
            // ExEnd:1

            Console.WriteLine("KeepSeparatorsForBlankRow executed successfully.\r\n");
        }
    }
}
```
