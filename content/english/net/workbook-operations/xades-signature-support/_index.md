---
title: XAdESSignature Support in Workbook using Aspose.Cells
linktitle: XAdESSignature Support in Workbook using Aspose.Cells
second_title: Aspose.Cells .NET Excel Processing API
description: 
type: docs
weight: 29
url: /net/workbook-operations/xades-signature-support/
---

## Complete Source Code
```csharp
using Aspose.Cells.DigitalSignatures;
using System;
using System.IO;

namespace Aspose.Cells.Examples.CSharp._Workbook
{
    public class XAdESSignatureSupport
    {
        public static void Run()
        {
            // ExStart:1
            //Source directory
            string sourceDir = "Your Document Directory";

            //Output directory
            string outputDir = "Your Document Directory";

            Workbook workbook = new Workbook(sourceDir + "sourceFile.xlsx");
            string password = "pfxPassword";
            string pfx = "pfxFile";

            DigitalSignature signature = new DigitalSignature(File.ReadAllBytes(pfx), password, "testXAdES", DateTime.Now);

            signature.XAdESType = XAdESType.XAdES;
            DigitalSignatureCollection dsCollection = new DigitalSignatureCollection();
            dsCollection.Add(signature);

            workbook.SetDigitalSignature(dsCollection);

            workbook.Save(outputDir + "XAdESSignatureSupport_out.xlsx");
            // ExEnd:1

            Console.WriteLine("XAdESSignatureSupport executed successfully.");
        }
    }
}

```
