---
title: Protect Excel Worksheet
linktitle: Protect Excel Worksheet
second_title: Aspose.Cells for .NET API Reference
description: Discover in this tutorial how to protect an Excel spreadsheet using Aspose.Cells for .NET. Step by step guide in C#.
type: docs
weight: 50
url: /net/protect-excel-file/protect-excel-worksheet/
---
In this tutorial, we'll look at some C# source code that uses the Aspose.Cells library to protect an Excel spreadsheet. We'll walk through each step of the code and explain how it works. Be sure to follow the instructions carefully to get the desired results.

## Step 1: Prerequisites

Before you start, make sure you have installed the Aspose.Cells library for .NET. You can get it from Aspose official website. Also make sure you have a recent version of Visual Studio or any other C# development environment.

## Step 2: Import required namespaces

To use the Aspose.Cells library, we need to import the necessary namespaces into our code. Add the following lines to the top of your C# source file:

```csharp
using Aspose.Cells;
using System.IO;
```

## Step 3: Load the Excel file

In this step, we will load the Excel file that we want to protect. Be sure to specify the correct path to the directory containing the Excel file. Use the following code to upload the file:

```csharp
// Path to the documents directory.
string dataDir = "YOUR_DIRECTORY_OF_DOCUMENTS";

// Create a stream of files containing the Excel file to open.
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);

// Instantiate a Workbook object.
// Open Excel file via file stream.
Workbook excel = new Workbook(fstream);
```

Be sure to replace `"YOUR_DOCUMENTS_DIR"` with the appropriate path to your documents directory.

## Step 4: Access the spreadsheet

Now that we have loaded the Excel file, we can access the first worksheet. Use the following code to access the first worksheet:

```csharp
// Access to the first worksheet in the Excel file.
Worksheet worksheet = excel.Worksheets[0];
```

## Step 5: Protect the worksheet

In this step, we will protect the spreadsheet using a password. Use the following code to protect the spreadsheet:

```csharp
// Protect the worksheet with a password.
worksheet.Protect(ProtectionType.All, "YOUR_PASSWORD", null);
```

Replace `"YOUR_PASSWORD"` with the password you want to use to protect the spreadsheet.

## Step 6: Save the Modified Excel File Now that we have protected

é the spreadsheet, we will save the modified Excel file in the default format. Use the following code to save the Excel file:

```csharp
// Save the modified Excel file in the default format.
excel.Save(dataDir + "output.out.xls", SaveFormat.Excel97To2003);
```

Make sure to specify the correct path to save the modified Excel file.

## Step 7: Close File Stream

To release all resources, we need to close the file stream used to load the Excel file. Use the following code to close the file stream:

```csharp
// Close file stream to release all resources.
fstream.Close();
```

Be sure to include this step at the end of your code.


### Sample source code for Protect Excel Worksheet using Aspose.Cells for .NET 
```csharp
// The path to the documents directory.
string dataDir = "YOUR DOCUMENT DIRECTORY";
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
```

## Conclusion

Congratulation ! You now have C# source code that allows you to protect an Excel spreadsheet using the Aspose.Cells library for .NET. Be sure to follow the steps carefully and customize the code to your specific needs.

### FAQs (Frequently Asked Questions)

#### Is it possible to protect multiple worksheets in one Excel file?
A: Yes, you can protect multiple worksheets in one Excel file by repeating steps 4-6 for each worksheet.

#### How can I specify specific permissions for authorized users?
A: You can use the additional options provided by the `Protect` method to specify specific permissions for authorized users. See the Aspose.Cells documentation for more information.

#### Can I protect the Excel file itself with a password?
A: Yes, you can password protect the Excel file itself using other methods provided by the Aspose.Cells library. Please refer to the documentation for specific examples.

#### Does the Aspose.Cells library support other Excel file formats?
A: Yes, Aspose.Cells library supports a wide range of Excel file formats, including XLSX, XLSM, XLSB, CSV, etc.