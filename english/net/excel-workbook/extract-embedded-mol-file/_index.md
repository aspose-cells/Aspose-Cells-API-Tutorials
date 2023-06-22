---
title: Extract Embedded Mol File
linktitle: Extract Embedded Mol File
second_title: Aspose.Cells for .NET API Reference
description: Learn how to easily extract embedded MOL files from an Excel workbook using Aspose.Cells for .NET.
type: docs
weight: 90
url: /net/excel-workbook/extract-embedded-mol-file/
---
In this tutorial, we will walk you through step-by-step how to extract an embedded MOL file from an Excel workbook using the Aspose.Cells library for .NET. You will learn how to browse the workbook sheets, extract the corresponding OLE objects and save the extracted MOL files. Follow the steps below to complete this task successfully.

## Step 1: Define source and output directories
First, we need to define the source and output directories in our code. These directories indicate where the source Excel workbook is located and where the extracted MOL files will be saved. Here is the corresponding code:

```csharp
// Directories
string SourceDir = RunExamples.Get_SourceDirectory();
string outputDir = RunExamples.Get_OutputDirectory();
```

Be sure to specify the appropriate paths as needed.

## Step 2: Loading the Excel workbook
The next step is to load the Excel workbook containing the embedded OLE objects and MOL files. Here is the code to load the workbook:

```csharp
Workbook workbook = new Workbook(SourceDir + "EmbeddedMolSample.xlsx");
```

Make sure to specify the source file name correctly in the code.

## Step 3: Traverse the sheets and extract the MOL files
Now we will loop through each sheet in the workbook and extract the corresponding OLE objects, which contain the MOL files. Here is the corresponding code:

```csharp
var index = 1;
foreach(Worksheet sheet in workbook.Worksheets)
{
     OleObjectCollection oles = sheet.OleObjects;
     foreach(OleObject ole in oles)
     {
         string fileName = outputDir + "OleObject" + index + ".mol";
         FileStream fs = File.Create(fileName);
         fs.Write(ole.ObjectData, 0, ole.ObjectData.Length);
         fs. Close();
         index++;
     }
}
Console.WriteLine("ExtractEmbeddedMolFile executed successfully.");
```

This code loops through each sheet in the workbook, fetches the OLE objects, and saves the extracted MOL files to the output directory.

### Sample source code for Extract Embedded Mol File using Aspose.Cells for .NET 
```csharp
//directories
string SourceDir = RunExamples.Get_SourceDirectory();
string outputDir = RunExamples.Get_OutputDirectory();
Workbook workbook = new Workbook(SourceDir + "EmbeddedMolSample.xlsx");
var index = 1;
foreach (Worksheet sheet in workbook.Worksheets)
{
	OleObjectCollection oles = sheet.OleObjects;
	foreach (OleObject ole in oles)
	{
		string fileName = outputDir + "OleObject" + index + ".mol ";
		FileStream fs = File.Create(fileName);
		fs.Write(ole.ObjectData, 0, ole.ObjectData.Length);
		fs.Close();
		index++;
	}
}
Console.WriteLine("ExtractEmbeddedMolFile executed successfully.");
```

## Conclusion
Congratulation ! You have learned how to extract an embedded MOL file from an Excel workbook using Aspose.Cells for .NET. You can now apply this knowledge to extract MOL files from your own Excel workbooks. Feel free to explore the Aspose.Cells library further and learn about its other powerful features.

### FAQs

#### Q: What is a MOL file?
 
	 A: A MOL file is a file format used to represent chemical structures in computational chemistry. It contains information about atoms, bonds and other molecular properties.

#### Q: Does this method work with all Excel file types?

	 A: Yes, this method works with all Excel file types supported by Aspose.Cells.

#### Q: Can I extract multiple MOL files at once?

	 A: Yes, you can extract multiple MOL files at once by iterating through OLE objects on each sheet in the workbook.
