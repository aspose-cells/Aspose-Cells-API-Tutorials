---
title: Convert Smart Art to Group Shape in Excel
linktitle: Convert Smart Art to Group Shape in Excel
second_title: Aspose.Cells .NET Excel Processing API
description: 
type: docs
weight: 15
url: /net/excel-shape-text-modifications/convert-smart-art-group-shape-excel/
---

## Complete Source Code
```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;

using Aspose.Cells.Drawing;

namespace Aspose.Cells.Examples.CSharp.DrawingObjects
{
    class ConvertSmartArtToGroupShape 
    {
        public static void Run()
        {
            //Source directory
            string sourceDir = RunExamples.Get_SourceDirectory();

            //Load the sample smart art shape - Excel file
            Workbook wb = new Workbook(sourceDir + "sampleSmartArtShape_GetResultOfSmartArt.xlsx");

            //Access first worksheet
            Worksheet ws = wb.Worksheets[0];

            //Access first shape
            Shape sh = ws.Shapes[0];

            //Determine if shape is smart art
            Console.WriteLine("Is Smart Art Shape: " + sh.IsSmartArt);

            //Determine if shape is group shape
            Console.WriteLine("Is Group Shape: " + sh.IsGroup);

            //Convert smart art shape into group shape
            Console.WriteLine("Is Group Shape: " + sh.GetResultOfSmartArt().IsGroup);

            Console.WriteLine("ConvertSmartArtToGroupShape executed successfully.\r\n");
        }
    }
}

```
