---
title: Create Shared Workbook using Aspose.Cells
linktitle: Create Shared Workbook using Aspose.Cells
second_title: Aspose.Cells .NET Excel Processing API
description: 
type: docs
weight: 16
url: /net/workbook-operations/create-shared-workbook/
---

## Complete Source Code
```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;

using Aspose.Cells;

namespace Aspose.Cells.Examples.CSharp._Workbook
{
    class CreateSharedWorkbook 
    {
        public static void Run()
        {
            //Output directory
            string outputDir = "Your Document Directory";

            //Create Workbook object
            Workbook wb = new Workbook();

            //Share the Workbook
            wb.Settings.Shared = true;

            //Save the Shared Workbook
            wb.Save(outputDir + "outputSharedWorkbook.xlsx");

            Console.WriteLine("CreateSharedWorkbook executed successfully.\r\n");
        }
    }
}

```
