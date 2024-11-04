---
title: Access Excel Web Extension Information using Aspose.Cells
linktitle: Access Excel Web Extension Information using Aspose.Cells
second_title: Aspose.Cells .NET Excel Processing API
description: 
type: docs
weight: 10
url: /net/workbook-operations/access-web-extension-information/
---

## Complete Source Code
```csharp
using Aspose.Cells.WebExtensions;
using System;

namespace Aspose.Cells.Examples.CSharp._Workbook
{
    public class AccessWebExtensionInformation
    {
        public static void Run()
        {
            // ExStart:1
            //Source directory
            string sourceDir = "Your Document Directory";

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
            // ExEnd:1

            Console.WriteLine("AccessWebExtensionInformation executed successfully.");
        }
    }
}

```
