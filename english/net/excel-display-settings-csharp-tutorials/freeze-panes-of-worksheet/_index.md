---
title: Freeze Panes Of Worksheet
linktitle: Freeze Panes Of Worksheet
second_title: Aspose.Cells for .NET API Reference
description: Easily manipulate freeze panes of Excel worksheet with Aspose.Cells for .NET.
type: docs
weight: 70
url: /net/excel-display-settings-csharp-tutorials/freeze-panes-of-worksheet/
---
In this tutorial, we will show you how to lock panes in an Excel worksheet using C# source code with Aspose.Cells for .NET. Follow the steps below to get the desired result.

## Step 1: Import the necessary libraries

Make sure you have installed the Aspose.Cells library for .NET and import the necessary libraries into your C# project.

```csharp
using Aspose.Cells;
```

## Step 2: Set directory path and open Excel file

Set the path to the directory containing your Excel file, then open the file by instantiating a `Workbook` object.

```csharp
string dataDir = "YOUR DOCUMENTS DIRECTORY";
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
Workbook workbook = new Workbook(fstream);
```

## Step 3: Go to spreadsheet and apply pane lock settings

Navigate to the first worksheet in the Excel file using the `Worksheet` object. Then use the `FreezePanes` method to apply the pane lock settings.

```csharp
Worksheet worksheet = workbook.Worksheets[0];
worksheet. FreezePanes(3, 2, 3, 2);
```

In the example above, the panes are locked to the cell in row 3 and column 2.

## Step 4: Save Changes

Once you have made the necessary changes, save the modified Excel file using the `Save` method of the `Workbook` object.

```csharp
workbook.Save(dataDir + "output.xls");
```

### Sample source code for Freeze Panes Of Worksheet using Aspose.Cells for .NET 

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
// Applying freeze panes settings
worksheet.FreezePanes(3, 2, 3, 2);
// Saving the modified Excel file
workbook.Save(dataDir + "output.xls");
// Closing the file stream to free all resources
fstream.Close();
```

## Conclusion

This step-by-step guide showed you how to lock panes in an Excel spreadsheet using Aspose.Cells for .NET. Using the provided C# source code, you can easily customize pane lock settings to better organize and visualize your data in Excel files.

## Frequently Asked Questions (FAQ)

**What is Aspose.Cells for .NET?**

Aspose.Cells for .NET is a powerful library for manipulating Excel files in .NET applications.

**How can I install Aspose.Cells for .NET?**

To install Aspose.Cells for .NET, you need to download the relevant package from [Aspose Releases](https://releases/aspose.com/cells/net/) and add it to your .NET project.

**How to lock panes in an Excel worksheet using Aspose.Cells for .NET?**

You can use the `FreezePanes` method of the `Worksheet` object to lock the panes of a worksheet. Specify the cells to lock by providing row and column indices.

**Can I customize pane lock settings with Aspose.Cells for .NET?**

Yes, using the `FreezePanes` method, you can specify which cells to lock as needed, providing the appropriate row and column indices.

