---
title: Use Dynamic Formulas in Smart Markers Aspose.Cells
linktitle: Use Dynamic Formulas in Smart Markers Aspose.Cells
second_title: Aspose.Cells .NET Excel Processing API
description: 
type: docs
weight: 13
url: /net/smart-markers-dynamic-data/dynamic-formulas-smart-markers/
---

## Complete Source Code
```csharp
using System.IO;

using Aspose.Cells;

namespace Aspose.Cells.Examples.CSharp.SmartMarkers
{
    public class DynamicFormulas
    {
        public static void Run()
        {
            // ExStart:1
            // The path to the documents directory.
            string dataDir = "Your Document Directory";

            // Create directory if it is not already present.
            bool IsExists = System.IO.Directory.Exists(dataDir);
            if (!IsExists)
                System.IO.Directory.CreateDirectory(dataDir);

            if (designerFile != null)
            {

                // Instantiating a WorkbookDesigner object
                WorkbookDesigner designer = new WorkbookDesigner();

                // Open a designer spreadsheet containing smart markers
                designer.Workbook = new Workbook(designerFile);

                // Set the data source for the designer spreadsheet
                designer.SetDataSource(dataset);

                // Process the smart markers
                designer.Process();               
            }
            // ExEnd:1
            
        }

        public static Stream designerFile { get; set; }

        public static System.Data.SqlClient.SqlConnection dataset { get; set; }
    }
}
```
