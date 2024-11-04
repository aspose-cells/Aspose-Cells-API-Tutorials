---
title: Query Cell Areas Mapped to Xml Map Path using Aspose.Cells
linktitle: Query Cell Areas Mapped to Xml Map Path using Aspose.Cells
second_title: Aspose.Cells .NET Excel Processing API
description: 
type: docs
weight: 12
url: /net/xml-map-operations/query-cell-areas-mapped-to-xml-map-path/
---

## Complete Source Code
```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;

using System.Diagnostics;
using System.Collections;

namespace Aspose.Cells.Examples.CSharp.XmlMaps
{
    class QueryCellAreasMappedToXmlMapPath 
    {
        public static void Run()
        {
            //Source directory
            string sourceDir = "Your Document Directory";

            //Output directory
            string outputDir = "Your Document Directory";

            //Load sample Excel file having Xml Map
            Workbook wb = new Workbook(sourceDir + "sampleXmlMapQuery.xlsx");

            //Access first XML Map
            XmlMap xmap = wb.Worksheets.XmlMaps[0];

            //Access first worksheet
            Worksheet ws = wb.Worksheets[0];

            //Query Xml Map from Path - /MiscData
            Console.WriteLine("Query Xml Map from Path - /MiscData");
            ArrayList ret = ws.XmlMapQuery("/MiscData", xmap);

            //Print returned ArrayList values
            for (int i = 0; i < ret.Count; i++)
            {
                Console.WriteLine(ret[i]);
            }

            Console.WriteLine("");

            //Query Xml Map from Path - /MiscData/row/Color
            Console.WriteLine("Query Xml Map from Path - /MiscData/row/Color");
            ret = ws.XmlMapQuery("/MiscData/row/Color", xmap);

            //Print returned ArrayList values
            for (int i = 0; i < ret.Count; i++)
            {
                Console.WriteLine(ret[i]);
            }

            Console.WriteLine("QueryCellAreasMappedToXmlMapPath executed successfully.\r\n");
        }
    }
}

```
