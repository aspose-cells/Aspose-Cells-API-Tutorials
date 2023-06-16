---
title: Insert Image In Header Footer
linktitle: Insert Image In Header Footer
second_title: Aspose.Cells for .NET API Reference
description: Learn how to insert an image into the header or footer of an Excel document using Aspose.Cells for .NET. Step by step guide with source code in C#.
type: docs
weight: 60
url: /net/excel-page-setup/insert-image-in-header-footer/
---
The ability to insert an image in the header or footer of an Excel document can be very useful for customizing your reports or adding company logos. In this article, we will guide you step by step to insert an image in the header or footer of an Excel document using Aspose.Cells for .NET. You will learn how to accomplish this using C# source code.

## Step 1: Setting up the environment

Before you start, make sure you have Aspose.Cells for .NET installed on your machine. Also create a new project in your preferred development environment.

## Step 2: Import necessary libraries

In your code file, import the libraries needed to work with Aspose.Cells. Here is the corresponding code:

```csharp
using Aspose.Cells;
```

## Step 3: Set Document Directory

Set the directory where the Excel document you want to work with is located. Use the following code to set the directory:

```csharp
string dataDir = "YOUR DOCUMENTS DIRECTORY";
```

Be sure to specify the full directory path.

## Step 4: Creating a Workbook Object

The Workbook object represents the Excel document with which you will work. You can create it using the following code:

```csharp
Workbook workbook = new Workbook();
```

This creates a new empty Workbook object.

## Step 5: Storing the Image URL

Define the URL or path of the image you want to insert in the header or footer. Use the following code to store the image URL:

```csharp
string logo_url = dataDir + "aspose-logo.jpg";
```

Make sure the specified path is correct and the image exists in that location.

## Step 6: Opening the image file

To open the image file, we'll use a FileStream object and read the binary data from the image. Here is the corresponding code:

```csharp
FileStream inFile;
byte[] binaryData;

inFile = new System.IO.FileStream(logo_url, System.IO.FileMode.Open, System.IO.FileAccess.Read);
binaryData = new Byte[inFile.Length];
long bytesRead = inFile.Read(binaryData, 0, (int)inFile.Length);
```

Make sure the image path is correct and you have the correct permissions to access it.

## Step 7: Configuring the PageSetup

The PageSetup object is used to set the Excel document page settings including the header and footer. Use the following code to get the PageSetup object of the first worksheet:

```csharp
PageSetup pageSetup = workbook. Worksheets

[0].PageSetup;
```

This will allow you to access the page settings for the first worksheet in the workbook.

## Step 8: Adding the image to the header

Use the SetHeaderPicture() method of the PageSetup object to set the image in the middle section of the page header. Here is the corresponding code:

```csharp
pageSetup.SetHeaderPicture(1, binaryData);
```

This will add the specified image to the page header.

## Step 9: Adding a script to the header

To add script to the page header, use the SetHeader() method of the PageSetup object. Here is the corresponding code:

```csharp
pageSetup.SetHeader(1, "&G");
```

This will add the specified script to the page header. In this example, the "&G" script displays the page number.

## Step 10: Add Sheet Name to Header

To display the sheet name in the page header, use the SetHeader() method of the PageSetup object again. Here is the corresponding code:

```csharp
pageSetup.SetHeader(2, "&A");
```

This will add the sheet name to the page header. The "&A" script is used to represent the sheet name.

## Step 11: Saving the workbook

To save changes to the workbook, use the Save() method of the Workbook object. Here is the corresponding code:

```csharp
workbook.Save(dataDir + "InsertImageInHeaderFooter_out.xls");
```

This will save the workbook with the changes to the specified directory.

## Step 12: Closing the FileStream

After reading the binary data from the image, be sure to close the FileStream to free the resources. Use the following code to close the FileStream:

```csharp
inFile.Close();
```

Be sure to always close FileStreams when you're done using them.

### Sample source code for Insert Image In Header Footer using Aspose.Cells for .NET 
```csharp
// The path to the documents directory.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Creating a Workbook object
Workbook workbook = new Workbook();
// Creating a string variable to store the url of the logo/picture
string logo_url = dataDir + "aspose-logo.jpg";
// Declaring a FileStream object
FileStream inFile;
// Declaring a byte array
byte[] binaryData;
// Creating the instance of the FileStream object to open the logo/picture in the stream
inFile = new System.IO.FileStream(logo_url, System.IO.FileMode.Open, System.IO.FileAccess.Read);
// Instantiating the byte array of FileStream object's size
binaryData = new Byte[inFile.Length];
// Reads a block of bytes from the stream and writes data in a given buffer of byte array.
long bytesRead = inFile.Read(binaryData, 0, (int)inFile.Length);
// Creating a PageSetup object to get the page settings of the first worksheet of the workbook
PageSetup pageSetup = workbook.Worksheets[0].PageSetup;
// Setting the logo/picture in the central section of the page header
pageSetup.SetHeaderPicture(1, binaryData);
// Setting the script for the logo/picture
pageSetup.SetHeader(1, "&G");
// Setting the Sheet's name in the right section of the page header with the script
pageSetup.SetHeader(2, "&A");
// Saving the workbook
workbook.Save(dataDir + "InsertImageInHeaderFooter_out.xls");
//Closing the FileStream object
inFile.Close();       
```
## Conclusion

Congratulation ! You now know how to insert an image in the header or footer of an Excel document using Aspose.Cells for .NET. This tutorial walked you through every step of the process, from setting up the environment to saving the modified workbook. Feel free to experiment more with the features of Aspose.Cells to create personalized and professional Excel documents.

### FAQ's

#### Q1: Is it possible to insert multiple images in the header or footer of an Excel document?

A1: Yes, you can insert multiple images into the header or footer of an Excel document by repeating steps 8 and 9 for each additional image.

#### Q2: What image formats are supported for insertion in header or footer?
A2: Aspose.Cells supports a variety of common image formats such as JPEG, PNG, GIF, BMP, etc.

#### Q3: Can I further customize the appearance of the header or footer?

A3: Yes, you can use special scripts and codes to further format and customize the appearance of the header or footer. Refer to the Aspose.Cells documentation for more information on customization options.

#### Q4: Does Aspose.Cells work with different versions of Excel?

A4: Yes, Aspose.Cells is compatible with different versions of Excel including Excel 2003, Excel 2007, Excel 2010, Excel 2013, Excel 2016 and Excel 2019.

#### Q5: Is it possible to insert images in other parts of the Excel document, such as cells or charts?

A5: Yes, Aspose.Cells provides extensive functionality for inserting images into different parts of the Excel document, including cells, charts and drawing objects.