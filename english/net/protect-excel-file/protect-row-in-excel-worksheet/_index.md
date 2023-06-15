---
title: Protect Row In Excel Worksheet
linktitle: Protect Row In Excel Worksheet
second_title: Aspose.Cells for .NET API Reference
description: Discover in this tutorial how to protect the rows of an Excel spreadsheet using Aspose.Cells for .NET. Step by step tutorial in C#.
type: docs
weight: 60
url: /net/protect-excel-file/protect-row-in-excel-worksheet/
---
In this tutorial, we'll look at some C# source code that uses the Aspose.Cells library to protect rows in an Excel spreadsheet. We'll walk through each step of the code and explain how it works. Follow the instructions carefully to get the desired results.

## Step 1: Prerequisites

Before you start, make sure you have installed the Aspose.Cells library for .NET. You can get it from Aspose official website. Also make sure you have a recent version of Visual Studio or any other C# development environment.

## Step 2: Import required namespaces

To use the Aspose.Cells library, we need to import the necessary namespaces into our code. Add the following lines to the top of your C# source file:

```csharp
using Aspose.Cells;
```

## Step 3: Creating an Excel workbook

In this step, we will create a new Excel workbook. Use the following code to create an Excel workbook:

```csharp
// Path to the documents directory.
string dataDir = "YOUR_DIRECTORY_OF_DOCUMENTS";

// Create a new workbook.
Workbook wb = new Workbook();
```

Be sure to replace `"YOUR_DOCUMENTS_DIR"` with the appropriate path to your documents directory.

## Step 4: Creating a spreadsheet

Now that we have created the Excel workbook, let's create a worksheet and get the first sheet. Use the following code:

```csharp
// Create a spreadsheet object and get the first sheet.
Worksheet sheet = wb.Worksheets[0];
```

## Step 5: Defining the Style

In this step, we will define the style to apply to the rows of the spreadsheet. Use the following code:

```csharp
// Definition of the style object.
Styling styling;
```

## Step 6: Loop to unlock all columns

Now we will loop through all the columns in the worksheet and unlock them. Use the following code:

```csharp
// Loop through all the columns in the worksheet and unlock them.
for (int i = 0; i <= 255; i++)
{
     style = sheet.Cells.Columns[(byte)i].Style;
     style. IsLocked = false;
     sheet.Cells.Columns[(byte)i].ApplyStyle(style);
}
```

## Step 7: Locking the first line

In this step, we will lock the first row of the worksheet. Use the following code:

```csharp
// Get the style of the first line.
style = sheet.Cells.Rows[0].Style;
// Lock the style.
style. IsLocked = true;
// Apply the style to the first line.
sheet.Cells.ApplyRowStyle(0, style);
```

## Step 8: Protecting the worksheet

Now that we've set the styles and locked the rows, let's protect the spreadsheet. Use the following code:

```csharp
// Protect the worksheet.
sheet.Protect(ProtectionType.All);
```

## Step 9: Saving the Excel file

Finally, we will save the modified Excel file. Use the following code:

```csharp
// Save the Excel file.
wb.Save(dataDir + "output.out.xls", SaveFormat.Excel97To2003);
```

Make sure to specify the correct path to save the modified Excel file.

### Sample source code for Protect Row In Excel Worksheet using Aspose.Cells for .NET 
```csharp
// The path to the documents directory.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Create directory if it is not already present.
bool IsExists = System.IO.Directory.Exists(dataDir);
if (!IsExists)
    System.IO.Directory.CreateDirectory(dataDir);
// Create a new workbook.
Workbook wb = new Workbook();
// Create a worksheet object and obtain the first sheet.
Worksheet sheet = wb.Worksheets[0];
// Define the style object.
Style style;
// Define the styleflag object.
StyleFlag flag;
// Loop through all the columns in the worksheet and unlock them.
for (int i = 0; i <= 255; i++)
{
    style = sheet.Cells.Columns[(byte)i].Style;
    style.IsLocked = false;
    flag = new StyleFlag();
    flag.Locked = true;
    sheet.Cells.Columns[(byte)i].ApplyStyle(style, flag);
}
// Get the first row style.
style = sheet.Cells.Rows[0].Style;
// Lock it.
style.IsLocked = true;
// Instantiate the flag.
flag = new StyleFlag();
// Set the lock setting.
flag.Locked = true;
// Apply the style to the first row.
sheet.Cells.ApplyRowStyle(0, style, flag);
// Protect the sheet.
sheet.Protect(ProtectionType.All);
// Save the excel file.
wb.Save(dataDir + "output.out.xls", SaveFormat.Excel97To2003);
```

## Conclusion

Congratulation ! You now have C# source code that allows you to protect rows in an Excel spreadsheet using the Aspose.Cells library for .NET. Be sure to follow the steps carefully and customize the code to your specific needs.

## FAQs (Frequently Asked Questions)

1. Does this code work with recent versions of Excel?
    A: Yes, this code works with recent versions of Excel, including files in Excel 2010 and above format.

2. Can I protect only specific rows instead of all rows in the worksheet?
    A: Yes, you can modify the code to specify the specific rows you want to protect. You will need to adjust the loop and indices accordingly.

3. How can I unlock locked lines again?
    A: You can use the `IsLocked` method of the `Style` object to set the value to `false` and unlock the rows.

4. Is it possible to protect multiple worksheets in the same Excel workbook?
    A: Yes, you can repeat the steps of creating a worksheet, setting the style and protecting for each worksheet in the workbook.

5. How can I change the spreadsheet protection password?
    A: You can change the password using the `Protect` method and specifying a new password as an argument.