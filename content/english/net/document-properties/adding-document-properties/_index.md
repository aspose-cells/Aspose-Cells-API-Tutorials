---
title: Adding Document Properties in .NET
linktitle: Adding Document Properties in .NET
second_title: Aspose.Cells .NET Excel Processing API
description: 
type: docs
weight: 12
url: /net/document-properties/adding-document-properties/
---

## Complete Source Code
```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;

namespace Aspose.Cells.Examples.CSharp.Files.Utility
{
    class AddingDocumentProperties
    {
        public static void Run()
        {
            // ExStart:1
            // The path to the documents directory.
            string dataDir = "Your Document Directory";

            // Instantiate a Workbook object
            // Open an Excel file
            Workbook workbook = new Workbook(dataDir + "sample-document-properties.xlsx");

            // Retrieve a list of all custom document properties of the Excel file
            Aspose.Cells.Properties.CustomDocumentPropertyCollection customProperties = workbook.Worksheets.CustomDocumentProperties;

            // Adding a custom document property to the Excel file
            Aspose.Cells.Properties.DocumentProperty publisher = customProperties.Add("Publisher", "Aspose");

            // Saving resultant spreadsheet
            workbook.Save(dataDir + "out_sample-document-properties.xlsx");
            // ExEnd:1

        }
    }
}

```
