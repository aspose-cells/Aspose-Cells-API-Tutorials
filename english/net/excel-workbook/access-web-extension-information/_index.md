---
title: Access Web Extension Information
linktitle: Access Web Extension Information
second_title: Aspose.Cells for .NET API Reference
description: Access web extension information with Aspose.Cells for .NET.
type: docs
weight: 10
url: /net/excel-workbook/access-web-extension-information/
---
Access to web extension information is an essential feature when developing applications using Aspose.Cells for .NET. In this step by step guide, we will explain the provided C# source code that will allow you to access web extension information using Aspose.Cells for .NET. We'll also provide you with a conclusion and answer in Markdown format to make it easier to understand. Follow the steps below to get valuable information about web extensions.

## Step 1: Set source directory

```csharp
// source directory
string sourceDir = RunExamples.Get_SourceDirectory();
```

In this first step, we define the source directory that will be used to load the Excel file containing the web extension information.

## Step 2: Load the Excel file

```csharp
// Load the example Excel file
Workbook workbook = new Workbook(sourceDir + "WebExtensionsSample.xlsx");
```

Here we load the sample Excel file which contains the web extension information we want to retrieve.

## Step 3: Access information from the web extension task window

```csharp
WebExtensionTaskPaneCollection taskPanes = workbook.Worksheets.WebExtensionTaskPanes;
foreach(WebExtensionTaskPane taskPane in taskPanes)
{
Console.WriteLine("Width: " + taskPane.Width);
Console.WriteLine("Is visible: " + taskPane.IsVisible);
Console.WriteLine("Is locked: " + taskPane.IsLocked);
Console.WriteLine("Docking State: " + taskPane.DockState);
Console.WriteLine("Store Name: " + taskPane.WebExtension.Reference.StoreName);
Console.WriteLine("Store type: " + taskPane.WebExtension.Reference.StoreType);
Console.WriteLine("Web Extension ID: " + taskPane.WebExtension.Id);
}
```

In this step, we access the information of each web extension task window present in the Excel file. We display different properties such as width, visibility, lock state, home state, store name, store type, and web extension ID.

## Step 4: Show success message

```csharp
Console.WriteLine("AccessWebExtensionInformation executed successfully.");
```

Finally, we display a message indicating that the web extension information was accessed successfully.

### Sample source code for Access Web Extension Information using Aspose.Cells for .NET 
```csharp
//Source directory
string sourceDir = RunExamples.Get_SourceDirectory();
//Load sample Excel file
Workbook workbook = new Workbook(sourceDir + "WebExtensionsSample.xlsx");
WebExtensionTaskPaneCollection taskPanes = workbook.Worksheets.WebExtensionTaskPanes;
foreach (WebExtensionTaskPane taskPane in taskPanes)
{
	Console.WriteLine("Width: " + taskPane.Width);
	Console.WriteLine("IsVisible: " + taskPane.IsVisible);
	Console.WriteLine("IsLocked: " + taskPane.IsLocked);
	Console.WriteLine("DockState: " + taskPane.DockState);
	Console.WriteLine("StoreName: " + taskPane.WebExtension.Reference.StoreName);
	Console.WriteLine("StoreType: " + taskPane.WebExtension.Reference.StoreType);
	Console.WriteLine("WebExtension.Id: " + taskPane.WebExtension.Id);
}
Console.WriteLine("AccessWebExtensionInformation executed successfully.");
```

## Conclusion

In this tutorial, we learned how to access web extension information using Aspose.Cells for .NET. By following the steps provided, you will be able to easily extract task windows information from a web extension into an Excel file.


### FAQs

#### Q: What is Aspose.Cells for .NET?

	 A: Aspose.Cells for .NET is a powerful class library that allows .NET developers to create, modify, convert and manipulate Excel files with ease.

#### Q: Does Aspose.Cells support other programming languages?

	 A: Yes, Aspose.Cells supports multiple programming languages like C#, VB.NET, Java, PHP, Python, etc.

#### Q: Can I use Aspose.Cells in commercial projects?

	 A: Yes, Aspose.Cells is a commercial library and can be used in commercial projects according to the license agreement.

#### Q: Is there additional documentation on Aspose.Cells?

	 A: Yes, you can check out the full Aspose.Cells documentation on the official Aspose website for more information and resources.
