---
title: Set Excel Headers And Footers
linktitle: Set Excel Headers And Footers
second_title: Aspose.Cells for .NET API Reference
description: Learn how to set headers and footers in Excel using Aspose.Cells for .NET. 
type: docs
weight: 100
url: /net/excel-page-setup/set-excel-headers-and-footers/
---

In this tutorial, we are going to show you step by step how to set headers and footers in Excel using Aspose.Cells for .NET. We will use C# source code to illustrate the process.

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
Workbook excel = new Workbook();
PageSetup pageSetup = excel.Worksheets[0].PageSetup;
```

This will create an empty workbook with a worksheet and provide access to that worksheet's PageSetup object.

## Step 5: Setting Headers

Set the spreadsheet headers using the `SetHeader` methods of the PageSetup object. Here is a sample code:

```csharp
pageSetup.SetHeader(0, "&A");
pageSetup.SetHeader(1, "&\"Times New Roman,Bold\"&D-&T");
pageSetup.SetHeader(2, "&\"Times New Roman,Bold\"&12&F");
```

This will set the worksheet name, current date and time, and file name in the headers respectively.

## Step 6: Defining footers

Set spreadsheet footers using the `SetFooter` methods of the PageSetup object. Here is a sample code:

```csharp
pageSetup.SetFooter(0, "Hello World! &\"Courier New\"&14 123");
pageSetup.SetFooter(1, "&P");
pageSetup.SetFooter(2, "&N");
```

This will respectively set a text string, the current page number and the total number of pages in the footers.

## Step 7: Saving the Modified Workbook

Save the modified workbook using the following code:

```csharp
excel.Save(dataDir + "OutputFileName.xls");
```

This will save the modified workbook to the specified data directory.

### Sample source code for Set Excel Headers And Footers using Aspose.Cells for .NET 
```csharp
// The path to the documents directory.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Instantiating a Workbook object
Workbook excel = new Workbook();
// Obtaining the reference of the PageSetup of the worksheet
PageSetup pageSetup = excel.Worksheets[0].PageSetup;
// Setting worksheet name at the left section of the header
pageSetup.SetHeader(0, "&A");
// Setting current date and current time at the centeral section of the header
// and changing the font of the header
pageSetup.SetHeader(1, "&\"Times New Roman,Bold\"&D-&T");
// Setting current file name at the right section of the header and changing the
// font of the header
pageSetup.SetHeader(2, "&\"Times New Roman,Bold\"&12&F");
// Setting a string at the left section of the footer and changing the font
// of a part of this string ("123")
pageSetup.SetFooter(0, "Hello World! &\"Courier New\"&14 123");
// Setting the current page number at the central section of the footer
pageSetup.SetFooter(1, "&P");
// Setting page count at the right section of footer
pageSetup.SetFooter(2, "&N");
// Save the Workbook.
excel.Save(dataDir + "SetHeadersAndFooters_out.xls");
```


## Conclusion

You have now learned how to set headers and footers in Excel using Aspose.Cells for .NET. This tutorial walked you through every step of the process, from setting up the environment to saving the modified workbook. Feel free to further explore the features of Aspose.Cells to perform further manipulations in your Excel files.

### Frequently Asked Questions (FAQ)

#### 1. How can I install Aspose.Cells for .NET on my system?
To install Aspose.Cells for .NET, you need to download the installation package from Aspose official website and follow the instructions provided in the documentation.

#### 2. Does this method work with all versions of Excel?
Yes, the method of setting headers and footers with Aspose.Cells for .NET works with all supported versions of Excel.

#### 3. Can I further customize headers and footers?
Yes, Aspose.Cells offers an extensive range of features to customize headers and footers, including text placement, color, font, page numbers and more.

#### 4. How can I add dynamic information to headers and footers?
You can use special variables and formatting codes to add dynamic information such as current date, time, file name, page number, etc., to headers and footers.

#### 5. Can I remove headers and footers after setting them?
Yes, you can remove headers and footers using the `ClearHeaderFooter` method of the `PageSetup` object. This will restore the default headers and footers.
