---
title: Detect Link Types
linktitle: Detect Link Types
second_title: Aspose.Cells for .NET API Reference
description: 
type: docs
weight: 80
url: /net/excel-workbook/detect-link-types/
---
### Sample source code for Detect Link Types using Aspose.Cells for .NET 
```csharp
            //source directory
            string SourceDir = RunExamples.Get_SourceDirectory();
            Workbook workbook = new Workbook(SourceDir + "LinkTypes.xlsx");
            // Get the first (default) worksheet
            Worksheet worksheet = workbook.Worksheets[0];
            // Create a range A2:B3
            Range range = worksheet.Cells.CreateRange("A1", "A7");
            // Get Hyperlinks in range
            Hyperlink[] hyperlinks = range.Hyperlinks;
            foreach (Hyperlink link in hyperlinks)
            {
                Console.WriteLine(link.TextToDisplay + ": " + link.LinkType);
            }
            Console.WriteLine("DetectLinkTypes executed successfully.");
```