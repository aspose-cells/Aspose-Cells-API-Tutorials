---
title: Allow Leading Apostrophe
linktitle: Allow Leading Apostrophe
second_title: Aspose.Cells for .NET API Reference
description: Allow leading apostrophe in Excel workbooks with Aspose.Cells for .NET.
type: docs
weight: 60
url: /net/excel-workbook/allow-leading-apostrophe/
---
In this step-by-step tutorial, we will explain the provided C# source code that will allow you to allow the use of a leading apostrophe in an Excel workbook using Aspose.Cells for .NET. Follow the steps below to perform this operation.

## Step 1: Set source and output directories

```csharp
// source directory
string sourceDir = RunExamples.Get_SourceDirectory();
// Output directory
string outputDir = RunExamples.Get_OutputDirectory();
```

In this first step, we define the source and output directories for the Excel files.

## Step 2: Instantiate a WorkbookDesigner object

```csharp
// Instantiate a WorkbookDesigner object
WorkbookDesigner designer = new WorkbookDesigner();
```

We create an instance of the `WorkbookDesigner` class from Aspose.Cells.

## Step 3: Load Excel Workbook

```csharp
// Load the Excel workbook
Workbook workbook = new Workbook(sourceDir + "AllowLeadingApostropheSample.xlsx");
workbook.Settings.QuotePrefixToStyle = false;
designer.Workbook = workbook;
```

We load the Excel workbook from the specified file and disable the automatic conversion of initial apostrophes to text style.

## Step 4: Set Data Source

```csharp
// Define the data source for the designer workbook
List<DataObject> list = new List<DataObject>
{
new DataObject
{
Id=1,
Name = "demo"
},
new DataObject
{
ID=2,
Name = "'demo"
}
};
designer.SetDataSource("sampleData", list);
```

We define a list of data objects and use the `SetDataSource` method to set the data source for the designer workbook.

## Step 5: Process smart markers

```csharp
// Process smart markers
designer. Process();
```

We use the `Process` method to process smart markers in the designer workbook.

## Step 6: Save the modified Excel workbook

```csharp
// Save the modified Excel workbook
designer.Workbook.Save(outputDir + "AllowLeadingApostropheSample_out.xlsx");
```

We save the modified Excel workbook with the changes made.

### Sample source code for Allow Leading Apostrophe using Aspose.Cells for .NET 
```csharp
//Source directory
string sourceDir = RunExamples.Get_SourceDirectory();
string outputDir = RunExamples.Get_OutputDirectory();
// Instantiating a WorkbookDesigner object
WorkbookDesigner designer = new WorkbookDesigner();
Workbook workbook = new Workbook(sourceDir + "AllowLeadingApostropheSample.xlsx");
workbook.Settings.QuotePrefixToStyle = false;
// Open a designer spreadsheet containing smart markers
designer.Workbook = workbook;
List<DataObject> list = new List<DataObject>
{
	new DataObject
	{
		 Id =1,
		 Name = "demo"
	},
	new DataObject
	{
		Id=2,
		Name = "'demo"
	}
};
// Set the data source for the designer spreadsheet
designer.SetDataSource("sampleData", list);
// Process the smart markers
designer.Process();
designer.Workbook.Save(outputDir + "AllowLeadingApostropheSample_out.xlsx");
Console.WriteLine("AllowLeadingApostrophe executed successfully.");
```

## Conclusion

Congratulation ! You learned how to allow the use of a leading apostrophe in an Excel workbook using Aspose.Cells for .NET. Experiment with your own data to further customize your Excel workbooks.

### FAQs

#### Q: What is leading apostrophe permission in an Excel workbook?

	 A: Allowing the initial apostrophe in an Excel workbook allows data that begins with an apostrophe to be displayed correctly without converting it to a text style. This is useful when you want to keep the apostrophe as part of the data.

#### Q: Why do I need to turn off automatic conversion of initial apostrophes?

	 A: By disabling the automatic conversion of leading quotes, you can preserve their use as it is in your data. This avoids any unintended modification of the data while opening or manipulating the Excel workbook.

#### Q: How to set datasource in designer workbook?

	 A: To set the data source in the designer workbook, you can use the `SetDataSource` method specifying the name of the data source and a list of corresponding data objects.

#### Q: Does allowing leading apostrophe affect other data in Excel workbook?

	 A: No, allowing the leading apostrophe only affects data beginning with an apostrophe. Other data in the Excel workbook remains unchanged.

#### Q: Can I use this feature with other Excel file formats?

	 A: Yes, you can use this feature with other Excel file formats supported by Aspose.Cells, such as .xls, .xlsm, etc.
