---
title: Allow User To Edit Ranges In Excel Worksheet
linktitle: Allow User To Edit Ranges In Excel Worksheet
second_title: Aspose.Cells for .NET API Reference
description: Allow users to edit specific ranges in an Excel spreadsheet using Aspose.Cells for .NET. Step by step guide with source code in C#.
type: docs
weight: 10
url: /net/protect-excel-file/allow-user-to-edit-ranges-in-excel-worksheet/
---
In this guide, we will walk you through how to use Aspose.Cells for .NET to allow the user to edit specific ranges in an Excel spreadsheet. Follow the steps below to accomplish this task.

## Step 1: Setting up the environment

Make sure you have set up your development environment and installed Aspose.Cells for .NET. You can download the latest version of the library from Aspose official website.

## Step 2: Import required namespaces

In your C# project, import the necessary namespaces to work with Aspose.Cells:

```csharp
using Aspose.Cells;
```

## Step 3: Setting the path to the documents directory

Declare a `dataDir` variable to specify the path to the directory where you want to save the generated Excel file:

```csharp
string dataDir = "YOUR_DIRECTORY_OF_DOCUMENTS";
```

Be sure to replace `"YOUR_DOCUMENT_DIRECTORY"` with the correct path on your system.

## Step 4: Creating a Workbook Object

Instantiate a new Workbook object that represents the Excel workbook you want to create:

```csharp
Workbook book = new Workbook();
```

## Step 5: Access to the first worksheet

Navigate to the first worksheet in the Excel workbook using the following code:

```csharp
Worksheet sheet = book.Worksheets[0];
```

## Step 6: Retrieving authorized modification ranges

Get the collection of allowed edit ranges using the `AllowEditRanges` property:

```csharp
ProtectedRangeCollection allowRanges = sheet.AllowEditRanges;
```

## Step 7: Define a Protected Range

Define a protected range using the `Add` method of the `AllowEditRanges` collection:

```csharp
int idx = allowRanges.Add("r2", 1, 1, 3, 3);
protectedRange protectedRange = allowRanges[idx];
```

Here we have created a protected range "r2" that spans from cell A1 to cell C3.

## Step 8: Specifying the password

Specify a password for the protected range using the `Password` property:

```csharp
protectedRange.Password = "YOUR_PASSWORD";
```

Be sure to replace `"YOUR_PASSWORD"` with the desired password.

## Step 9: Protecting the worksheet

Protect the worksheet using the `Protect` method of the `Worksheet` object:

```csharp
sheet.Protect(ProtectionType.All);
```

This will protect the spreadsheet by preventing any modification outside the allowed ranges.

## Step 10: Registering the

  Excel file

Save the generated Excel file using the `Save` method of the `Workbook` object:

```csharp
book.Save(dataDir + "protectedrange.out.xls");
```

Be sure to specify the desired file name and the correct path.

### Sample source code for Allow User To Edit Ranges In Excel Worksheet using Aspose.Cells for .NET 
```csharp
// The path to the documents directory.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Create directory if it is not already present.
bool IsExists = System.IO.Directory.Exists(dataDir);
if (!IsExists)
    System.IO.Directory.CreateDirectory(dataDir);
// Instantiate a new Workbook
Workbook book = new Workbook();
// Get the first (default) worksheet
Worksheet sheet = book.Worksheets[0];
// Get the Allow Edit Ranges
ProtectedRangeCollection allowRanges = sheet.AllowEditRanges;
// Define ProtectedRange
ProtectedRange proteced_range;
// Create the range
int idx = allowRanges.Add("r2", 1, 1, 3, 3);
proteced_range = allowRanges[idx];
// Specify the passoword
proteced_range.Password = "123";
// Protect the sheet
sheet.Protect(ProtectionType.All);
// Save the Excel file
book.Save(dataDir + "protectedrange.out.xls");
```

## Conclusion

You have now learned how to use Aspose.Cells for .NET to allow the user to edit specific ranges in an Excel spreadsheet. Feel free to further explore the features offered by Aspose.Cells to meet your specific needs.


### FAQs

#### 1. How to allow user to edit specific ranges in Excel spreadsheet?

You can use the `ProtectedRangeCollection` class to define allowed ranges of modification. Use the `Add` method to create a new protected range with the desired cells.

#### 2. Can I set a password for authorized modification ranges?

Yes, you can specify a password using the `Password` property of the `ProtectedRange` object. This will restrict access only to users with the password.

#### 3. How do I protect the spreadsheet once the allowed ranges are set?

Use the `Protect` method of the `Worksheet` object to protect the worksheet. This will prevent any changes outside of the allowed ranges, possibly prompting for a password if you specified one.