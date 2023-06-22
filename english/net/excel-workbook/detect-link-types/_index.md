---
title: Detect Link Types
linktitle: Detect Link Types
second_title: Aspose.Cells for .NET API Reference
description: Detect link types in an Excel workbook using Aspose.Cells for .NET.
type: docs
weight: 80
url: /net/excel-workbook/detect-link-types/
---
In this tutorial, we will walk you through the provided C# source code step by step that will allow you to detect link types in an Excel workbook using Aspose.Cells for .NET. Follow the steps below to perform this operation.

## Step 1: Set source directory

```csharp
// source directory
string SourceDir = RunExamples.Get_SourceDirectory();
```

In this first step, we define the source directory where the Excel workbook containing the links is located.

## Step 2: Load Excel Workbook

```csharp
// Load the Excel workbook
Workbook workbook = new Workbook(SourceDir + "LinkTypes.xlsx");
```

We load the Excel workbook using the source file path.

## Step 3: Get the Spreadsheet

```csharp
// Get the first worksheet (default)
Worksheet worksheet = workbook.Worksheets[0];
```

We get the first worksheet of the workbook. You can change the `[0]` index to access a specific worksheet if needed.

## Step 4: Create a range of cells

```csharp
// Create a range of cells A1:B3
Range range = worksheet.Cells.CreateRange("A1", "A7");
```

We create a range of cells, in this example from cell A1 to cell A7. You can adjust cell references as needed.

## Step 5: Get the hyperlinks in range

```csharp
// Get the hyperlinks in the range
Hyperlink[] hyperlinks = range.Hyperlinks;
```

We get all the hyperlinks present in the specified range.

## Step 6: Browse Hyperlinks and View Link Types

```csharp
foreach (Hyperlink link in hyperlinks)
{
Console.WriteLine(link.TextToDisplay + ": " + link.LinkType);
}
```

We loop through each link and display the display text and associated link type.

### Sample source code for Detect Link Types using Aspose.Cells for .NET 
```csharp
//source directory
string SourceDir = RunExamples.Get_SourceDirectory();
Workbook workbook = new Workbook(SourceDir + "LinkTypes.xlsx");
// Get the first (default) worksheet
Worksheet worksheet = workbook.Worksheets[0];
// Create a range A2:B3
Range range = worksheet.Cells.CreateRange("A1", "A7");
// Get Hyperlinks in range
Hyperlink[] hyperlinks = range.Hyperlinks;
foreach (Hyperlink link in hyperlinks)
{
	Console.WriteLine(link.TextToDisplay + ": " + link.LinkType);
}
Console.WriteLine("DetectLinkTypes executed successfully.");
```

## Conclusion

Congratulation ! You have learned how to detect link types in an Excel workbook using Aspose.Cells for .NET. This feature allows you to work with the hyperlinks present in your Excel workbooks. Keep exploring the features of Aspose.Cells to expand your Excel workbook processing capabilities.

### FAQs

#### Q: How can I install Aspose.Cells for .NET in my project?

	 A: You can install Aspose.Cells for .NET using the NuGet package manager. Search for [Aspose Releases](https://releases.aspose.com/cells/net) in the NuGet Package Manager Console and install the latest version.

#### Q: Can I detect link types in specific worksheets rather than the first sheet?

	 A: Yes, you can modify the `workbook.Worksheets[0]` index to access a specific worksheet. For example, to access the second sheet, use `workbook.Worksheets[1]`.

#### Q: Is it possible to modify the types of links detected in the range?

	 A: Yes, you can browse hyperlinks and perform editing operations, such as updating URLs or removing unwanted links.

#### Q: What types of links are possible in Aspose.Cells for .NET?

	 A: Possible link types include hyperlinks, links to other worksheets, links to external files, links to websites, etc.

#### Q: Does Aspose.Cells for .NET support creating new links in a spreadsheet?

	 A: Yes, Aspose.Cells for .NET supports creating new links using the `Hyperlink` class and its associated properties. You can add hyperlinks, links to URLs, links to other spreadsheets, etc.

#### Q: Can I use Aspose.Cells for .NET in web applications?

	 A: Yes, Aspose.Cells for .NET can be used in web applications. You can embed it in ASP.NET, ASP.NET Core, and other .NET-based web frameworks.

#### Q: Are there any file size limits when using Aspose.Cells for .NET?

	 A: Aspose.Cells for .NET can process large Excel workbooks without specific limitation. However, the actual file size may be limited by available system resources.
