---
title: Unprotect Simple Excel Sheet
linktitle: Unprotect Simple Excel Sheet
second_title: Aspose.Cells for .NET API Reference
description: Learn how to Unprotect an Excel spreadsheet with Aspose.Cells for .NET. Step by step tutorial in C#.
type: docs
weight: 30
url: /net/unprotect-excel-sheet/unprotect-simple-excel-sheet/
---
In this tutorial, we will guide you through the steps required to unlock a simple Excel spreadsheet using the Aspose.Cells library for .NET.

## Step 1: Preparing the environment

Before you start, make sure you have Aspose.Cells for .NET installed on your machine. Download the library from Aspose official website and follow the installation instructions provided.

## Step 2: Configuring the document directory path

In the provided source code, you need to specify the directory path where the Excel file you want to unlock is located. Modify the `dataDir` variable by replacing "YOUR DOCUMENT DIRECTORY" with the absolute path of the directory on your machine.

```csharp
// The path to the documents directory.
string dataDir = "PATH TO YOUR DOCUMENTS DIRECTORY";
```

## Step 3: Creating a Workbook Object

To start, we need to create a Workbook object that represents our Excel file. Use the Workbook class constructor and specify the full path of the Excel file to open.

```csharp
// Instantiating a Workbook object
Workbook workbook = new Workbook(dataDir + "book1.xls");
```

## Step 4: Accessing the spreadsheet

Next, we need to navigate to the first worksheet in the Excel file. Use the `Worksheets` property of the Workbook object to access the collection of worksheets, then use the `[0]` index to access the first sheet.

```csharp
// Accessing the first worksheet in the Excel file
Worksheet worksheet = workbook.Worksheets[0];
```

## Step 5: Unlocking the Spreadsheet

Now we will unlock the worksheet using the `Unprotect()` method of the Worksheet object. This method does not require a password.

```csharp
// Unprotecting the worksheet without a password
worksheet.Unprotect();
```

## Step 6: Saving the unlocked Excel file

Once the spreadsheet is unlocked, we can save the final Excel file. Use the `Save()` method to specify the full path of the output file and the save format.

```csharp
// Saving the Workbook
workbook.Save(dataDir + "output.out.xls", SaveFormat.Excel97To2003);
```
### Sample source code for Unprotect Simple Excel Sheet using Aspose.Cells for .NET 
```csharp
// The path to the documents directory.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Instantiating a Workbook object
Workbook workbook = new Workbook(dataDir + "book1.xls");
// Accessing the first worksheet in the Excel file
Worksheet worksheet = workbook.Worksheets[0];
// Unprotecting the worksheet without a password
worksheet.Unprotect();
// Saving the Workbook
workbook.Save(dataDir + "output.out.xls", SaveFormat.Excel97To2003);
```

## Conclusion

Congratulation ! You have now learned how to unlock a simple Excel spreadsheet using Aspose.Cells for .NET. By following the steps in this tutorial, you can easily apply this feature to your own projects.

Feel free to explore more features of Aspose.Cells
for more advanced operations on Excel files.

### FAQs

#### Q: What precautions should I take when unlocking an Excel spreadsheet?

A: When unlocking an Excel spreadsheet, make sure you have the necessary permissions to access the file. Also, be sure to use the correct unlock method and provide the correct password, if applicable.

#### Q: How do I know if the spreadsheet is password protected?

A: You can check if a worksheet is password protected using properties or methods provided by the Aspose.Cells library for .NET. For example, you can use the `IsProtected()` method of the Worksheet object to check if the worksheet is protected.

#### Q: I get an exception when trying to unlock the spreadsheet. What should I do ?

A: If you encounter an exception while unlocking the spreadsheet, please make sure you have correctly specified the path to the Excel file and check that you have the necessary permissions to access it. If the problem persists, feel free to contact Aspose.Cells support for further assistance.