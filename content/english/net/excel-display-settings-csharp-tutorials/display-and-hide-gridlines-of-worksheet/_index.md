---
title: Display And Hide Gridlines Of Worksheet
linktitle: Display And Hide Gridlines Of Worksheet
second_title: Aspose.Cells for .NET API Reference
description: Control the display of gridlines in Excel worksheet with Aspose.Cells for .NET.
type: docs
weight: 30
url: /net/excel-display-settings-csharp-tutorials/display-and-hide-gridlines-of-worksheet/
---
In this tutorial, we will show you how to show and hide gridlines in an Excel worksheet using C# source code with Aspose.Cells for .NET. Follow the steps below to get the desired result.

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

## Step 3: Go to the first worksheet and hide the gridlines

Access the first worksheet in the Excel file using the `Worksheets` property of the `Workbook` object. Then use the `IsGridlinesVisible` property of the `Worksheet` object to hide the gridlines.

```csharp
Worksheet worksheet = workbook.Worksheets[0];
worksheet.IsGridlinesVisible = false;
```

## Step 4: Save Changes

Once you have made the necessary changes, save the modified Excel file using the `Save` method of the `Workbook` object.

```csharp
workbook.Save(dataDir + "output.xls");
```

### Sample source code for Display And Hide Gridlines Of Worksheet using Aspose.Cells for .NET 

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
// Hiding the grid lines of the first worksheet of the Excel file
worksheet.IsGridlinesVisible = false;
// Saving the modified Excel file
workbook.Save(dataDir + "output.xls");
// Closing the file stream to free all resources
fstream.Close();
```

## Conclusion

This step-by-step guide showed you how to show and hide gridlines in an Excel spreadsheet using Aspose.Cells for .NET. Using the provided C# source code, you can easily customize the display of gridlines in your Excel files.

### Frequently Asked Questions (FAQ)

#### What is Aspose.Cells for .NET?

Aspose.Cells for .NET is a powerful library for manipulating Excel files in .NET applications.

#### How can I install Aspose.Cells for .NET?

To install Aspose.Cells for .NET, you need to download the relevant package from [Aspose Releases](https://releases/aspose.com/cells/net/) and add it to your .NET project.

#### How can I show or hide gridlines in an Excel spreadsheet with Aspose.Cells for .NET?

You can use the `IsGridlinesVisible` property of the `Worksheet` object to show or hide gridlines. Set it to `true` to show them and to `false` to hide them.

#### What other Excel file formats are supported by Aspose.Cells for .NET?

Aspose.Cells for .NET supports various Excel file formats, such as XLS, XLSX, CSV, HTML, PDF, and many more.


