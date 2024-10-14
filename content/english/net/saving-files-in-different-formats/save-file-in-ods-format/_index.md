---
title: Save File in ODS Format
linktitle: Save File in ODS Format
second_title: Aspose.Cells .NET Excel Processing API
description: 
type: docs
weight: 14
url: /net/saving-files-in-different-formats/save-file-in-ods-format/
---

## Complete Source Code
```csharp
using System.IO;

using Aspose.Cells;

namespace Aspose.Cells.Examples.CSharp.Files.Handling
{
    public class SaveInODSFormat
    {
        public static void Run()
        {
            // ExStart:1
            // The path to the documents directory.
            string dataDir = "Your Document Directory";

            // Creating a Workbook object
            Workbook workbook = new Workbook();

            // Save in ods format
            workbook.Save(dataDir + "output.ods");
            // ExEnd:1
            }
        }
  }

```
