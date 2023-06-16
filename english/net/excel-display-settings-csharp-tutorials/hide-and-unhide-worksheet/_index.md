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

## Step 1: Preparing the environment

Before you start, make sure you have Aspose.Cells for .NET installed on your system. If you don't already have it installed, you can download it from Aspose's official website. Once installed, you can create a new project in your preferred integrated development environment (IDE).

## Step 2: Import required namespaces

In your C# source file, add the necessary namespaces to use the features of Aspose.Cells. Add the following lines to the beginning of your file:

```csharp
using Aspose.Cells;
using System.IO;
```

## Step 3: Load the Excel file

Before hiding or unhiding a worksheet, you must load the Excel file into your application. Make sure you have the Excel file you want to use in the same directory as your project. Use the following code to load the Excel file:

```csharp
string dataDir = "PATH TO YOUR DOCUMENTS DIRECTORY";
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
Workbook workbook = new Workbook(fstream);
```

Be sure to replace "PATH TO YOUR DOCUMENTS DIRECTORY" with the actual path to the directory containing your Excel file.

## Step 4: Access the spreadsheet

Once the Excel file is loaded, you can navigate to the worksheet you want to hide or unhide. Use the following code to access the first worksheet in the file:

```csharp
Worksheet worksheet = workbook.Worksheets[0];
```

## Step 5: Hide the worksheet

Now that you have accessed the worksheet, you can hide it using the `IsVisible` property. Use the following code to hide the first worksheet in the file:

```csharp
worksheet. IsVisible = false;
```

## Step 6: Redisplay the worksheet

If you want to redisplay the previously hidden worksheet, you can use the same code by changing the value of the `IsVisible` property. Use the following code to redisplay the first worksheet:

```csharp
worksheet. IsVisible = true;
```

## Step 7: Save Changes

Once you

  have hidden or unhided the worksheet as needed, you must save the changes to the Excel file. Use the following code to save changes:

```csharp
workbook.Save(dataDir + "output.out.xls");
fstream.Close();
```

Make sure to specify the correct output path to save the modified Excel file.

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

You can install Aspose.Cells for .NET by downloading the relevant NuGet package from [Aspose Releases](https://releases/aspose.com/cells/net/) and adding it to your Visual Studio project.

**What is the minimum required version of .NET Framework to use Aspose.Cells for .NET?**

Aspose.Cells for .NET supports .NET Framework 2.0 and later.

**Can I open and edit existing Excel files with Aspose.Cells for .NET?**

Yes, you can open and edit existing Excel files using Aspose.Cells for .NET. You can access worksheets, cells, formulas and other elements of the Excel file.

**Does Aspose.Cells for .NET support reporting and exporting to other file formats?**

Yes, Aspose.Cells for .NET supports report generation and export to formats like PDF, HTML, CSV, TXT, etc.

**Is the modification of the Excel file permanent?**

Yes, the Excel file edit is permanent once you save it. Be sure to save a backup copy before making any changes to the original file.
