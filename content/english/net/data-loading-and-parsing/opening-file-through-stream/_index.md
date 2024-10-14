---
title: Opening File through Stream
linktitle: Opening File through Stream
second_title: Aspose.Cells .NET Excel Processing API
description: 
type: docs
weight: 13
url: /net/data-loading-and-parsing/opening-file-through-stream/
---

## Complete Source Code
```csharp
using System.IO;

using Aspose.Cells;
using System;

namespace Aspose.Cells.Examples.CSharp.Files.Handling
{
    public class OpeningFilesThroughStream
    {
        public static void Run()
        {
            // ExStart:1
            // The path to the documents directory.
            string dataDir = "Your Document Directory";
            // Opening through Stream
            // Create a Stream object
            FileStream fstream = new FileStream(dataDir + "Book2.xls", FileMode.Open);

            // Creating a Workbook object, open the file from a Stream object
            // That contains the content of file and it should support seeking
            Workbook workbook2 = new Workbook(fstream);
            Console.WriteLine("Workbook opened using stream successfully!");
            fstream.Close();
            // ExEnd:1
            }
          }
      }    

```
