---
title: Opening File with Data Only
linktitle: Opening File with Data Only
second_title: Aspose.Cells .NET Excel Processing API
description: 
type: docs
weight: 11
url: /net/data-loading-and-parsing/opening-file-with-data-only/
---

## Complete Source Code
```csharp
using System.IO;

using Aspose.Cells;
using System;

namespace Aspose.Cells.Examples.CSharp.Files.Handling
{
    public class OpeningFilewithDataOnly
    {
        public static void Run()
        {
            // ExStart:1
            // The path to the documents directory.
            string dataDir = "Your Document Directory";
            // Load only specific sheets with data and formulas
            // Other objects, items etc. would be discarded

            // Instantiate LoadOptions specified by the LoadFormat
            LoadOptions loadOptions = new LoadOptions(LoadFormat.Xlsx);

            // Set LoadFilter property to load only data & cell formatting
            loadOptions.LoadFilter = new LoadFilter(LoadDataFilterOptions.CellData);
            

            // Create a Workbook object and opening the file from its path
            Workbook book = new Workbook(dataDir + "Book1.xlsx", loadOptions);
            Console.WriteLine("File data imported successfully!");
            // ExEnd:1
            
        }
    }
}

```
