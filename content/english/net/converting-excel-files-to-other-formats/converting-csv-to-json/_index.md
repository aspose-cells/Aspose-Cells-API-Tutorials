---
title: Converting CSV to JSON Programmatically in .NET
linktitle: Converting CSV to JSON Programmatically in .NET
second_title: Aspose.Cells .NET Excel Processing API
description: 
type: docs
weight: 10
url: /net/converting-excel-files-to-other-formats/converting-csv-to-json/
---

## Complete Source Code
```csharp
using Aspose.Cells.Utility;
using System;
using System.IO;

namespace Aspose.Cells.Examples.CSharp.LoadingSavingConvertingAndManaging
{
    public class ConvertCsvToJson
    {
        public static void Run()
        {
            // ExStart:1
            //Source directory
            string sourceDir = RunExamples.Get_SourceDirectory();

            LoadOptions loadOptions = new LoadOptions(LoadFormat.Csv);
            // Load csv file
            Workbook workbook = new Workbook(sourceDir + "SampleCsv.csv", loadOptions);
            Cell lastCell = workbook.Worksheets[0].Cells.LastCell;

            // Set ExportRangeToJsonOptions
            ExportRangeToJsonOptions options = new ExportRangeToJsonOptions();
            Range range = workbook.Worksheets[0].Cells.CreateRange(0, 0, lastCell.Row + 1, lastCell.Column + 1);
            string data = JsonUtility.ExportRangeToJson(range, options);

            // Print JSON
            Console.WriteLine(data);
            // ExEnd:1

            Console.WriteLine("ConvertCsvToJson executed successfully.");
        }
    }
}

```
