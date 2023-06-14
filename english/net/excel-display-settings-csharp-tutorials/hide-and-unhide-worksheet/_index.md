---
title: Hide And Unhide Worksheet
linktitle: Hide And Unhide Worksheet
second_title: Aspose.Cells for .NET API Reference
description: A powerful library for working with Excel files, including creating, modifying and manipulating data.
type: docs
weight: 90
url: /net/excel-display-settings-csharp-tutorials/hide-and-unhide-worksheet/
---
In this tutorial, we will take you step by step to explain the following C# source code which is used to hide and show a worksheet using Aspose.Cells for .NET. Follow the steps below:

## Step 1: Create a file stream containing the Excel file to open
```csharp
string dataDir = "YOUR DOCUMENTS DIRECTORY";
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
```

## Step 2: Instantiate a Workbook object by opening the Excel file via file flow
```csharp
Workbook workbook = new Workbook(fstream);
```

## Step 3: Access the first worksheet of the Excel file
```csharp
Worksheet worksheet = workbook.Worksheets[0];
```

## Step 4: Hide the first worksheet of the Excel file
```csharp
worksheet. IsVisible = false;
```

## Step 5: Display the first worksheet of the Excel file (if necessary)
```csharp
//worksheet.IsVisible = true;
```

## Step 6: Save modified Excel file in default format (i.e. Excel 2003)
```csharp
workbook.Save(dataDir + "output.out.xls");
```

## Step 7: Close the file stream to release all resources
```csharp
fstream.Close();
```

### Sample source code for Hide And Unhide Worksheet using Aspose.Cells for .NET 

```csharp
// The path to the documents directory.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Creating a file stream containing the Excel file to be opened
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
// Instantiating a Workbook object with opening the Excel file through the file stream
Workbook workbook = new Workbook(fstream);
// Accessing the first worksheet in the Excel file
Worksheet worksheet = workbook.Worksheets[0];
// Hiding the first worksheet of the Excel file
worksheet.IsVisible = false;
// Shows first worksheet of the Excel file
//Worksheet.IsVisible = true;
// Saving the modified Excel file in default (that is Excel 2003) format
workbook.Save(dataDir + "output.out.xls");
// Closing the file stream to free all resources
fstream.Close();
```

## Conclusion

Congratulation ! You have learned how to hide and show a spreadsheet using Aspose.Cells for .NET. You can now use this feature to control the visibility of your spreadsheets in your Excel files.

## Frequently Asked Questions (FAQ)

**How can I install Aspose.Cells for .NET?**

You can install Aspose.Cells for .NET by downloading the relevant NuGet package and adding it to your Visual Studio project.

**What is the minimum required version of .NET Framework to use Aspose.Cells for .NET?**

Aspose.Cells for .NET supports .NET Framework 2.0 and later.

**Can I open and edit existing Excel files with Aspose.Cells for .NET?**

Yes, you can open and edit existing Excel files using Aspose.Cells for .NET. You can access worksheets, cells, formulas and other elements of the Excel file.

**Does Aspose.Cells for .NET support reporting and exporting to other file formats?**

Yes, Aspose.Cells for .NET supports report generation and export to formats like PDF, HTML, CSV, TXT, etc.

**Is the modification of the Excel file permanent?**

Yes, the Excel file edit is permanent once you save it. Be sure to save a backup copy before making any changes to the original file.
