---
title: Lock Cells in Worksheet using Aspose.Cells
linktitle: Lock Cells in Worksheet using Aspose.Cells
second_title: Aspose.Cells .NET Excel Processing API
description: 
type: docs
weight: 25
url: /net/worksheet-security/lock-cells/
---

## Complete Source Code
```csharp
using System.IO;

using Aspose.Cells;

namespace Aspose.Cells.Examples.CSharp.Worksheets.Security
{
    public class LockCell
    {
        public static void Run()
        {
            // ExStart:1
            // The path to the documents directory.
            string dataDir = "Your Document Directory";
            Workbook workbook = new Workbook(dataDir + "Book1.xlsx");

            // Accessing the first worksheet in the Excel file
            Worksheet worksheet = workbook.Worksheets[0];

            worksheet.Cells["A1"].GetStyle().IsLocked = true;
            // Finally, Protect the sheet now.

            worksheet.Protect(ProtectionType.All);
            workbook.Save(dataDir + "output.xlsx");

            // ExEnd:1


        }
    }
}

```
