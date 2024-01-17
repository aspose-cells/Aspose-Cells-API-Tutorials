---
title: 工作表的分頁預覽
linktitle: 工作表的分頁預覽
second_title: Aspose.Cells for .NET API 參考
description: 使用 Aspose.Cells for .NET 顯示工作表分頁預覽的逐步指南。
type: docs
weight: 110
url: /zh-hant/net/excel-display-settings-csharp-tutorials/page-break-preview-of-worksheet/
---
在本教學中，我們將說明如何使用 Aspose.Cells for .NET 顯示工作表的分頁符號預覽。請按照以下步驟操作以獲得所需的結果：

## 第一步：建構環境

確保您已安裝 Aspose.Cells for .NET 並設定您的開發環境。另外，請確保您擁有要在其上顯示分頁符號預覽的 Excel 檔案的副本。

## 步驟2：導入必要的依賴項

新增必要的指令以使用 Aspose.Cells 中的類別：

```csharp
using Aspose.Cells;
using System.IO;
```

## 第三步：程式碼初始化

首先初始化包含 Excel 文件的目錄的路徑：

```csharp
string dataDir = "YOUR DOCUMENTS DIRECTORY";
```

## 步驟 4：開啟 Excel 文件

創建一個`FileStream`包含要開啟的 Excel 檔案的物件：

```csharp
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
```

實例化一個`Workbook`物件並使用文件流程開啟 Excel 文件：

```csharp
Workbook workbook = new Workbook(fstream);
```

## 第 5 步：存取電子表格

導覽至 Excel 文件中的第一個工作表：

```csharp
Worksheet worksheet = workbook.Worksheets[0];
```

## 步驟 6：顯示分頁預覽

啟用電子表格的分頁預覽：

```csharp
worksheet. IsPageBreakPreview = true;
```

## 第 7 步：儲存更改

儲存對 Excel 檔案所做的變更：

```csharp
workbook.Save(dataDir + "output.xls");
```

## 第8步：關閉文件流

關閉檔案流以釋放所有資源：

```csharp
fstream.Close();
```

### 使用 Aspose.Cells for .NET 進行工作表分頁預覽的範例原始程式碼 
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
//在分頁預覽中顯示工作表
worksheet.IsPageBreakPreview = true;
//儲存修改後的Excel文件
workbook.Save(dataDir + "output.xls");
//關閉文件流以釋放所有資源
fstream.Close();
```

## 結論

在本教學中，您學習如何使用 Aspose.Cells for .NET 顯示工作表的分頁符號預覽。透過執行所述步驟，您可以輕鬆控制 Excel 檔案的外觀和佈局。

### 常見問題 (FAQ)

#### 什麼是 Aspose.Cells for .NET？

Aspose.Cells for .NET 是一個流行的軟體庫，用於在 .NET 應用程式中操作 Excel 檔案。

#### 我可以顯示特定工作表而不是整個工作表的逐頁預覽嗎？

是的，使用 Aspose.Cells，您可以透過造訪對應的 Worksheet 物件來啟用特定工作表的分頁預覽。

#### Aspose.Cells 是否支援其他 Excel 檔案編輯功能？

是的，Aspose.Cells 提供了廣泛的編輯和操作 Excel 檔案的功能，例如新增資料、格式化、建立圖表等。

#### Aspose.Cells 只能處理 .xls 格式的 Excel 檔案嗎？

不，Aspose.Cells 支援各種 Excel 檔案格式，包括 .xls 和 .xlsx。
	