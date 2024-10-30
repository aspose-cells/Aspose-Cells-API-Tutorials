---
title: Implement Variable Array with Smart Markers Aspose.Cells
linktitle: Implement Variable Array with Smart Markers Aspose.Cells
second_title: Aspose.Cells .NET Excel Processing API
description: 
type: docs
weight: 23
url: /net/smart-markers-dynamic-data/variable-array-smart-markers/
---

## Complete Source Code
```csharp
using System.IO;

using Aspose.Cells;
using System.Data;

namespace Aspose.Cells.Examples.CSharp.SmartMarkers
{
    public class UsingVariableArray
    {
        public static void Run()
        {
            // ExStart:1
            // The path to the documents directory.
            string dataDir = "Your Document Directory";

            // Instantiate a new Workbook designer.
            WorkbookDesigner report = new WorkbookDesigner();

            // Get the first worksheet of the workbook.
            Worksheet w = report.Workbook.Worksheets[0];

            // Set the Variable Array marker to a cell.
            // You may also place this Smart Marker into a template file manually in Ms Excel and then open this file via Workbook.
            w.Cells["A1"].PutValue("&=$VariableArray");

            // Set the DataSource for the marker(s).
            report.SetDataSource("VariableArray", new string[] { "English", "Arabic", "Hindi", "Urdu", "French" });

            // Process the markers.
            report.Process(false);

            // Save the Excel file.
            report.Workbook.Save(dataDir + "output.xlsx");
            // ExEnd:1

        }
    }
}
```
