---
title: Encrypting Files in .NET
linktitle: Encrypting Files in .NET
second_title: Aspose.Cells .NET Excel Processing API
description: 
type: docs
weight: 11
url: /net/security-and-encryption/encrypting-files/
---

## Complete Source Code
```csharp
using System.IO;

using Aspose.Cells;

namespace Aspose.Cells.Examples.CSharp.Files.Utility
{
    public class EncryptingFiles
    {
        public static void Run()
        {
            // ExStart:1
            // The path to the documents directory.
            string dataDir = "Your Document Directory";

            // Instantiate a Workbook object.
            // Open an excel file.
            Workbook workbook = new Workbook(dataDir + "Book1.xls");

            // Specify XOR encryption type.
            workbook.SetEncryptionOptions(EncryptionType.XOR, 40);

            // Specify Strong Encryption type (RC4,Microsoft Strong Cryptographic Provider).
            workbook.SetEncryptionOptions(EncryptionType.StrongCryptographicProvider, 128);

            // Password protect the file.
            workbook.Settings.Password = "1234";

            // Save the excel file.
            workbook.Save(dataDir + "encryptedBook1.out.xls");
            // ExEnd:1
        }
        public static void SpecifyPasswordToModifyOption()
        {
            // ExStart:SpecifyPasswordToModifyOption
            // The path to the documents directory.
            string dataDir = "Your Document Directory";

            // Instantiate a Workbook object.
            // Open an excel file.
            Workbook workbook = new Workbook(dataDir + "Book1.xls");
           
            // Set the password for modification.
            workbook.Settings.WriteProtection.Password = "1234";           

            // Save the excel file.
            workbook.Save(dataDir + "SpecifyPasswordToModifyOption.out.xls");
            // ExEnd:SpecifyPasswordToModifyOption
        }
    }
}

```
