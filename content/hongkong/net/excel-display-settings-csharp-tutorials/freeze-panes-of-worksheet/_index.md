---
title: 凍結工作表的窗格
linktitle: 凍結工作表的窗格
second_title: Aspose.Cells for .NET API 參考
description: 使用 Aspose.Cells for .NET 輕鬆操作 Excel 工作表的凍結窗格。
type: docs
weight: 70
url: /zh-hant/net/excel-display-settings-csharp-tutorials/freeze-panes-of-worksheet/
---
在本教學中，我們將向您展示如何使用 C# 原始程式碼和 Aspose.Cells for .NET 鎖定 Excel 工作表中的窗格。請按照以下步驟操作以獲得所需的結果。

## 步驟1：導入必要的庫

確保您已安裝適用於 .NET 的 Aspose.Cells 庫並將必要的庫匯入到您的 C# 專案中。

```csharp
using Aspose.Cells;
```

## 步驟2：設定目錄路徑並開啟Excel文件

設定包含 Excel 檔案的目錄的路徑，然後透過實例化開啟該文件`Workbook`目的。

```csharp
string dataDir = "YOUR DOCUMENTS DIRECTORY";
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
Workbook workbook = new Workbook(fstream);
```

## 步驟 3：前往電子表格並套用窗格鎖定設定

使用以下命令導覽至 Excel 文件中的第一個工作表`Worksheet`目的。然後使用`FreezePanes`套用窗格鎖定設定的方法。

```csharp
Worksheet worksheet = workbook.Worksheets[0];
worksheet. FreezePanes(3, 2, 3, 2);
```

在上面的範例中，窗格被鎖定到第 3 行第 2 列中的儲存格。

## 第 4 步：儲存更改

進行必要的變更後，使用以下命令儲存修改後的 Excel 檔案：`Save`的方法`Workbook`目的。

```csharp
workbook.Save(dataDir + "output.xls");
```

### 使用 Aspose.Cells for .NET 凍結工作表窗格的範例原始碼 

```csharp
//文檔目錄的路徑。
string dataDir = "YOUR DOCUMENT DIRECTORY";
//建立包含要開啟的 Excel 檔案的檔案流
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
//實例化 Workbook 物件
//透過檔案流程開啟Excel文件
Workbook workbook = new Workbook(fstream);
//存取 Excel 文件中的第一個工作表
Worksheet worksheet = workbook.Worksheets[0];
//套用凍結窗格設定
worksheet.FreezePanes(3, 2, 3, 2);
//儲存修改後的Excel文件
workbook.Save(dataDir + "output.xls");
//關閉文件流以釋放所有資源
fstream.Close();
```

## 結論

本逐步指南向您展示如何使用 Aspose.Cells for .NET 鎖定 Excel 電子表格中的窗格。使用提供的 C# 原始程式碼，您可以輕鬆自訂窗格鎖定設置，以更好地組織和視覺化 Excel 文件中的資料。

### 常見問題 (FAQ)

#### 什麼是 Aspose.Cells for .NET？

Aspose.Cells for .NET 是一個功能強大的程式庫，用於在 .NET 應用程式中操作 Excel 檔案。

#### 如何安裝 Aspose.Cells for .NET？

要安裝Aspose.Cells for .NET，您需要從以下位置下載相關套件[Aspose 發布](https://releases/aspose.com/cells/net/)並將其新增至您的 .NET 專案。

#### 如何使用 Aspose.Cells for .NET 鎖定 Excel 工作表中的窗格？

您可以使用`FreezePanes`的方法`Worksheet`物件鎖定工作表的窗格。透過提供行索引和列索引來指定要鎖定的儲存格。

#### 我可以使用 Aspose.Cells for .NET 自訂窗格鎖定設定嗎？

是的，使用`FreezePanes`方法中，您可以根據需要指定要鎖定的儲存格，並提供適當的行索引和列索引。
