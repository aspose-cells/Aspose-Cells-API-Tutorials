---
title: Protect Entire Worksheet using Aspose.Cells
linktitle: Protect Entire Worksheet using Aspose.Cells
second_title: Aspose.Cells .NET Excel Processing API
description: 
type: docs
weight: 17
url: /net/worksheet-security/protect-worksheet/
---

## Complete Source Code
```csharp
using System.IO;

using Aspose.Cells;

namespace Aspose.Cells.Examples.CSharp.Worksheets.Security.Protecting
{
    public class ProtectingWorksheet
    {
        public static void Run()
        {
            // ExStart:1
            // The path to the documents directory.
            string dataDir = "Your Document Directory";

            // Creating a file stream containing the Excel file to be opened
            FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);

            // Instantiating a Workbook object
            // Opening the Excel file through the file stream
            Workbook excel = new Workbook(fstream);

            // Accessing the first worksheet in the Excel file
            Worksheet worksheet = excel.Worksheets[0];

            // Protecting the worksheet with a password
            worksheet.Protect(ProtectionType.All, "aspose", null);

            // Saving the modified Excel file in default format
            excel.Save(dataDir + "output.out.xls", SaveFormat.Excel97To2003);

            // Closing the file stream to free all resources
            fstream.Close();
            // ExEnd:1

        }
    }
}

```
