---
title: Other Print Options in Worksheet
linktitle: Other Print Options in Worksheet
second_title: Aspose.Cells .NET Excel Processing API
description: 
type: docs
weight: 17
url: /net/worksheet-page-setup-features/other-print-options/
---

## Complete Source Code
```csharp
using System.IO;
using Aspose.Cells;
using System;

namespace Aspose.Cells.Examples.CSharp.Worksheets.PageSetupFeatures
{
    public class OtherPrintOptions
    {
        public static void Run()
        {
            // ExStart:1
            // The path to the documents directory.
            string dataDir = "Your Document Directory";

            // Instantiating a Workbook object
            Workbook workbook = new Workbook();

            // Obtaining the reference of the PageSetup of the worksheet
            PageSetup pageSetup = workbook.Worksheets[0].PageSetup;

            // Allowing to print gridlines
            pageSetup.PrintGridlines = true;

            // Allowing to print row/column headings
            pageSetup.PrintHeadings = true;

            // Allowing to print worksheet in black & white mode
            pageSetup.BlackAndWhite = true;

            // Allowing to print comments as displayed on worksheet
            pageSetup.PrintComments = PrintCommentsType.PrintInPlace;

            // Allowing to print worksheet with draft quality
            pageSetup.PrintDraft = true;

            // Allowing to print cell errors as N/A
            pageSetup.PrintErrors = PrintErrorsType.PrintErrorsNA;

            // Save the workbook.
            workbook.Save(dataDir + "OtherPrintOptions_out.xls");
            // ExEnd:1
        }
    }
}

```
