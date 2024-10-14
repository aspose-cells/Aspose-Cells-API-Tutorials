---
title: Saving Text File with Custom Separator
linktitle: Saving Text File with Custom Separator
second_title: Aspose.Cells .NET Excel Processing API
description: 
type: docs
weight: 13
url: /net/file-handling/file-saving-text-file-with-custom-separator/
---

## Complete Source Code
```csharp
using System.IO;

using Aspose.Cells;
using System;

namespace Aspose.Cells.Examples.CSharp.Files.Handling
{
    public class SavingTextFilewithCustomSeparator
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

            // Specify the separator
            options.Separator = Convert.ToChar(";");

            // Save the file with the options
            wb.Save(dataDir + "output.csv", options);
              
            // ExEnd:1


        }
    }
}
```
