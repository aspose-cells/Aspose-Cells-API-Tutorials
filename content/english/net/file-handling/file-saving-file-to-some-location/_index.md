---
title: Saving File to Some Location
linktitle: Saving File to Some Location
second_title: Aspose.Cells .NET Excel Processing API
description: 
type: docs
weight: 11
url: /net/file-handling/file-saving-file-to-some-location/
---

## Complete Source Code
```csharp
using System.IO;

using Aspose.Cells;
using System;

namespace Aspose.Cells.Examples.CSharp.Files.Handling
{
    public class SavingFiletoSomeLocation
    {
        public static void Run()
        {
            // ExStart:1
            // The path to the documents directory.
            string dataDir = "Your Document Directory";

            string filePath = dataDir + "Book1.xls";

            // Load your source workbook
            Workbook workbook = new Workbook(filePath);

            // Save in Excel 97 ?2003 format
            workbook.Save(dataDir + ".output.xls");
            // OR
            workbook.Save(dataDir + ".output..xls", SaveFormat.Excel97To2003);

            // Save in Excel2007 xlsx format
            workbook.Save(dataDir + ".output.xlsx");

            // Save in Excel2007 xlsb format
            workbook.Save(dataDir + ".output.xlsb");

            // Save in ods format
            workbook.Save(dataDir + ".output.ods");

            // Save in Pdf format
            workbook.Save(dataDir + ".output.pdf");

            // Save in Html format
            workbook.Save(dataDir + ".output.html");

            // Save in SpreadsheetML format
            workbook.Save(dataDir + ".output.xml");

            // ExEnd:1


        }
    }
}
```
