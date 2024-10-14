---
title: Configuring Link to Content Document Property in .NET
linktitle: Configuring Link to Content Document Property in .NET
second_title: Aspose.Cells .NET Excel Processing API
description: 
type: docs
weight: 10
url: /net/link-and-configuration-operations/configuring-link-to-content-document-property/
---

## Complete Source Code
```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;

namespace Aspose.Cells.Examples.CSharp.Files.Utility
{
    class ConfigureLinktoContentDocumentProperty
    {
        public static void Run()
        {
            // ExStart:1
            // The path to the documents directory.
            string dataDir = "Your Document Directory";

            // Instantiate an object of Workbook
            // Open an Excel file
            Workbook workbook = new Workbook(dataDir + "sample-document-properties.xlsx");

            // Retrieve a list of all custom document properties of the Excel file
            Aspose.Cells.Properties.CustomDocumentPropertyCollection customProperties = workbook.Worksheets.CustomDocumentProperties;

            // Add link to content.
            customProperties.AddLinkToContent("Owner", "MyRange");

            // Accessing the custom document property by using the property name
            Aspose.Cells.Properties.DocumentProperty customProperty1 = customProperties["Owner"];

            // Check whether the property is lined to content
            bool islinkedtocontent = customProperty1.IsLinkedToContent;

            // Get the source for the property
            string source = customProperty1.Source;

            // Save the file
            workbook.Save(dataDir + "out_sample-document-properties.xlsx");
            // ExEnd:1

        }
    }
}

```
