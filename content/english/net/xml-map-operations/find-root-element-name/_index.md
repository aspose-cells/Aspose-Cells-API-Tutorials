---
title: Find Root Element Name of Xml Map using Aspose.Cells
linktitle: Find Root Element Name of Xml Map using Aspose.Cells
second_title: Aspose.Cells .NET Excel Processing API
description: 
type: docs
weight: 10
url: /net/xml-map-operations/find-root-element-name/
---

## Complete Source Code
```csharp
using System;
using System.IO;

using Aspose.Cells;

namespace Aspose.Cells.Examples.CSharp.XmlMaps
{
    public class FindRootElementNameOfXmlMap 
    {
        public static void Run()
        {
            //Source directory
            string sourceDir = "Your Document Directory";

            //Load sample Excel file having Xml Map
            Workbook wb = new Workbook(sourceDir + "sampleRootElementNameOfXmlMap.xlsx");

            //Access first Xml Map inside the Workbook
            XmlMap xmap = wb.Worksheets.XmlMaps[0];

            //Print Root Element Name of Xml Map on Console
            Console.WriteLine("Root Element Name Of Xml Map: " + xmap.RootElementName);

            Console.WriteLine("FindRootElementNameOfXmlMap executed successfully.\r\n");
        }
    }
}

```
