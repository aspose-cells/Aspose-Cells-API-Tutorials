---
title: Converting JSON to CSV Programmatically in .NET
linktitle: Converting JSON to CSV Programmatically in .NET
second_title: Aspose.Cells .NET Excel Processing API
description: 
type: docs
weight: 15
url: /net/converting-excel-files-to-other-formats/converting-json-to-csv/
---

## Complete Source Code
```csharp
using Aspose.Cells.Utility;
using System;
using System.IO;

namespace Aspose.Cells.Examples.CSharp.LoadingSavingConvertingAndManaging
{
    public class ConvertJsonToCsv
    {
        public static void Run()
        {
            // ExStart:1
            //Source directory
            string sourceDir = "Your Document Directory";

            //Output directory
            string outputDir = "Your Document Directory";

            // Read JSON file
            string str = File.ReadAllText(sourceDir + "SampleJson.json");

            // Create empty workbook
            Workbook workbook = new Workbook();

            // Get Cells
            Cells cells = workbook.Worksheets[0].Cells;

            // Set JsonLayoutOptions
            JsonLayoutOptions importOptions = new JsonLayoutOptions();
            importOptions.ConvertNumericOrDate = true;
            importOptions.ArrayAsTable = true;
            importOptions.IgnoreArrayTitle = true;
            importOptions.IgnoreObjectTitle = true;
            JsonUtility.ImportData(str, cells, 0, 0, importOptions);

            // Save Workbook
            workbook.Save(outputDir + @"SampleJson_out.csv");
            // ExEnd:1

            Console.WriteLine("ConvertJsonToCsv executed successfully.");
        }
    }
}

```
