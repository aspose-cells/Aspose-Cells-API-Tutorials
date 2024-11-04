---
title: Work with Content Type Properties of Workbook
linktitle: Work with Content Type Properties of Workbook
second_title: Aspose.Cells .NET Excel Processing API
description: 
type: docs
weight: 28
url: /net/workbook-operations/work-with-content-type-properties/
---

## Complete Source Code
```csharp
using Aspose.Cells.WebExtensions;
using System;

namespace Aspose.Cells.Examples.CSharp._Workbook
{
    public class WorkingWithContentTypeProperties
    {
        public static void Run()
        {
            // ExStart:1
            //source directory
            string outputDir = "Your Document Directory";

            Workbook workbook = new Workbook(FileFormatType.Xlsx);
            int index = workbook.ContentTypeProperties.Add("MK31", "Simple Data");
            workbook.ContentTypeProperties[index].IsNillable = false;
            index = workbook.ContentTypeProperties.Add("MK32", DateTime.Now.ToString("yyyy-MM-dd'T'hh:mm:ss"), "DateTime");
            workbook.ContentTypeProperties[index].IsNillable = true;
            workbook.Save(outputDir + "WorkingWithContentTypeProperties_out.xlsx");
            // ExEnd:1

            Console.WriteLine("WorkingWithContentTypeProperties executed successfully.");
        }
    }
}

```
