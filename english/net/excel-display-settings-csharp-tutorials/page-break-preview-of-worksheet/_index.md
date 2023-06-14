---
title: Page Break Preview Of Worksheet
linktitle: Page Break Preview Of Worksheet
second_title: Aspose.Cells for .NET API Reference
description: Step by step guide to show page break preview of worksheet using Aspose.Cells for .NET.
type: docs
weight: 110
url: /net/excel-display-settings-csharp-tutorials/page-break-preview-of-worksheet/
---
In this tutorial, we are going to explain how to show the page break preview of an worksheet using Aspose.Cells for .NET. Follow these steps to get the desired result:

## Step 1: Setting up the environment

Make sure you have installed Aspose.Cells for .NET and set up your development environment. Also, make sure you have a copy of the Excel file you want to display the page break preview on.

## Step 2: Import the necessary dependencies

Add the necessary directives to use the classes from Aspose.Cells:

```csharp
using Aspose.Cells;
using System.IO;
```

## Step 3: Code initialization

Start by initializing the path to the directory containing your Excel documents:

```csharp
string dataDir = "YOUR DOCUMENTS DIRECTORY";
```

## Step 4: Opening the Excel file

Create a `FileStream` object containing the Excel file to open:

```csharp
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
```

Instantiate a `Workbook` object and open the Excel file using the file stream:

```csharp
Workbook workbook = new Workbook(fstream);
```

## Step 5: Accessing the Spreadsheet

Navigate to the first worksheet in the Excel file:

```csharp
Worksheet worksheet = workbook.Worksheets[0];
```

## Step 6: Displaying the page-by preview

Enable page-by preview for the spreadsheet:

```csharp
worksheet. IsPageBreakPreview = true;
```

## Step 7: Saving Changes

Save the changes made to the Excel file:

```csharp
workbook.Save(dataDir + "output.xls");
```

## Step 8: Closing the file stream

Close the file stream to release all resources:

```csharp
fstream.Close();
```

### Sample source code for Page Break Preview Of Worksheet using Aspose.Cells for .NET 
```csharp
// The path to the documents directory.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Creating a file stream containing the Excel file to be opened
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
// Instantiating a Workbook object
// Opening the Excel file through the file stream
Workbook workbook = new Workbook(fstream);
// Accessing the first worksheet in the Excel file
Worksheet worksheet = workbook.Worksheets[0];
// Displaying the worksheet in page break preview
worksheet.IsPageBreakPreview = true;
// Saving the modified Excel file
workbook.Save(dataDir + "output.xls");
// Closing the file stream to free all resources
fstream.Close();
```

## Conclusion

In this tutorial, you learned how to display the page break preview of an worksheet using Aspose.Cells for .NET. By following the steps described, you can easily control the appearance and layout of your Excel files.

## Frequently Asked Questions (FAQ)

**What is Aspose.Cells for .NET?**

Aspose.Cells for .NET is a popular software library for manipulating Excel files in .NET applications.

**Where can I find documentation for Aspose.Cells for .NET?**

Full documentation of Aspose.Cells for .NET is available on Aspose official website.

**Can I show the page-by preview for a specific worksheet instead of the whole worksheet?**

Yes, using Aspose.Cells you can enable page break preview for a specific worksheet by accessing the corresponding Worksheet object.

**Does Aspose.Cells support other Excel file editing features?**

Yes, Aspose.Cells offers a wide range of features for editing and manipulating Excel files, such as adding data, formatting, creating charts, etc.

**Does Aspose.Cells only work with Excel files in .xls format?**

No, Aspose.Cells supports various Excel file formats including .xls and .xlsx.
	