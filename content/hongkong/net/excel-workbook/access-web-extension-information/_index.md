---
title: 存取 Web 擴充資訊
linktitle: 存取 Web 擴充資訊
second_title: Aspose.Cells for .NET API 參考
description: 使用 Aspose.Cells for .NET 存取 Web 擴充資訊。
type: docs
weight: 10
url: /zh-hant/net/excel-workbook/access-web-extension-information/
---
使用 Aspose.Cells for .NET 開發應用程式時，存取 Web 擴充資訊是一項重要功能。在本逐步指南中，我們將解釋提供的 C# 原始程式碼，該程式碼將允許您使用 Aspose.Cells for .NET 存取 Web 擴充功能資訊。我們還將以 Markdown 格式為您提供結論和答案，使其更易於理解。請按照以下步驟獲取有關 Web 擴充功能的有價值的資訊。

## 第1步：設定來源目錄

```csharp
//來源目錄
string sourceDir = RunExamples.Get_SourceDirectory();
```

在第一步中，我們定義將用於載入包含 Web 擴充功能資訊的 Excel 檔案的來源目錄。

## 第 2 步：載入 Excel 文件

```csharp
//載入範例 Excel 文件
Workbook workbook = new Workbook(sourceDir + "WebExtensionsSample.xlsx");
```

這裡我們載入範例 Excel 文件，其中包含我們要檢索的 Web 擴充資訊。

## 步驟 3：從 Web 擴充任務視窗存取訊息

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

在此步驟中，我們存取 Excel 檔案中存在的每個 Web 擴充任務視窗的資訊。我們顯示不同的屬性，例如寬度、可見性、鎖定狀態、主狀態、商店名稱、商店類型和 Web 擴充 ID。

## 第四步：顯示成功訊息

```csharp
Console.WriteLine("AccessWebExtensionInformation executed successfully.");
```

最後，我們會顯示一則訊息，表示 Web 擴充資訊已成功存取。

### 使用 Aspose.Cells for .NET 存取 Web 擴充資訊的範例原始程式碼 
```csharp
//原始碼目錄
string sourceDir = RunExamples.Get_SourceDirectory();
//載入範例 Excel 文件
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

## 結論

在本教程中，我們學習如何使用 Aspose.Cells for .NET 存取 Web 擴充資訊。透過按照提供的步驟操作，您將能夠輕鬆地將任務視窗資訊從 Web 擴充功能提取到 Excel 文件中。


### 常見問題解答

#### Q：什麼是 Aspose.Cells for .NET？

答：Aspose.Cells for .NET 是一個功能強大的類別庫，可讓.NET 開發人員輕鬆建立、修改、轉換和操作 Excel 檔案。

#### Q：Aspose.Cells 支援其他程式語言嗎？

答：是的，Aspose.Cells 支援多種程式語言，如 C#、VB.NET、Java、PHP、Python 等。

#### Q：我可以在商業專案中使用 Aspose.Cells 嗎？

A：是的，Aspose.Cells是一個商業庫，根據許可協議可以在商業項目中使用。

#### Q：是否有關於 Aspose.Cells 的附加文件？

答：是的，您可以在 Aspose 官方網站上查看完整的 Aspose.Cells 文檔，以獲取更多資訊和資源。