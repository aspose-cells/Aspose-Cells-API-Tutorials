---
title: Access Web Extension Information
linktitle: Access Web Extension Information
second_title: Aspose.Cells for .NET API Reference
description: 
type: docs
weight: 10
url: /net/excel-workbook/access-web-extension-information/
---
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