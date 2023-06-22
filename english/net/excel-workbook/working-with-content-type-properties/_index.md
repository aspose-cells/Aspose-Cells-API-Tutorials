---
title: Working With Content Type Properties
linktitle: Working With Content Type Properties
second_title: Aspose.Cells for .NET API Reference
description: Learn how to work with content type properties using Aspose.Cells for .NET.
type: docs
weight: 180
url: /net/excel-workbook/working-with-content-type-properties/
---
Content type properties play a vital role in managing and manipulating Excel files using the Aspose.Cells library for .NET. These properties allow you to define additional metadata for Excel files, making it easier to organize and find data. In this tutorial, we'll take you step-by-step to understand and work with content type properties using sample C# code.

## Prerequisites

Before you begin, make sure you have the following:

- Aspose.Cells for .NET installed on your development machine.
- An integrated development environment (IDE) compatible with C#, such as Visual Studio.

## Step 1: Setting up the environment

Before you start working with content type properties, make sure you have set up your development environment with Aspose.Cells for .NET. You can add the reference to the Aspose.Cells library in your project and import the required namespace into your class.

```csharp
using Aspose.Cells;
```

## Step 2: Creating a new Excel workbook

First, we'll create a new Excel workbook using the `Workbook` class provided by Aspose.Cells. The following code shows how to create a new Excel workbook and store it in a specified output directory.

```csharp
// Destination directory
string outputDir = RunExamples.Get_OutputDirectory();

// Create a new Excel workbook
Workbook workbook = new Workbook(FileFormatType.Xlsx);
```

## Step 3: Adding Content Type Properties

Now that we have our Excel workbook, we can add content type properties using the `Add` method of the `ContentTypeProperties` collection of the `Workbook` class. Each property is represented by a name and a value. YOU

  You can also specify the data type of the property.

```csharp
// Add the first content type property
int index = workbook.ContentTypeProperties.Add("MK31", "Simple Data");
workbook.ContentTypeProperties[index].IsNillable = false;

// Add the second content type property
index = workbook.ContentTypeProperties.Add("MK32", DateTime.Now.ToString("yyyy-MM-dd'T'hh:mm:ss"), "DateTime");
workbook.ContentTypeProperties[index].IsNillable = true;
```

## Step 4: Saving the Excel workbook

After adding the content type properties, we can save the Excel workbook with the changes. Use the `Save` method of the `Workbook` class to specify the output directory and file name.

```csharp
// Save the Excel workbook
workbook.Save(outputDir + "WorkingWithContentTypeProperties_out.xlsx");
```

### Sample source code for Working With Content Type Properties using Aspose.Cells for .NET 
```csharp
//source directory
string outputDir = RunExamples.Get_OutputDirectory();
Workbook workbook = new Workbook(FileFormatType.Xlsx);
int index = workbook.ContentTypeProperties.Add("MK31", "Simple Data");
workbook.ContentTypeProperties[index].IsNillable = false;
index = workbook.ContentTypeProperties.Add("MK32", DateTime.Now.ToString("yyyy-MM-dd'T'hh:mm:ss"), "DateTime");
workbook.ContentTypeProperties[index].IsNillable = true;
workbook.Save(outputDir + "WorkingWithContentTypeProperties_out.xlsx");
Console.WriteLine("WorkingWithContentTypeProperties executed successfully.");
```

## Conclusion

Congratulation ! You learned how to work with content type properties using Aspose.Cells for .NET. Now you can add custom metadata to your Excel files and manage them more efficiently.

### FAQs

#### Q: Are content type properties compatible with all versions of Excel?

	 A: Yes, content type properties are compatible with Excel files created in all versions of Excel.

#### Q: Can I edit content type properties after adding them to the Excel workbook?

	 A: Yes, you can change the content type properties at any time by going to the `ContentTypeProperties` collection of the `Workbook` class and using the and p methodsappropriate properties.

#### Q: Are content type properties supported when saving to PDF?

	 A: No, content type properties are not supported when saving to PDF. They are specific to Excel files.
