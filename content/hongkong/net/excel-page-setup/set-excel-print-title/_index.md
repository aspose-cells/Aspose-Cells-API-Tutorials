---
title: 設定 Excel 列印標題
linktitle: 設定 Excel 列印標題
second_title: Aspose.Cells for .NET API 參考
description: 了解如何使用 Aspose.Cells for .NET 輕鬆操作 Excel 檔案並自訂列印選項。
type: docs
weight: 170
url: /zh-hant/net/excel-page-setup/set-excel-print-title/
---
在本指南中，我們將引導您了解如何使用 Aspose.Cells for .NET 在 Excel 電子表格中設定列印標題。請依照以下步驟完成此任務。

## 第一步：建構環境

確保您已設定開發環境並安裝 Aspose.Cells for .NET。您可以從Aspose官方網站下載最新版本的程式庫。

## 步驟2：導入所需的命名空間

在您的 C# 專案中，匯入必要的命名空間以使用 Aspose.Cells：

```csharp
using Aspose.Cells;
```

## 第三步：設定文檔目錄路徑

聲明一個`dataDir`變數來指定要儲存產生的 Excel 檔案的目錄的路徑：

```csharp
string dataDir = "YOUR_DIRECTORY_OF_DOCUMENTS";
```

一定要更換`"YOUR_DOCUMENT_DIRECTORY"`與系統上的正確路徑。

## 第 4 步：建立工作簿對象

實例化一個代表要建立的 Excel 工作簿的 Workbook 物件：

```csharp
Workbook workbook = new Workbook();
```

## 第 5 步：存取第一個工作表

使用下列程式碼導覽至 Excel 工作簿中的第一個工作表：

```csharp
Worksheet worksheet = workbook.Worksheets[0];
```

## 第 6 步：定義標題列

使用以下程式碼定義標題列：

```csharp
pageSetup.PrintTitleColumns = "$A:$B";
```

這裡我們將 A 列和 B 列定義為標題列。您可以根據需要調整該值。

## 第 7 步：定義標題行

使用以下程式碼定義標題行：

```csharp
pageSetup.PrintTitleRows = "$1:$2";
```

我們將第 1 行和第 2 行定義為標題行。您可以根據需要調整這些值。

## 步驟 8：儲存 Excel 工作簿

若要儲存定義了列印標題的 Excel 工作簿，請使用`Save`Workbook物件的方法：

```csharp
workbook.Save(dataDir + "SetPrintTitle_out.xls");
```

這會將 Excel 工作簿儲存在指定目錄中，檔案名稱為「SetPrintTitle_out.xls」。

### 使用 Aspose.Cells for .NET 設定 Excel 列印標題的範例原始程式碼 
```csharp
//文檔目錄的路徑。
string dataDir = "YOUR DOCUMENT DIRECTORY";
//實例化 Workbook 物件
Workbook workbook = new Workbook();
//取得工作表PageSetup的引用
Aspose.Cells.PageSetup pageSetup = workbook.Worksheets[0].PageSetup;
//將列號 A 和 B 定義為標題列
pageSetup.PrintTitleColumns = "$A:$B";
//將行號 1 和 2 定義為標題行
pageSetup.PrintTitleRows = "$1:$2";
//儲存工作簿。
workbook.Save(dataDir + "SetPrintTitle_out.xls");
```

## 結論

恭喜！您已經了解如何使用 Aspose.Cells for .NET 在 Excel 電子表格中設定列印標題。列印標題可讓您在每個列印頁面上顯示特定的行和列，使資料更易於閱讀和引用。

### 常見問題解答

#### 1. Excel中可以為特定欄位設定列印標題嗎？

是的，使用 Aspose.Cells for .NET，您可以使用以下命令將特定列設定為列印標題`PrintTitleColumns`的財產`PageSetup`目的。

#### 2. 是否可以同時定義列標題和列印行標題？

是的，您可以使用以下命令設定列印列標題和行標題`PrintTitleColumns`和`PrintTitleRows`的屬性`PageSetup`目的。

#### 3. 我還可以使用 Aspose.Cells for .NET 自訂哪些其他佈局設定？

使用 Aspose.Cells for .NET，您可以自訂各種頁面佈局設置，例如邊距、頁面方向、列印比例等。