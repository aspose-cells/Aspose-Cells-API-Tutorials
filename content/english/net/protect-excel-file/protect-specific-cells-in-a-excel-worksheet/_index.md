---
title: Protect Specific Cells In A Excel Worksheet
linktitle: Protect Specific Cells In A Excel Worksheet
second_title: Aspose.Cells for .NET API Reference
description: Learn how to protect specific cells in Excel with Aspose.Cells for .NET. Step by step tutorial in C#.
type: docs
weight: 70
url: /net/protect-excel-file/protect-specific-cells-in-a-excel-worksheet/
---
In this tutorial, we'll look at C# source code that uses the Aspose.Cells library to protect specific cells in an Excel spreadsheet. We'll walk through each step of the code and explain how it works. Follow the instructions carefully to get the desired results.

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

In this step, we will define the style to apply to specific cells. Use the following code:

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

## Step 7: Locking Specific Cells

In this step, we will lock specific cells. Use the following code:

```csharp
// Locking all three cells... i.e. A1, B1, C1.
style = sheet.Cells["A1"].GetStyle();
style. IsLocked = true;
sheet.Cells["A1"].SetStyle(style);

style = sheet.Cells["B1"].GetStyle();
style. IsLocked = true;
sheet.Cells["B1"].SetStyle(style);

style = sheet.Cells["C1"].GetStyle();
style. IsLocked = true;
sheet.Cells["C1"].SetStyle(style);
```

## Step 8: Protecting the worksheet

Finally, we will protect the worksheet to prevent specific cells from being modified. Use the following code:

```csharp
// Protect the worksheet.
sheet.Protect(ProtectionType.All);
```

## Step 9: Saving the Excel file

We will now save the modified Excel file. Use the following code:

```csharp
// Save the Excel file.
wb.Save(dataDir + "output.out.xls", SaveFormat.Excel97To2003);
```

Make sure to specify the correct path to save the modified Excel file.

### Sample source code for Protect Specific Cells In A Excel Worksheet using Aspose.Cells for .NET 
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
// Define the styleflag object
StyleFlag styleflag;
// Loop through all the columns in the worksheet and unlock them.
for (int i = 0; i <= 255; i++)
{
    style = sheet.Cells.Columns[(byte)i].Style;
    style.IsLocked = false;
    styleflag = new StyleFlag();
    styleflag.Locked = true;
    sheet.Cells.Columns[(byte)i].ApplyStyle(style, styleflag);
}
// Lock the three cells...i.e. A1, B1, C1.
style = sheet.Cells["A1"].GetStyle();
style.IsLocked = true;
sheet.Cells["A1"].SetStyle(style);
style = sheet.Cells["B1"].GetStyle();
style.IsLocked = true;
sheet.Cells["B1"].SetStyle(style);
style = sheet.Cells["C1"].GetStyle();
style.IsLocked = true;
sheet.Cells["C1"].SetStyle(style);
// Finally, Protect the sheet now.
sheet.Protect(ProtectionType.All);
// Save the excel file.
wb.Save(dataDir + "output.out.xls", SaveFormat.Excel97To2003);
```


## Conclusion

Congratulation ! You now have C# source code that allows you to protect specific cells in an Excel worksheet using the Aspose.Cells library for .NET. Feel free to customize the code to suit your specific needs.

### FAQs (Frequently Asked Questions)

#### Does this code work with recent versions of Excel?

Yes, this code works with recent versions of Excel, including files in Excel 2010 and above format.

#### Can I protect other cells besides A1, B1 and C1?

Yes, you can modify the code to lock other specific cells by adjusting the cell references in the corresponding lines of code.

#### How can I unlock locked cells again?

You can use `SetStyle` method with `IsLocked` set to `false` to unlock cells.

#### Can I add more worksheets to the workbook?

Yes, you can add other worksheets to the workbook using the `Worksheets.Add()` method and repeat the cell protection steps for each worksheet.

#### How can I change the save format of the Excel file?

You can change the save format using the `SaveFormat` method with the desired format, for example `SaveFormat.Xlsx` for Excel 2007 and later.