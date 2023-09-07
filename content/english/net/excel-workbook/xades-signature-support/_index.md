---
title: Xades Signature Support
linktitle: Xades Signature Support
second_title: Aspose.Cells for .NET API Reference
description: Learn how to add a Xades signature to an Excel file using Aspose.Cells for .NET.
type: docs
weight: 190
url: /net/excel-workbook/xades-signature-support/
---
In this article, we will take you step by step to explain the C# source code below, which is about Xades signature support using Aspose.Cells library for .NET. You will find out how to use this library to add a Xades digital signature to an Excel file. We will also provide you with an overview of the signing process and its execution. Follow the steps below to get conclusive results.

## Step 1: Define source and output directories
To start, we need to define the source and output directories in our code. These directories indicate where the source files are located and where the output file will be saved. Here is the corresponding code:

```csharp
// Source directory
string sourceDir = RunExamples.Get_SourceDirectory();
// Output directory
string outputDir = RunExamples.Get_OutputDirectory();
```

Be sure to adapt the directory paths as needed.

## Step 2: Loading the Excel workbook
The next step is to load the Excel workbook on which we want to add the Xades digital signature. Here is the code to load the workbook:

```csharp
Workbook workbook = new Workbook(sourceDir + "sourceFile.xlsx");
```

Make sure to specify the source file name correctly in the code.

## Step 3: Configuring the digital signature
Now we will configure the Xades digital signature by providing the necessary information. We must specify the PFX file containing the digital certificate, as well as the associated password. Here is the corresponding code:

```csharp
string password = "pfxPassword";
string pfx = "pfxFile";
DigitalSignature signature = new DigitalSignature(File.ReadAllBytes(pfx), password, "testXAdES", DateTime.Now);
signature.XAdESType = XAdESType.XAdES;
```

Be sure to replace "pfxPassword" with your actual password and "pfxFile" with the path to the PFX file.

## Step 4: Adding the digital signature
Now that we have configured the digital signature, we can add it to the Excel workbook. Here is the corresponding code:

```csharp
DigitalSignatureCollection dsCollection = new DigitalSignatureCollection();
dsCollection.Add(signature);
workbook.SetDigitalSignature(dsCollection);
```

This step adds the Xades digital signature to the Excel workbook.

## Step 5: Saving the workbook with the signature
Finally, we save the Excel workbook with the digital signature added. Here is the corresponding code:

```csharp
workbook.Save(outputDir + "XAdESSignatureSupport_out.xlsx");
```

Make sure to adapt the name of the output file according to your needs.

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

## Conclusion
Congratulation ! You have learned how to use the Aspose.Cells library for .NET to add a Xades digital signature to an Excel file. By following the steps provided in this article, you will be able to implement this functionality in your own projects. Feel free to experiment more with the library and discover other powerful features it offers.

### FAQs

#### Q: What is Xades?

A: Xades is an advanced electronic signature standard used to ensure the integrity and authenticity of digital documents.

#### Q: Can I use other types of digital signatures with Aspose.Cells?

A: Yes, Aspose.Cells also supports other types of digital signatures, such as XMLDSig signatures and PKCS#7 signatures.

#### Q: Can I apply a signature to other file types than Excel files?
 
A: Yes, Aspose.Cells also allows applying digital signatures to other supported file types such as Word, PDF and PowerPoint files.
