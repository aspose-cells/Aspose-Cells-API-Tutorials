---
title: Add Digital Signature To An Already Signed Excel File
linktitle: Add Digital Signature To An Already Signed Excel File
second_title: Aspose.Cells for .NET API Reference
description: Easily add digital signatures to existing Excel files with Aspose.Cells for .NET.
type: docs
weight: 30
url: /net/excel-workbook/add-digital-signature-to-an-already-signed-excel-file/
---
In this step-by-step guide, we will explain the provided C# source code that will allow you to add a digital signature to an already signed Excel file using Aspose.Cells for .NET. Follow the steps below to add a new digital signature to an existing Excel file.

## Step 1: Set source and output directories

```csharp
// source directory
string sourceDir = RunExamples.Get_SourceDirectory();

// Output directory
string outputDir = RunExamples.Get_OutputDirectory();
```

In this first step, we define the source and output directories that will be used to load the existing Excel file and save the file with the new digital signature.

## Step 2: Load existing Excel file

```csharp
// Load the already signed Excel workbook
Aspose.Cells.Workbook workbook = new Aspose.Cells.Workbook(sourceDir + "sampleDigitallySignedByCells.xlsx");
```

Here we load the already signed Excel file using the `Workbook` class of Aspose.Cells.

## Step 3: Create the collection of digital signatures

```csharp
// Create the collection of digital signatures
Aspose.Cells.DigitalSignatures.DigitalSignatureCollection dsCollection = new Aspose.Cells.DigitalSignatures.DigitalSignatureCollection();
```

We create a new collection of digital signatures using the `DigitalSignatureCollection` class.

## Step 4: Create a new certificate

```csharp
// Create a new certificate
System.Security.Cryptography.X509Certificates.X509Certificate2 certificate = new System.Security.Cryptography.X509Certificates.X509Certificate2(certFileName, password);
```

Here we create a new certificate from the provided file and password.

## Step 5: Add a new digital signature to the collection

```csharp
// Create a new digital signature
Aspose.Cells.DigitalSignatures.DigitalSignature signature = new Aspose.Cells.DigitalSignatures.DigitalSignature(certificate, "Aspose.Cells added a new digital signature to the already signed workbook.", DateTime.Now);

// Add the digital signature to the collection
dsCollection.Add(signature);
```

We create a new digital signature using the `DigitalSignature` class and add it to the collection of digital signatures.

## Step 6: Add the collection of digital signatures to the workbook

```csharp
// Add the collection of digital signatures to the workbook
workbook.AddDigitalSignature(dsCollection);
```

We add the collection of digital signatures to the existing Excel workbook using the `AddDigitalSignature()` method.

## Step 7: Save and close the workbook

```csharp
// Save the workbook and close it
workbook.Save(outputDir + "outputDigitallySignedByCells.xlsx");
workbook.Dispose();
```

We save the workbook with the new digital signature to the specified output directory, then close it and release the associated resources.

### Sample source code for Add Digital Signature To An Already Signed Excel File using Aspose.Cells for .NET 
```csharp
//Source directory
string sourceDir = RunExamples.Get_SourceDirectory();
//Output directory
string outputDir = RunExamples.Get_OutputDirectory();
//Certificate file and its password
string certFileName = sourceDir + "AsposeDemo.pfx";
string password = "aspose";
//Load the workbook which is already digitally signed to add new digital signature
Aspose.Cells.Workbook workbook = new Aspose.Cells.Workbook(sourceDir + "sampleDigitallySignedByCells.xlsx");
//Create the digital signature collection
Aspose.Cells.DigitalSignatures.DigitalSignatureCollection dsCollection = new Aspose.Cells.DigitalSignatures.DigitalSignatureCollection();
//Create new certificate
System.Security.Cryptography.X509Certificates.X509Certificate2 certificate = new System.Security.Cryptography.X509Certificates.X509Certificate2(certFileName, password);
//Create new digital signature and add it in digital signature collection
Aspose.Cells.DigitalSignatures.DigitalSignature signature = new Aspose.Cells.DigitalSignatures.DigitalSignature(certificate, "Aspose.Cells added new digital signature in existing digitally signed workbook.", DateTime.Now);
dsCollection.Add(signature);
//Add digital signature collection inside the workbook
workbook.AddDigitalSignature(dsCollection);
//Save the workbook and dispose it.
workbook.Save(outputDir + "outputDigitallySignedByCells.xlsx");
workbook.Dispose();
Console.WriteLine("AddDigitalSignatureToAnAlreadySignedExcelFile executed successfully.\r\n");
```

## Conclusion

Congratulation ! You have now learned how to add a digital signature to an already signed Excel file using Aspose.Cells for .NET. Digital signatures add an extra layer of security to your Excel files, ensuring their authenticity and integrity.

### FAQS

#### Q: What is Aspose.Cells for .NET?

A: Aspose.Cells for .NET is a powerful class library that allows .NET developers to create, modify, convert and manipulate Excel files with ease.

#### Q: What is a digital signature in an Excel file?

A: A digital signature in an Excel file is an electronic mark that guarantees the authenticity, integrity and origin of the document. It is used to verify that the file has not been modified since it was signed and comes from a reliable source.

#### Q: What are the benefits of adding a digital signature to an Excel file?

A: Adding a digital signature to an Excel file provides several benefits, including protection against unauthorized changes, ensuring data integrity, authenticating the author of the document, and providing confidence in the information 'it contains.

#### Q: Can I add multiple digital signatures to an Excel file?

A: Yes, Aspose.Cells allows you to add multiple digital signatures to an Excel file. You can create a collection of digital signatures and add them to the file in one operation.

#### Q: What are the requirements for adding a digital signature to an Excel file?

A: To add a digital signature to an Excel file, you need a valid digital certificate which will be used to sign the document. Make sure you have the correct certificate and password before adding the digital signature.
