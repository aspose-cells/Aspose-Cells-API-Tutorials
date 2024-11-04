---
title: Check if VBA Project is Protected and Locked for Viewing
linktitle: Check if VBA Project is Protected and Locked for Viewing
second_title: Aspose.Cells .NET Excel Processing API
description: 
type: docs
weight: 10
url: /net/workbook-vba-project/check-vba-project-protection/
---

## Complete Source Code
```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;

namespace Aspose.Cells.Examples.CSharp.WorkbookVBAProject
{
    class CheckifVBAProjectisProtectedandLockedforViewing
    {
        public static void Run()
        {
            //ExStart:CheckifVBAProjectisProtectedandLockedforViewing

            //The path to the documents directory.
            string dataDir = "Your Document Directory";

            //Load your source Excel file.
            Workbook wb = new Workbook(dataDir + "sampleCheckifVBAProjectisProtected.xlsm");

            //Access the VBA project of the workbook.
            Aspose.Cells.Vba.VbaProject vbaProject = wb.VbaProject;

            //Whether "Lock project for viewing" is true or not.
            Console.WriteLine("Is VBA Project Locked for Viewing: " + vbaProject.IslockedForViewing);

            //ExEnd:CheckifVBAProjectisProtectedandLockedforViewing
        }
    }
}

```
