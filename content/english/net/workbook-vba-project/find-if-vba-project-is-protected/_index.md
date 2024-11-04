---
title: Find out if VBA Project is Protected using Aspose.Cells
linktitle: Find out if VBA Project is Protected using Aspose.Cells
second_title: Aspose.Cells .NET Excel Processing API
description: 
type: docs
weight: 12
url: /net/workbook-vba-project/find-if-vba-project-is-protected/
---

## Complete Source Code
```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;

namespace Aspose.Cells.Examples.CSharp.WorkbookVBAProject
{
    class FindoutifVBAProjectisProtected
    {
        public static void Run()
        {
            //ExStart:FindoutifVBAProjectisProtected

            //Create a workbook.
            Workbook wb = new Workbook();

            //Access the VBA project of the workbook.
            Aspose.Cells.Vba.VbaProject vbaProj = wb.VbaProject;

            //Find out if VBA Project is Protected using IsProtected property.
            Console.WriteLine("IsProtected - Before Protecting VBA Project: " + vbaProj.IsProtected);

            //Protect the VBA project.
            vbaProj.Protect(true, "11");

            //Find out if VBA Project is Protected using IsProtected property.
            Console.WriteLine("IsProtected - After Protecting VBA Project: " + vbaProj.IsProtected);

            //ExEnd:FindoutifVBAProjectisProtected
        }
    }
}

```
