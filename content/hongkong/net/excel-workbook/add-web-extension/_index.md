---
title: 新增網頁擴展
linktitle: 新增網頁擴展
second_title: Aspose.Cells for .NET API 參考
description: 使用 Aspose.Cells for .NET 輕鬆將 Web 擴充功能新增至您的 Excel 工作簿。
type: docs
weight: 40
url: /zh-hant/net/excel-workbook/add-web-extension/
---
在本逐步教程中，我們將解釋提供的 C# 原始程式碼，該程式碼將允許您使用 Aspose.Cells for .NET 新增 Web 擴充功能。請依照下列步驟將 Web 擴充功能新增至您的 Excel 工作簿。

## 第1步：設定輸出目錄

```csharp
//輸出目錄
string outDir = RunExamples.Get_OutputDirectory();
```

在第一步中，我們定義將儲存修改後的 Excel 工作簿的輸出目錄。

## 第 2 步：建立新工作簿

```csharp
//建立新工作簿
Workbook workbook = new Workbook();
```

在這裡，我們使用以下命令建立一個新的 Excel 工作簿`Workbook`來自 Aspose.Cells 的類別。

## 第 3 步：存取 Web 擴充集合

```csharp
//存取 Web 擴充集合
WebExtensionCollection extensions = workbook.Worksheets.WebExtensions;
```

我們使用以下命令存取 Excel 工作簿的 Web 擴充集合`WebExtensions`的財產`Worksheets`目的。

## 第 4 步：新增新的 Web 擴充

```csharp
//新增的網路擴展
int extensionIndex = extensions.Add();
WebExtension extension = extensions[extensionIndex];
extension.Reference.Id = "wa104379955";
extension.Reference.StoreName = "en-US";
extension.Reference.StoreType = WebExtensionStoreType.OMEX;
```

我們正在為擴充集合中新增一個新的 Web 擴充功能。我們定義擴充的參考 ID、商店名稱和商店類型。

## 步驟 5：存取 Web 擴充任務窗格集合

```csharp
//存取 Web 擴充功能的任務窗格集合
WebExtensionTaskPaneCollection taskPanes = workbook.Worksheets.WebExtensionTaskPanes;
```

我們使用以下命令存取 Excel Workbook Web Extension 任務窗格集合`WebExtensionTaskPanes`的財產`Worksheets`目的。

## 步驟 6：新增任務窗格

```csharp
//新增任務窗格
int taskPaneIndex = taskPanes.Add();
WebExtensionTaskPane taskPane = taskPanes[taskPaneIndex];
taskPane. IsVisible = true;
taskPane. DockState = "right";
taskPane. WebExtension = extension;
```

我們正在為任務窗格集合新增一個新的任務窗格。我們設定窗格的可見性、其停靠狀態以及關聯的 Web 擴充功能。

## 步驟 7：儲存並關閉工作簿

```csharp
//儲存並關閉工作簿
workbook.Save(outDir + "AddWebExtension_Out.xlsx");
Console.WriteLine("AddWebExtension executed successfully.");
```

我們將修改後的工作簿儲存到指定的輸出目錄，然後關閉它。

### 使用 Aspose.Cells for .NET 新增 Web 擴充功能的範例原始程式碼 
```csharp
//原始碼目錄
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

## 結論

恭喜！現在您已經了解如何使用 Aspose.Cells for .NET 新增 Web 擴充功能。試驗程式碼並探索 Aspose.Cells 的其他功能，以充分利用在 Excel 工作簿中操作 Web 擴充功能。

## 常見問題解答

#### Q：Excel 工作簿中的 Web 擴充功能是什麼？

答：Excel 工作簿中的 Web 擴充功能是一個元件，可讓您透過整合 Web 應用程式為 Excel 新增附加功能。它可以提供互動功能、自訂儀表板、外部整合等。

#### Q：如何使用 Aspose.Cells 將 Web 擴充功能新增至 Excel 工作簿？

答：要使用 Aspose.Cells 將 Web 擴充功能新增至 Excel 工作簿，您可以按照我們的逐步指南中提供的步驟進行操作。使用`WebExtensionCollection`和`WebExtensionTaskPaneCollection`用於新增和設定 Web 擴充及關聯任務窗格的類別。

#### Q：新增 Web 擴充功能需要哪些資訊？

答：新增 Web 擴充功能時，您必須提供擴充功能 SKU ID、商店名稱和商店類型。此資訊有助於正確識別和載入擴充功能。

#### Q：我可以為單一 Excel 工作簿新增多個 Web 擴充功能嗎？

答：是的，您可以將多個 Web 擴充功能新增到單一 Excel 工作簿中。使用`Add`Web 擴展集合的方法來新增每個擴展，然後將它們與對應的任務窗格關聯。