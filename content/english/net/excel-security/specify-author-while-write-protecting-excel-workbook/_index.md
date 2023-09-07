---
title: Specify Author While Write Protecting Excel Workbook
linktitle: Specify Author While Write Protecting Excel Workbook
second_title: Aspose.Cells for .NET API Reference
description: Learn how to protect and customize your Excel workbooks using Aspose.Cells for .NET. Step by step tutorial in C#.
type: docs
weight: 30
url: /net/excel-security/specify-author-while-write-protecting-excel-workbook/
---

In this tutorial, we will show you how to specify the author when write-protecting an Excel workbook using the Aspose.Cells library for .NET.

## Step 1: Preparing the environment

Before you start, make sure you have Aspose.Cells for .NET installed on your machine. Download the library from Aspose official website and follow the installation instructions provided.

## Step 2: Configuring source and output directories

In the provided source code, you must specify the source and output directories. Modify the `sourceDir` and `outputDir` variables by replacing "YOUR SOURCE DIRECTORY" and "YOUR OUTPUT DIRECTORY" with the respective absolute paths on your machine.

```csharp
// Source directory
string sourceDir = "PATH TO YOUR SOURCE DIRECTORY";

// Output directory
string outputDir = "YOUR OUTPUT DIRECTORY PATH";
```

## Step 3: Creating an empty Excel workbook

To start, we create a Workbook object that represents an empty Excel workbook.

```csharp
// Create empty workbook.
Workbook wb = new Workbook();
```

## Step 4: Write protection with password

Next, we specify a password to write protect the Excel workbook using the `WriteProtection.Password` property of the Workbook object.

```csharp
// Write protect workbook with password.
wb.Settings.WriteProtection.Password = "YOUR_PASSWORD";
```

## Step 5: Author specification

Now we specify the author of the Excel workbook using the `WriteProtection.Author` property of the Workbook object.

```csharp
// Specify author while write protecting workbook.
wb.Settings.WriteProtection.Author = "YOUR_AUTHOR";
```

## Step 6: Backup Protected Excel Workbook

Once the write protection and the author are specified, we can save the Excel workbook in the XLSX format using the `Save()` method.

```csharp
// Save the workbook in XLSX format.
wb.Save(outputDir + "outputSpecifyAuthorWhileWriteProtectingWorkbook.xlsx");
```

### Sample source code for Specify Author While Write Protecting Excel Workbook using Aspose.Cells for .NET 
```csharp
//Source directory
string sourceDir = "YOUR SOURCE DIRECTORY";

//Output directory
string outputDir = "YOUR OUTPUT DIRECTORY";

// Create empty workbook.
Workbook wb = new Workbook();

// Write protect workbook with password.
wb.Settings.WriteProtection.Password = "YOUR_PASSWORD";

// Specify author while write protecting workbook.
wb.Settings.WriteProtection.Author = "YOUR_AUTHOR";

// Save the workbook in XLSX format.
wb.Save(outputDir + "outputSpecifyAuthorWhileWriteProtectingWorkbook.xlsx");

```

## Conclusion

Congratulation ! You have now learned how to specify the author when write-protecting an Excel workbook with Aspose.Cells for .NET. You can apply these steps to your own projects to protect and customize your Excel workbooks.

Feel free to further explore the features of Aspose.Cells for .NET for more advanced operations on Excel files.

## FAQs

#### Q: Can I write protect an Excel workbook without specifying a password?

A: Yes, you can use the Workbook object's `WriteProtect()` method without specifying a password to write-protect an Excel workbook. This will restrict changes to the workbook without requiring a password.

#### Q: How do I remove write protection from an Excel workbook?

A: To remove write protection from an Excel workbook, you can use the `Unprotect()` method of the Worksheet object or the `RemoveWriteProtection()` method of the Workbook object, depending on your specific use case. .

#### Q: I forgot the password to protect my Excel workbook. What can I do ?

A: If you forgot the password to protect your Excel workbook, you can't remove it directly. However, you can try to use specialized third-party tools that provide password recovery features for protected Excel files.

#### Q: Is it possible to specify multiple authors when write-protecting an Excel workbook?

A: No, the Aspose.Cells for .NET library allows specifying a single author when write-protecting an Excel workbook. If you want to specify multiple authors, you will need to consider custom solutions by directly manipulating the Excel file.
