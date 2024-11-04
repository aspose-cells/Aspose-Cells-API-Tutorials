---
title: Add Web Extension to Workbook using Aspose.Cells
linktitle: Add Web Extension to Workbook using Aspose.Cells
second_title: Aspose.Cells .NET Excel Processing API
description: 
type: docs
weight: 13
url: /net/workbook-operations/add-web-extension/
---

## Complete Source Code
```csharp
using Aspose.Cells.WebExtensions;
using System;

namespace Aspose.Cells.Examples.CSharp._Workbook
{
    public class AddWebExtension
    {
        public static void Run()
        {
            // ExStart:1
            //Source directory
            string outDir = "Your Document Directory";
            
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
            // ExEnd:1

            Console.WriteLine("AddWebExtension executed successfully.");
        }
    }
}

```
