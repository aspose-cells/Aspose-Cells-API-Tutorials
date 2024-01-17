---
title: 顯示和隱藏工作表捲軸
linktitle: 顯示和隱藏工作表捲軸
second_title: Aspose.Cells for .NET API 參考
description: 使用 Aspose.Cells for .NET 在 Excel 工作表中顯示或隱藏捲軸。
type: docs
weight: 50
url: /zh-hant/net/excel-display-settings-csharp-tutorials/display-and-hide-scroll-bars-of-worksheet/
---
在本教學中，我們將向您展示如何使用 C# 原始程式碼和 Aspose.Cells for .NET 在 Excel 工作表中顯示或隱藏垂直和水平捲軸。請按照以下步驟操作以獲得所需的結果。

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

## 第 3 步：隱藏捲軸

使用`IsVScrollBarVisible`和`IsHScrollBarVisible`的屬性`Workbook.Settings`物件隱藏工作表的垂直和水平捲軸。

```csharp
workbook.Settings.IsVScrollBarVisible = false;
workbook.Settings.IsHScrollBarVisible = false;
```

## 第 4 步：儲存更改

進行必要的變更後，使用以下命令儲存修改後的 Excel 檔案：`Save`的方法`Workbook`目的。

```csharp
workbook.Save(dataDir + "output.xls");
```

### 使用 Aspose.Cells for .NET 顯示和隱藏工作表捲軸的範例原始程式碼 

```csharp
//文檔目錄的路徑。
string dataDir = "YOUR DOCUMENT DIRECTORY";
//建立包含要開啟的 Excel 檔案的檔案流
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
//實例化 Workbook 物件
//透過檔案流程開啟Excel文件
Workbook workbook = new Workbook(fstream);
//隱藏Excel檔案的垂直滾動條
workbook.Settings.IsVScrollBarVisible = false;
//隱藏Excel檔案的水平滾動條
workbook.Settings.IsHScrollBarVisible = false;
//儲存修改後的Excel文件
workbook.Save(dataDir + "output.xls");
//關閉文件流以釋放所有資源
fstream.Close();
```

### 結論

本逐步指南向您展示如何使用 Aspose.Cells for .NET 在 Excel 電子表格中顯示或隱藏垂直和水平捲軸。使用提供的 C# 原始程式碼，您可以輕鬆自訂 Excel 檔案中捲軸的顯示。

### 常見問題 (FAQ)

#### 什麼是 Aspose.Cells for .NET？

Aspose.Cells for .NET 是一個功能強大的程式庫，用於在 .NET 應用程式中操作 Excel 檔案。

#### 如何安裝 Aspose.Cells for .NET？

要安裝Aspose.Cells for .NET，您需要從以下位置下載相關套件[Aspose 發布](https://releases/aspose.com/cells/net/)並將其新增至您的 .NET 專案。

#### 如何使用 Aspose.Cells for .NET 在 Excel 電子表格中顯示或隱藏捲軸？

您可以使用`IsVScrollBarVisible`和`IsHScrollBarVisible`的屬性`Workbook.Settings`物件分別在 Excel 工作表中顯示或隱藏垂直和水平捲軸。

#### Aspose.Cells for .NET 支援哪些其他 Excel 檔案格式？

Aspose.Cells for .NET支援多種Excel檔案格式，例如XLS、XLSX、CSV、HTML、PDF等。