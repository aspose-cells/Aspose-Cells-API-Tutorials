---
title: Add Custom Labels with Smart Markers in Aspose.Cells
linktitle: Add Custom Labels with Smart Markers in Aspose.Cells
second_title: Aspose.Cells .NET Excel Processing API
description: 
type: docs
weight: 10
url: /net/smart-markers-dynamic-data/add-custom-labels-smart-markers/
---

## Complete Source Code
```csharp
using System.IO;

using Aspose.Cells;
using System.Data;
using System;

namespace Aspose.Cells.Examples.CSharp.SmartMarkers

{
    public class AddCustomLabels
    {
        public static void Run()
        {
            // ExStart:1
            // The path to the documents directory.
            string dataDir = "Your Document Directory";
            // Instantiate the workbook from a template file that contains Smart Markers
            Workbook workbook = new Workbook(dataDir + "Book1.xlsx");
            Workbook designer = new Workbook(dataDir + "SmartMarker_Designer.xlsx");

            // Export data from the first worksheet to fill a data table
            DataTable dt = workbook.Worksheets[0].Cells.ExportDataTable(0, 0, 11, 5, true);

            // Set the table name
            dt.TableName = "Report";

            // Instantiate a new WorkbookDesigner
            WorkbookDesigner d = new WorkbookDesigner();

            // Specify the workbook to the designer book
            d.Workbook = designer;

            // Set the data source
            d.SetDataSource(dt);

            // Process the smart markers
            d.Process();

            // Save the Excel file
            designer.Save(dataDir + "output.xlsx", SaveFormat.Xlsx);
            // ExEnd:1

            Console.WriteLine("AddCustomLabels executed successfully.");
        }
    }
}

```
