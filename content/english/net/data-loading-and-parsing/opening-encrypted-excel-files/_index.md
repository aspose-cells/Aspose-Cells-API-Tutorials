---
title: Opening Encrypted Excel Files
linktitle: Opening Encrypted Excel Files
second_title: Aspose.Cells .NET Excel Processing API
description: 
type: docs
weight: 10
url: /net/data-loading-and-parsing/opening-encrypted-excel-files/
---

## Complete Source Code
```csharp
using System.IO;

using Aspose.Cells;
using System;

namespace Aspose.Cells.Examples.CSharp.Files.Handling
{
    public class OpeningEncryptedExcelFiles
    {
        public static void Run()
        {
            // ExStart:1
            // The path to the documents directory.
            string dataDir = "Your Document Directory";

            // Instantiate LoadOptions
            LoadOptions loadOptions6 = new LoadOptions();

            // Specify the password
            loadOptions6.Password = "1234";

            // Create a Workbook object and opening the file from its path
            Workbook wbEncrypted = new Workbook(dataDir + "encryptedBook.xls", loadOptions6);
            Console.WriteLine("Encrypted excel file opened successfully!");
            // ExEnd:1
            }
          }
        }

```
