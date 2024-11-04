---
title: Regex Replace in Workbook using Aspose.Cells
linktitle: Regex Replace in Workbook using Aspose.Cells
second_title: Aspose.Cells .NET Excel Processing API
description: 
type: docs
weight: 25
url: /net/workbook-operations/regex-replace/
---

## Complete Source Code
```csharp
using System;

namespace Aspose.Cells.Examples.CSharp._Workbook
{
    public class RegexReplace
    {
        public static void Run()
        {
            // ExStart:1
            //Source directory
            string sourceDir = "Your Document Directory";

            //Output directory
            string outputDir = "Your Document Directory";

            Workbook workbook = new Workbook(sourceDir + "SampleRegexReplace.xlsx");

            ReplaceOptions replace = new ReplaceOptions();
            replace.CaseSensitive = false;
            replace.MatchEntireCellContents = false;
            // Set to true to indicate that the searched key is regex
            replace.RegexKey = true;

            workbook.Replace("\\bKIM\\b", "^^^TIM^^^", replace);
            workbook.Save(outputDir + "RegexReplace_out.xlsx");
            // ExEnd:1

            Console.WriteLine("RegexReplace executed successfully.");
        }
    }
}

```
