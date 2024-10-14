---
title: Opening CSV Files
linktitle: Opening CSV Files
second_title: Aspose.Cells .NET Excel Processing API
description: 
type: docs
weight: 10
url: /net/csv-file-handling/csv-file-opening-csv-files/
---

## Complete Source Code
```csharp
using System.IO;

using Aspose.Cells;
using System;

namespace Aspose.Cells.Examples.CSharp.Files.Handling
{
    public class OpeningCSVFiles
    {
        public static void Run()
        {
            // ExStart:1
            // The path to the documents directory.
            string dataDir = "Your Document Directory";

            // Instantiate LoadOptions specified by the LoadFormat.
            LoadOptions loadOptions4 = new LoadOptions(LoadFormat.Csv);

            // Create a Workbook object and opening the file from its path
            Workbook wbCSV = new Workbook(dataDir + "Book_CSV.csv", loadOptions4);
            Console.WriteLine("CSV file opened successfully!");
            // ExEnd:1
            }
          }
        }
            

```
