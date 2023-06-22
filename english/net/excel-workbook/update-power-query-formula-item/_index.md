---
title: Update Power Query Formula Item
linktitle: Update Power Query Formula Item
second_title: Aspose.Cells for .NET API Reference
description: Learn how to update Power Query formula elements in Excel files using Aspose.Cells for .NET.
type: docs
weight: 160
url: /net/excel-workbook/update-power-query-formula-item/
---
Updating a Power Query formula item is a common operation when working with data in Excel files. With Aspose.Cells for .NET, you can easily update a Power Query formula item by following these steps:

## Step 1: Specify source and output directories

First, you need to specify the source directory where the Excel file containing the Power Query formulas to update is located, as well as the output directory where you want to save the modified file. Here's how to do it using Aspose.Cells:

```csharp
// source directory
string SourceDir = RunExamples.Get_SourceDirectory();

// Output directory
string outputDir = RunExamples.Get_OutputDirectory();
```

## Step 2: Load the source Excel workbook

Next, you need to load the source Excel workbook on which you want to update the Power Query formula item. Here's how to do it:

```csharp
// Load the source Excel workbook
Workbook workbook = new Workbook(SourceDir + "SamplePowerQueryFormula.xlsx");
```

## Step 3: Browse and Update Power Query Formula Items

After loading the workbook, you can navigate to the Power Query formula collection and browse through each formula and its elements. In this example, we are looking for the formula item with the name "Source" and updating its value. Here is sample code to update a Power Query formula item:

```csharp
// Access the Power Query formula collection
DataMashup mashupData = workbook.DataMashup;

// Loop through Power Query formulas and their elements
foreach(PowerQueryFormula formula in mashupData.PowerQueryFormulas)
{
     foreach(PowerQueryFormulaItem item in formula.PowerQueryFormulaItems)
     {
         if (item.Name == "Source")
         {
             item.Value = "Excel.Workbook(File.Contents(\"" + SourceDir + "SamplePowerQueryFormulaSource.xlsx\"), null, true)";
         }
     }
}
```

## Step 4: Save the output Excel workbook

Once you have updated the Power Query formula item, you can save the modified Excel workbook to the specified output directory. Here's how to do it:

```csharp
// Save the output Excel workbook
workbook.Save(outputDir + "SamplePowerQueryFormula_out.xlsx");
Console.WriteLine("UpdatePowerQueryFormulaItem executed successfully.\r\n");
```

### Sample source code for Update Power Query Formula Item using Aspose.Cells for .NET 
```csharp
// Working directories
string SourceDir = RunExamples.Get_SourceDirectory();
string outputDir = RunExamples.Get_OutputDirectory();
Workbook workbook = new Workbook(SourceDir + "SamplePowerQueryFormula.xlsx");
DataMashup mashupData = workbook.DataMashup;
foreach (PowerQueryFormula formula in mashupData.PowerQueryFormulas)
{
	foreach (PowerQueryFormulaItem item in formula.PowerQueryFormulaItems)
	{
		if (item.Name == "Source")
		{
			item.Value = "Excel.Workbook(File.Contents(\"" + SourceDir + "SamplePowerQueryFormulaSource.xlsx\"), null, true)";
		}
	}
}
// Save the output workbook.
workbook.Save(outputDir + "SamplePowerQueryFormula_out.xlsx");
Console.WriteLine("UpdatePowerQueryFormulaItem executed successfully.");
```

## Conclusion

Updating Power Query formula elements is an essential operation when using Aspose.Cells to manipulate and process data in Excel files. By following the steps given above, you can easily update formula elements

### FAQs

#### Q: What is Power Query in Excel?
     
	 A: Power Query is a feature in Excel that helps collect, transform, and load data from different sources. It offers powerful tools to clean, combine and reshape data before importing it into Excel.

#### Q: How do I know if a Power Query formula item was updated successfully?
    A: After running the Power Query Formula Item Update, you can check if the operation was successful by viewing the output and ensuring that the output Excel file was created correctly.

#### Q: Can I update multiple Power Query formula items at once?
    
	 A: Yes, you can loop through the Power Query formula item collection and update multiple items in a single loop, depending on your specific needs.

#### Q: Are there other operations I can perform on Power Query formulas with Aspose.Cells?
    
	 A: Yes, Aspose.Cells offers a full range of features for working with Power Query formulas, including creating, deleting, copying and searching formulas in an Excel workbook.
