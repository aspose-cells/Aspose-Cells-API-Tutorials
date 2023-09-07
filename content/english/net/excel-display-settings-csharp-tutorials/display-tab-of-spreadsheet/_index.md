---
title: Display Tab Of Spreadsheet
linktitle: Display Tab Of Spreadsheet
second_title: Aspose.Cells for .NET API Reference
description: Display an Excel spreadsheet tab using Aspose.Cells for .NET.
type: docs
weight: 60
url: /net/excel-display-settings-csharp-tutorials/display-tab-of-spreadsheet/
---
In this tutorial, we will show you how to display the tab of an Excel worksheet using C# source code with Aspose.Cells for .NET. Follow the steps below to get the desired result.

## Step 1: Import the necessary libraries

Make sure you have installed the Aspose.Cells library for .NET and import the necessary libraries into your C# project.

```csharp
using Aspose.Cells;
```

## Step 2: Set directory path and open Excel file

Set the path to the directory containing your Excel file, then open the file by instantiating a `Workbook` object.

```csharp
string dataDir = "YOUR DOCUMENTS DIRECTORY";
Workbook workbook = new Workbook(dataDir + "book1.xls");
```

## Step 3: Show the worksheet tab

Use the `ShowTabs` property of the `Workbook.Settings` object to show the Excel worksheet tab.

```csharp
workbook.Settings.ShowTabs = true;
```

## Step 4: Save Changes

Once you have made the necessary changes, save the modified Excel file using the `Save` method of the `Workbook` object.

```csharp
workbook.Save(dataDir + "output.xls");
```

### Sample source code for Display Tab Of Spreadsheet using Aspose.Cells for .NET 

```csharp
// The path to the documents directory.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Instantiating a Workbook object
// Opening the Excel file
Workbook workbook = new Workbook(dataDir + "book1.xls");
// Hiding the tabs of the Excel file
workbook.Settings.ShowTabs = true;
// Saving the modified Excel file
workbook.Save(dataDir + "output.xls");
```

### Conclusion

This step-by-step guide showed you how to show the tab of an Excel spreadsheet using Aspose.Cells for .NET. Using the provided C# source code, you can easily customize the display of tabs in your Excel files.

### Frequently Asked Questions (FAQ)

#### What is Aspose.Cells for .NET?

Aspose.Cells for .NET is a powerful library for manipulating Excel files in .NET applications.

#### How can I install Aspose.Cells for .NET?

To install Aspose.Cells for .NET, you need to download the relevant package from [Aspose Releases](https://releases/aspose.com/cells/net/) and add it to your .NET project.

#### How to display the tab of an Excel spreadsheet using Aspose.Cells for .NET?

You can use the `ShowTabs` property of the `Workbook.Settings` object and set it to `true` to show the worksheet tab.

#### What other Excel file formats are supported by Aspose.Cells for .NET?

Aspose.Cells for .NET supports a variety of Excel file formats, such as XLS, XLSX, CSV, HTML, PDF, etc.

