---
title: Xades Signature Support
linktitle: Xades Signature Support
second_title: Aspose.Cells for .NET API Reference
description: 
type: docs
weight: 190
url: /net/excel-workbook/xades-signature-support/
---
### Sample source code for Xades Signature Support using Aspose.Cells for .NET 
```csharp
            //Source directory
            string sourceDir = RunExamples.Get_SourceDirectory();
            //Output directory
            string outputDir = RunExamples.Get_OutputDirectory();
            Workbook workbook = new Workbook(sourceDir + "sourceFile.xlsx");
            string password = "pfxPassword";
            string pfx = "pfxFile";
            DigitalSignature signature = new DigitalSignature(File.ReadAllBytes(pfx), password, "testXAdES", DateTime.Now);
            signature.XAdESType = XAdESType.XAdES;
            DigitalSignatureCollection dsCollection = new DigitalSignatureCollection();
            dsCollection.Add(signature);
            workbook.SetDigitalSignature(dsCollection);
            workbook.Save(outputDir + "XAdESSignatureSupport_out.xlsx");
            Console.WriteLine("XAdESSignatureSupport executed successfully.");
```