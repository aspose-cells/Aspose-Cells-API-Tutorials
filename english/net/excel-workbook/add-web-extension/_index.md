---
title: Add Web Extension
linktitle: Add Web Extension
second_title: Aspose.Cells for .NET API Reference
description: 
type: docs
weight: 40
url: /net/excel-workbook/add-web-extension/
---
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