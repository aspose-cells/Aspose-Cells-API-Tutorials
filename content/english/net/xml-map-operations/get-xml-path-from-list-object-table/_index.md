---
title: Get XML Path from List Object Table using Aspose.Cells
linktitle: Get XML Path from List Object Table using Aspose.Cells
second_title: Aspose.Cells .NET Excel Processing API
description: 
type: docs
weight: 11
url: /net/xml-map-operations/get-xml-path-from-list-object-table/
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
    class GetXMLPathFromListObjectTable
    {
        public static void Main()
        {
            //Source directory
            string sourceDir = "Your Document Directory";

            // Load XLSX file containing data from XML file
            Workbook workbook = new Workbook(sourceDir + "XML Data.xlsx");

            // Access the first worksheet
            Worksheet ws = workbook.Worksheets[0];

            // Access ListObject from the first sheet
            Aspose.Cells.Tables.ListObject listObject = ws.ListObjects[0];


            // Get the url of the list object's xml map data binding
            string url = listObject.XmlMap.DataBinding.Url;

            // Display XML file name
            Console.WriteLine(url);

            Console.WriteLine("GetXMLPathFromListObjectTable executed successfully.\r\n");
        }
    }
}

```
