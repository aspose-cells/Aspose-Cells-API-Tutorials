---
title: Set Excel First Page Number
linktitle: Set Excel First Page Number
second_title: Aspose.Cells for .NET API Reference
description: Learn how to set the first page number in Excel using Aspose.Cells for .NET. 
type: docs
weight: 90
url: /net/excel-page-setup/set-excel-first-page-number/
---
In this tutorial, we will walk you through how to set the first page number in Excel using Aspose.Cells for .NET. We will use C# source code to illustrate the process.

## Step 1: Setting up the environment

Make sure you have Aspose.Cells for .NET installed on your machine. Also create a new project in your preferred development environment.

## Step 2: Import necessary libraries

In your code file, import the libraries needed to work with Aspose.Cells. Here is the corresponding code:

```csharp
using Aspose.Cells;
```

## Step 3: Set Data Directory

Set the data directory where you want to save the modified Excel file. Use the following code:

```csharp
string dataDir = "YOUR DATA DIRECTORY";
```

Be sure to specify the full directory path.

## Step 4: Creating the workbook and worksheet

Create a new Workbook object and navigate to the first worksheet in the workbook using the following code:

```csharp
Workbook workbook = new Workbook();
Worksheet worksheet = workbook.Worksheets[0];
```

This will create an empty workbook with a worksheet.

## Step 5: Setting the number of the first page

Set the number of the first page of the worksheet pages using the following code:

```csharp
worksheet.PageSetup.FirstPageNumber = 2;
```

This will set the first page number to 2.

## Step 6: Saving the Modified Workbook

Save the modified workbook using the following code:

```csharp
workbook.Save(dataDir + "OutputFileName.xls");
```

This will save the modified workbook to the specified data directory.

### Sample source code for Set Excel First Page Number using Aspose.Cells for .NET 
```csharp
// The path to the documents directory.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Instantiating a Workbook object
Workbook workbook = new Workbook();
// Accessing the first worksheet in the Excel file
Worksheet worksheet = workbook.Worksheets[0];
// Setting the first page number of the worksheet pages
worksheet.PageSetup.FirstPageNumber = 2;
// Save the Workbook.
workbook.Save(dataDir + "SetFirstPageNumber_out.xls");
```

## Conclusion

You have now learned how to set the first page number in Excel using Aspose.Cells for .NET. This tutorial walked you through every step of the process, from setting up the environment to setting the first page number. You can now use this knowledge to customize the page numbering in your Excel files.

## FAQ's

**Q1: Can I set a different first page number for each worksheet?**

A1: Yes, you can set a different first page number for each worksheet by accessing the `FirstPageNumber` property of the respective worksheet's `PageSetup` object.

**Q2: How can I check the first page number of an existing spreadsheet?**

A2: You can check the first page number of an existing worksheet by accessing the `FirstPageNumber` property of the `PageSetup` object corresponding to that worksheet.

**Q3: Does page numbering always start from 1 by default?**

A3: Yes, page numbering starts from 1 by default in Excel. However, you can use the code shown in this tutorial to set a different first page number.

**Q4: Are changes to the first page number permanent in the edited Excel file?**

A4: Yes, the changes made to the first page number are permanently saved in the modified Excel file.

**Q5: Does this method work for all Excel file formats, such as .xls and .xlsx?**

A5: Yes, this method works for all Excel file formats supported by Aspose.Cells, including .xls and .xlsx.