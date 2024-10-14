---
title: Opening Files Through Path
linktitle: Opening Files Through Path
second_title: Aspose.Cells .NET Excel Processing API
description: 
type: docs
weight: 12
url: /net/data-loading-and-parsing/opening-files-through-path/
---

## Complete Source Code
```csharp
using System.IO;

using Aspose.Cells;
using System;

namespace Aspose.Cells.Examples.CSharp.Files.Handling
{
    public class OpeningFilesThroughPath
    {
        public static void Run()
        {
            // ExStart:1
            // The path to the documents directory.
            string dataDir = "Your Document Directory";
            
            // Opening through Path
            // Creating a Workbook object and opening an Excel file using its file path
            Workbook workbook1 = new Workbook(dataDir + "Book1.xlsx");
            Console.WriteLine("Workbook opened using path successfully!");
            // ExEnd:1
            
        }
    }
}
            

```
