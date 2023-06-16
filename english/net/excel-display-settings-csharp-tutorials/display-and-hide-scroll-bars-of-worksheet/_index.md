---
title: Display And Hide Scroll Bars Of Worksheet
linktitle: Display And Hide Scroll Bars Of Worksheet
second_title: Aspose.Cells for .NET API Reference
description: Display or hide scroll bars in Excel worksheet using Aspose.Cells for .NET.
type: docs
weight: 50
url: /net/excel-display-settings-csharp-tutorials/display-and-hide-scroll-bars-of-worksheet/
---
In this tutorial, we will show you how to display or hide vertical and horizontal scroll bars in an Excel worksheet using C# source code with Aspose.Cells for .NET. Follow the steps below to get the desired result.

## Step 1: Import the necessary libraries

Make sure you have installed the Aspose.Cells library for .NET and import the necessary libraries into your C# project.

```csharp
using Aspose.Cells;
using System.IO;
```

## Step 2: Set directory path and open Excel file

Set the path to the directory containing your Excel file, then open the file by creating a file stream and instantiating a `Workbook` object.

```csharp
string dataDir = "YOUR DOCUMENTS DIRECTORY";
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
Workbook workbook = new Workbook(fstream);
```

## Step 3: Hide Scrollbars

Use the `IsVScrollBarVisible` and `IsHScrollBarVisible` properties of the `Workbook.Settings` object to hide the vertical and horizontal scrollbars of the worksheet.

```csharp
workbook.Settings.IsVScrollBarVisible = false;
workbook.Settings.IsHScrollBarVisible = false;
```

## Step 4: Save Changes

Once you have made the necessary changes, save the modified Excel file using the `Save` method of the `Workbook` object.

```csharp
workbook.Save(dataDir + "output.xls");
```

### Sample source code for Display And Hide Scroll Bars Of Worksheet using Aspose.Cells for .NET 

```csharp
// The path to the documents directory.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Creating a file stream containing the Excel file to be opened
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
// Instantiating a Workbook object
// Opening the Excel file through the file stream
Workbook workbook = new Workbook(fstream);
// Hiding the vertical scroll bar of the Excel file
workbook.Settings.IsVScrollBarVisible = false;
// Hiding the horizontal scroll bar of the Excel file
workbook.Settings.IsHScrollBarVisible = false;
// Saving the modified Excel file
workbook.Save(dataDir + "output.xls");
// Closing the file stream to free all resources
fstream.Close();
```

## Conclusion

This step-by-step guide showed you how to display or hide vertical and horizontal scroll bars in an Excel spreadsheet using Aspose.Cells for .NET. Using the provided C# source code, you can easily customize the display of scrollbars in your Excel files.

## Frequently Asked Questions (FAQ)

**What is Aspose.Cells for .NET?**

Aspose.Cells for .NET is a powerful library for manipulating Excel files in .NET applications.

**How can I install Aspose.Cells for .NET?**

To install Aspose.Cells for .NET, you need to download the relevant package from [Aspose Releases](https://releases/aspose.com/cells/net/) and add it to your .NET project.

**How can I display or hide scrollbars in an Excel spreadsheet with Aspose.Cells for .NET?**

You can use the `IsVScrollBarVisible` and `IsHScrollBarVisible` properties of the `Workbook.Settings` object to display or hide the vertical and horizontal scroll bar respectively in an Excel worksheet.

**What other Excel file formats are supported by Aspose.Cells for .NET?**

Aspose.Cells for .NET supports a variety of Excel file formats, such as XLS, XLSX, CSV, HTML, PDF, etc.
