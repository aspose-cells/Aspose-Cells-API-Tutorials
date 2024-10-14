---
title: Saving File to Stream
linktitle: Saving File to Stream
second_title: Aspose.Cells .NET Excel Processing API
description: 
type: docs
weight: 12
url: /net/file-handling/file-saving-file-to-stream/
---

## Complete Source Code
```csharp
using System.IO;

using Aspose.Cells;
using System;

namespace Aspose.Cells.Examples.CSharp.Files.Handling
{
    public class SavingFiletoStream
    {
        public static void Run()
        {
            // ExStart:1
            // The path to the documents directory.
            string dataDir = "Your Document Directory";
            string filePath = dataDir + "Book1.xlsx";

            // Load your source workbook
            using (FileStream stream = new FileStream(dataDir + "output.xlsx", FileMode.CreateNew))
            {
                Workbook workbook = new Workbook(filePath);

                workbook.Save(stream, SaveFormat.Xlsx);
                stream.Close();


            }
            // ExEnd:1


        }
    }
}
```
