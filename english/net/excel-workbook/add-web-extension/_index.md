---
title: Add Web Extension
linktitle: Add Web Extension
second_title: Aspose.Cells for .NET API Reference
description: Easily add web extension to your Excel workbooks with Aspose.Cells for .NET.
type: docs
weight: 40
url: /net/excel-workbook/add-web-extension/
---
In this step by step tutorial, we will explain the provided C# source code that will allow you to add a web extension using Aspose.Cells for .NET. Follow the steps below to add a web extension to your Excel workbook.

## Step 1: Set output directory

```csharp
// Output directory
string outDir = RunExamples.Get_OutputDirectory();
```

In this first step, we define the output directory where the modified Excel workbook will be saved.

## Step 2: Create a new workbook

```csharp
// Create a new workbook
Workbook workbook = new Workbook();
```

Here we are creating a new Excel workbook using the `Workbook` class from Aspose.Cells.

## Step 3: Access the Web Extensions Collection

```csharp
// Access the collection of web extensions
WebExtensionCollection extensions = workbook.Worksheets.WebExtensions;
```

We access the Excel workbook's web extensions collection using the `WebExtensions` property of the `Worksheets` object.

## Step 4: Add a new web extension

```csharp
// Add a new web extension
int extensionIndex = extensions.Add();
WebExtension extension = extensions[extensionIndex];
extension.Reference.Id = "wa104379955";
extension.Reference.StoreName = "en-US";
extension.Reference.StoreType = WebExtensionStoreType.OMEX;
```

We are adding a new web extension to the extension collection. We define the reference ID, store name and store type of the extension.

## Step 5: Access the Web Extension Task Pane Collection

```csharp
// Access the web extension's task pane collection
WebExtensionTaskPaneCollection taskPanes = workbook.Worksheets.WebExtensionTaskPanes;
```

We access the Excel Workbook Web Extension task panes collection using the `WebExtensionTaskPanes` property of the `Worksheets` object.

## Step 6: Add a new task pane

```csharp
// Add a new task pane
int taskPaneIndex = taskPanes.Add();
WebExtensionTaskPane taskPane = taskPanes[taskPaneIndex];
taskPane. IsVisible = true;
taskPane. DockState = "right";
taskPane. WebExtension = extension;
```

We are adding a new task pane to the task pane collection. We set the pane's visibility, its docking state, and the associated web extension.

## Step 7: Save and close the workbook

```csharp
// Save and close the workbook
workbook.Save(outDir + "AddWebExtension_Out.xlsx");
Console.WriteLine("AddWebExtension executed successfully.");
```

We save the modified workbook to the specified output directory and then close it.

### Sample source code for Add Web Extension using Aspose.Cells for .NET 
```csharp
//Source directory
string outDir = RunExamples.Get_OutputDirectory();
Workbook workbook = new Workbook();
WebExtensionCollection extensions = workbook.Worksheets.WebExtensions;
WebExtensionTaskPaneCollection taskPanes = workbook.Worksheets.WebExtensionTaskPanes;
int extensionIndex = extensions.Add();
int taskPaneIndex = taskPanes.Add();
WebExtension extension = extensions[extensionIndex];
extension.Reference.Id = "wa104379955";
extension.Reference.StoreName = "en-US";
extension.Reference.StoreType = WebExtensionStoreType.OMEX;
WebExtensionTaskPane taskPane = taskPanes[taskPaneIndex];
taskPane.IsVisible = true;
taskPane.DockState = "right";
taskPane.WebExtension = extension;
workbook.Save(outDir + "AddWebExtension_Out.xlsx");
Console.WriteLine("AddWebExtension executed successfully.");
```

## Conclusion

Congratulation ! You have now learned how to add a web extension using Aspose.Cells for .NET. Experiment with code and explore additional features of Aspose.Cells to get the most out of manipulating web extensions in your Excel workbooks.

## FAQs

#### Q: What is a web extension in an Excel workbook?

	 A: A web extension in an Excel workbook is a component that allows you to add additional functionality to Excel by integrating web applications. It can offer interactive features, custom dashboards, external integrations, and more.

#### Q: How to add web extension to Excel workbook with Aspose.Cells?

	 A: To add a web extension to an Excel workbook with Aspose.Cells, you can follow the steps provided in our step by step guide. Use the `WebExtensionCollection` and `WebExtensionTaskPaneCollection` classes to add and configure the web extension and associated task pane.

#### Q: What information is required to add a web extension?

	 A: When adding a web extension, you must provide the extension SKU ID, store name, and store type. This information helps to identify and load the extension correctly.

#### Q: Can I add multiple web extensions to a single Excel workbook?

	 A: Yes, you can add multiple Web Extensions to a single Excel workbook. Use the `Add` method of the web extensions collection to add each extension, then associate them with the corresponding task panes.
