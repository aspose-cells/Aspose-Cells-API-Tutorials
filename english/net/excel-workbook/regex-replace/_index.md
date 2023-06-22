---
title: Regex Replace
linktitle: Regex Replace
second_title: Aspose.Cells for .NET API Reference
description: 
type: docs
weight: 140
url: /net/excel-workbook/regex-replace/
---
### Sample source code for Regex Replace using Aspose.Cells for .NET 
```csharp
            //Source directory
            string sourceDir = RunExamples.Get_SourceDirectory();
            //Output directory
            string outputDir = RunExamples.Get_OutputDirectory();
            Workbook workbook = new Workbook(sourceDir + "SampleRegexReplace.xlsx");
            ReplaceOptions replace = new ReplaceOptions();
            replace.CaseSensitive = false;
            replace.MatchEntireCellContents = false;
            // Set to true to indicate that the searched key is regex
            replace.RegexKey = true;
            workbook.Replace("\\bKIM\\b", "^^^TIM^^^", replace);
            workbook.Save(outputDir + "RegexReplace_out.xlsx");
            Console.WriteLine("RegexReplace executed successfully.");
```