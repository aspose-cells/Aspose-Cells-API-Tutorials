---
title: Get Odata Details
linktitle: Get Odata Details
second_title: Aspose.Cells for .NET API Reference
description: Learn how to retrieve OData details from an Excel workbook using Aspose.Cells for .NET.
type: docs
weight: 110
url: /net/excel-workbook/get-odata-details/
---
The use of OData is common when it comes to retrieving structured data from external data sources. With Aspose.Cells for .NET, you can easily retrieve OData details from an Excel workbook. Follow the steps below to get the desired results:

## Step 1: Specify source directory

First, you need to specify the source directory where the Excel file containing the OData details is located. Here's how to do it using Aspose.Cells:

```csharp
// source directory
string SourceDir = RunExamples.Get_SourceDirectory();
```

## Step 2: Load the workbook

Once the source directory is specified, you can load the Excel workbook from the file. Here is a sample code:

```csharp
// Load the workbook
Workbook workbook = new Workbook(SourceDir + "ODataSample.xlsx");
```

## Step 3: Get the OData details

After loading the workbook, you can access the OData details using the PowerQueryFormulas collection. Here's how:

```csharp
// Retrieve the collection of Power Query formulas
PowerQueryFormulaCollction PQFcoll = workbook.DataMashup.PowerQueryFormulas;

// Walk through each Power Query formula
foreach(PowerQueryFormula PQF in PQFcoll)
{
Console.WriteLine("Connection name: " + PQF.Name);

// Retrieve the collection of Power Query formula elements
PowerQueryFormulaItemCollection PQFIcoll = PQF.PowerQueryFormulaItems;

// Iterate through each Power Query formula element
foreach (PowerQueryFormulaItem PQFI in PQFIcoll)
{
Console.WriteLine("Name: " + PQFI.Name);
Console.WriteLine("Value: " + PQFI.Value);
}
}

Console.WriteLine("GetOdataDetails executed successfully.");
```

### Sample source code for Get Odata Details using Aspose.Cells for .NET 
```csharp
// source directory
string SourceDir = RunExamples.Get_SourceDirectory();
Workbook workbook = new Workbook(SourceDir + "ODataSample.xlsx");
PowerQueryFormulaCollction PQFcoll = workbook.DataMashup.PowerQueryFormulas;
foreach (PowerQueryFormula PQF in PQFcoll)
{
	Console.WriteLine("Connection Name: " + PQF.Name);
	PowerQueryFormulaItemCollection PQFIcoll = PQF.PowerQueryFormulaItems;
	foreach (PowerQueryFormulaItem PQFI in PQFIcoll)
	{
		Console.WriteLine("Name: " + PQFI.Name);
		Console.WriteLine("Value: " + PQFI.Value);
	}
}
Console.WriteLine("GetOdataDetails executed successfully.");
```

## Conclusion

Retrieving OData details from an Excel workbook is now easy with Aspose.Cells for .NET. By following the steps outlined in this guide, you will be able to access and process OData data efficiently. Experiment with your own Excel files containing OData details and get the most out of this powerful feature.

### FAQs

#### Q: Does Aspose.Cells support other data sources besides OData?
    
A: Yes, Aspose.Cells supports multiple data sources such as SQL databases, CSV files, web services, etc.

#### Q: How can I use retrieved OData details in my application?
    
A: Once you have retrieved the OData details using Aspose.Cells, you can use them for data analysis, report generation or any other manipulation in your application.

#### Q: Can I filter or sort OData data when retrieving with Aspose.Cells?
    
A: Yes, Aspose.Cells offers advanced functionality to filter, sort and manipulate OData data to meet your specific needs.

#### Q: Can I automate the process of retrieving OData details with Aspose.Cells?
    
A: Yes, you can automate the process of retrieving OData details by integrating Aspose.Cells into your workflows or by using programming scripts.
