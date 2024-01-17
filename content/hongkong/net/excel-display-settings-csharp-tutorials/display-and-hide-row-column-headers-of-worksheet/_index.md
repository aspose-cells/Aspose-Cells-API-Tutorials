---
title: 顯示和隱藏工作表的行列標題
linktitle: 顯示和隱藏工作表的行列標題
second_title: Aspose.Cells for .NET API 參考
description: 使用 Aspose.Cells for .NET 在 Excel 工作表中顯示或隱藏行標題和列標題。
type: docs
weight: 40
url: /zh-hant/net/excel-display-settings-csharp-tutorials/display-and-hide-row-column-headers-of-worksheet/
---
在本教學中，我們將向您展示如何使用 C# 原始程式碼和 Aspose.Cells for .NET 顯示或隱藏 Excel 工作表的行標題和列標題。請按照以下步驟操作以獲得所需的結果。

## 步驟1：導入必要的庫

確保您已安裝適用於 .NET 的 Aspose.Cells 庫並將必要的庫匯入到您的 C# 專案中。

```csharp
using Aspose.Cells;
using System.IO;
```

## 步驟2：設定目錄路徑並開啟Excel文件

設定包含 Excel 檔案的目錄的路徑，然後透過建立檔案流並實例化一個檔案來開啟該文件`Workbook`目的。

```csharp
string dataDir = "YOUR DOCUMENTS DIRECTORY";
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
Workbook workbook = new Workbook(fstream);
```

## 步驟 3：前往第一個工作表並隱藏行標題和列標題

使用以下命令存取 Excel 文件中的第一個工作表`Worksheets`的財產`Workbook`目的。然後使用`IsRowColumnHeadersVisible`的財產`Worksheet`物件隱藏行標題和列標題。

```csharp
Worksheet worksheet = workbook.Worksheets[0];
worksheet. IsRowColumnHeadersVisible = false;
```

## 第 4 步：儲存更改

進行必要的變更後，使用以下命令儲存修改後的 Excel 檔案：`Save`的方法`Workbook`目的。

```csharp
workbook.Save(dataDir + "output.xls");
```

### 使用 Aspose.Cells for .NET 顯示和隱藏工作表行列標題的範例原始程式碼 
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
//隱藏行和列的標題
worksheet.IsRowColumnHeadersVisible = false;
//儲存修改後的Excel文件
workbook.Save(dataDir + "output.xls");
//關閉文件流以釋放所有資源
fstream.Close(); 
```

## 結論

本逐步指南向您展示如何使用 Aspose.Cells for .NET 在 Excel 電子表格中顯示或隱藏行標題和列標題。使用提供的 C# 原始程式碼，您可以輕鬆自訂 Excel 檔案中標題的顯示。

### 常見問題 (FAQ)

#### 什麼是 Aspose.Cells for .NET？

Aspose.Cells for .NET 是一個功能強大的程式庫，用於在 .NET 應用程式中操作 Excel 檔案。

#### 如何安裝 Aspose.Cells for .NET？

要安裝Aspose.Cells for .NET，您需要從以下位置下載相關套件[Aspose 發布](https://releases/aspose.com/cells/net/)並將其新增至您的 .NET 專案。

#### 如何使用 Aspose.Cells for .NET 顯示或隱藏 Excel 電子表格的行標題和列標題？

您可以使用`IsRowColumnHeadersVisible`的財產`Worksheet`顯示或隱藏行標題和列標題的物件。將其設定為`true`向他們展示並`false`隱藏它們。

#### Aspose.Cells for .NET 支援哪些其他 Excel 檔案格式？

Aspose.Cells for .NET 支援各種 Excel 檔案格式，例如 XLS、XLSX、CSV、HTML、PDF 等。
