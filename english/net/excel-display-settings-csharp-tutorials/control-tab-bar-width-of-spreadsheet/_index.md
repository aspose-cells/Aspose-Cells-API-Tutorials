---
title: Control Tab Bar Width Of Spreadsheet
linktitle: Control Tab Bar Width Of Spreadsheet
second_title: Aspose.Cells for .NET API Reference
description: Control the tab bar width of an Excel spreadsheet with Aspose.Cells for .NET.
type: docs
weight: 10
url: /net/excel-display-settings-csharp-tutorials/control-tab-bar-width-of-spreadsheet/
---
In this tutorial, we will show you how to control the tab bar width of an Excel worksheet using C# source code with Aspose.Cells for .NET. Follow the steps below to get the desired result.

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

## Step 3: Hide the worksheet tabs

To hide worksheet tabs, you can use the `ShowTabs` property of the `Settings` object of the `Workbook` class. Set it to `false` to hide the tabs.

```csharp
workbook.Settings.ShowTabs = false;
```

## Step 4: Adjust Tab Bar Width

To adjust the width of the worksheet tab bar, you can use the `SheetTabBarWidth` property of the `Settings` object of the `Workbook` class. Set it to the desired value (in points) to set the width.

```csharp
workbook.Settings.SheetTabBarWidth = 800;
```

## Step 5: Save Changes

Once you have made the necessary changes, save the modified Excel file using the `Save` method of the `Workbook` object.

```csharp
workbook.Save(dataDir + "output.xls");
```

### Sample source code for Control Tab Bar Width Of Spreadsheet using Aspose.Cells for .NET 
```csharp
// The path to the documents directory.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Instantiating a Workbook object
// Opening the Excel file
Workbook workbook = new Workbook(dataDir + "book1.xls");
// Hiding the tabs of the Excel file
workbook.Settings.ShowTabs = true;
// Adjusting the sheet tab bar width
workbook.Settings.SheetTabBarWidth = 800;
// Saving the modified Excel file
workbook.Save(dataDir + "output.xls");
```

## Conclusion

This step-by-step guide showed you how to control the tab bar width of an Excel worksheet using Aspose.Cells for .NET. Using the provided C# source code, you can easily customize the tab bar width in your Excel files.

## Frequently Asked Questions (FAQ)

**What is Aspose.Cells for .NET?**

Aspose.Cells for .NET is a powerful library for manipulating Excel files in .NET applications.

**How can I install Aspose.Cells for .NET?**

To install Aspose.Cells for .NET, you need to download the relevant package from [Aspose Releases](https://releases/aspose.com/cells/net/) and add it to your .NET project.

**What features does Aspose.Cells for .NET offer?**

Aspose.Cells for .NET offers many features, such as creating, modifying, converting and manipulating Excel files.

**How to hide tabs in Excel spreadsheet with Aspose.Cells for .NET?**

You can hide the tabs of a worksheet by using the `ShowTabs` property of the `Settings` object of the `Workbook` class and setting it to `false`.

**How to adjust tab bar width with Aspose.Cells for .NET?**

You can adjust the width of the tab bar by using the `SheetTabBarWidth` property of the `Settings` object of the `Workbook` class and assigning it a numerical value in points.
