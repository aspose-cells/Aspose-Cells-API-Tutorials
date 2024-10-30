---
title: Use HTML Property in Smart Markers Aspose.Cells .NET
linktitle: Use HTML Property in Smart Markers Aspose.Cells .NET
second_title: Aspose.Cells .NET Excel Processing API
description: 
type: docs
weight: 21
url: /net/smart-markers-dynamic-data/html-property-smart-markers/
---

## Complete Source Code
```csharp
using System.IO;

using Aspose.Cells;
using System;

namespace Aspose.Cells.Examples.CSharp.SmartMarkers
{
    public class UsingHTMLProperty
    {
        public static void Run()
        {
            // ExStart:1
            // The path to the documents directory.
            string dataDir = "Your Document Directory";
            Workbook workbook = new Workbook();
            WorkbookDesigner designer = new WorkbookDesigner();
            designer.Workbook = workbook;
            workbook.Worksheets[0].Cells["A1"].PutValue("&=$VariableArray(HTML)");
            designer.SetDataSource("VariableArray", new String[] { "Hello <b>World</b>", "Arabic", "Hindi", "Urdu", "French" });
            designer.Process();
            workbook.Save(dataDir + "output.xls");

            // ExEnd:1
        }
    }
}
```
