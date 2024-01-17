---
title: 刪除工作表的窗格
linktitle: 刪除工作表的窗格
second_title: Aspose.Cells for .NET API 參考
description: 使用 Aspose.Cells for .NET 從 Excel 工作表中刪除窗格的逐步指南。
type: docs
weight: 120
url: /zh-hant/net/excel-display-settings-csharp-tutorials/remove-panes-of-worksheet/
---
在本教學中，我們將說明如何使用 Aspose.Cells for .NET 從 Excel 工作表中刪除窗格。請按照以下步驟操作以獲得所需的結果：

## 第一步：建構環境

確保您已安裝 Aspose.Cells for .NET 並設定您的開發環境。另外，請確保您擁有要從中刪除窗格的 Excel 檔案的副本。

## 步驟2：導入必要的依賴項

新增必要的指令以使用 Aspose.Cells 中的類別：

```csharp
using Aspose.Cells;
```

## 第三步：程式碼初始化

首先初始化包含 Excel 文件的目錄的路徑：

```csharp
string dataDir = "YOUR DOCUMENTS DIRECTORY";
```

## 步驟 4：開啟 Excel 文件

實例化一個新的`Workbook`物件並使用開啟 Excel 文件`Open`方法：

```csharp
Workbook book = new Workbook(dataDir + "Book1.xls");
```

## 步驟 5：定義活動儲存格

使用以下指令設定工作表的活動儲存格`ActiveCell`財產：

```csharp
book.Worksheets[0].ActiveCell = "A20";
```

## 第 6 步：刪除窗格

使用下列命令從工作表視窗中刪除窗格`RemoveSplit`方法：

```csharp
book.Worksheets[0].RemoveSplit();
```

## 第 7 步：儲存更改

儲存對 Excel 檔案所做的變更：

```csharp
book.Save(dataDir + "output.xls");
```

### 使用 Aspose.Cells for .NET 刪除工作表窗格的範例原始碼 
```csharp
//文檔目錄的路徑。
string dataDir = "YOUR DOCUMENT DIRECTORY";
//實例化一個新工作簿並開啟範本文件
Workbook book = new Workbook(dataDir + "Book1.xls");
//設定活動儲存格
book.Worksheets[0].ActiveCell = "A20";
//分割工作表視窗
book.Worksheets[0].RemoveSplit();
//儲存 Excel 文件
book.Save(dataDir + "output.xls");
```

## 結論

在本教學中，您學習如何使用 Aspose.Cells for .NET 從 Excel 工作表中刪除窗格。透過執行所述步驟，您可以輕鬆自訂 Excel 檔案的外觀和行為。

### 常見問題 (FAQ)

#### 什麼是 Aspose.Cells for .NET？

Aspose.Cells for .NET 是一個流行的軟體庫，用於在 .NET 應用程式中操作 Excel 檔案。

#### 如何在 Aspose.Cells 中設定工作表的活動儲存格？

您可以使用以下命令設定活動儲存格`ActiveCell`Worksheet 物件的屬性。

#### 我可以從工作表視窗中僅刪除水平或垂直窗格嗎？

是的，使用 Aspose.Cells，您可以使用適當的方法僅刪除水平或垂直窗格，例如`RemoveHorizontalSplit`或者`RemoveVerticalSplit`.

#### Aspose.Cells 只能處理 .xls 格式的 Excel 檔案嗎？

不，Aspose.Cells 支援各種 Excel 檔案格式，包括 .xls 和 .xlsx。
	