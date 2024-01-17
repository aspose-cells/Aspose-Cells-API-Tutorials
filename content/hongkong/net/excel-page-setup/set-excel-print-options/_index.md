---
title: 設定 Excel 列印選項
linktitle: 設定 Excel 列印選項
second_title: Aspose.Cells for .NET API 參考
description: 學習使用 Aspose.Cells for .NET 輕鬆操作 Excel 檔案並自訂列印選項。
type: docs
weight: 150
url: /zh-hant/net/excel-page-setup/set-excel-print-options/
---
在本指南中，我們將引導您了解如何使用 Aspose.Cells for .NET 設定 Excel 工作簿的列印選項。我們將引導您逐步完成所提供的 C# 原始程式碼來完成此任務。

## 第一步：建構環境

在開始之前，請確保您已設定開發環境並安裝了 Aspose.Cells for .NET。您可以從Aspose官方網站下載最新版本的程式庫。

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

## 步驟5：取得工作表的PageSetup引用

要設定列印選項，我們首先需要從工作表中取得 PageSetup 參考。使用以下程式碼取得參考：

```csharp
PageSetup pageSetup = workbook.Worksheets[0].PageSetup;
```

## 第 6 步：啟用列印網格線

若要列印網格線，請使用以下程式碼：

```csharp
pageSetup. PrintGridlines = true;
```

## 步驟 7：啟用行/列標題列印

若要啟用行標題和列標題的列印，請使用以下程式碼：

```csharp
pageSetup.PrintHeadings = true;
```

## 步驟 8：啟用黑白列印模式

若要啟用黑白模式列印工作表，請使用下列程式碼：

```csharp
pageSetup.BlackAndWhite = true;
```

## 步驟9：啟用回饋列印

若要允許列印出現在電子表格上的註釋，請使用以下程式碼：

```csharp
pageSetup.PrintComments = PrintCommentsType.PrintInPlace;
```

## 步驟 10：啟用草稿模式列印

若要在草稿模式下列印電子表格，請使用下列程式碼：

```csharp
pageSetup.PrintDraft = true;
```

## 步驟 11：啟用列印儲存格錯誤為 N/A

允許將單元格錯誤列印為

  如果不適用，請使用以下程式碼：

```csharp
pageSetup.PrintErrors = PrintErrorsType.PrintErrorsNA;
```

## 第 12 步：儲存 Excel 工作簿

若要儲存設定了列印選項的 Excel 工作簿，請使用`Save`Workbook物件的方法：

```csharp
workbook.Save(dataDir + "OtherPrintOptions_out.xls");
```

這會將 Excel 工作簿儲存在指定目錄中，檔案名稱為「OtherPrintOptions_out.xls」。

### 使用 Aspose.Cells for .NET 設定 Excel 列印選項的範例原始程式碼 
```csharp
//文檔目錄的路徑。
string dataDir = "YOUR DOCUMENT DIRECTORY";
//實例化 Workbook 物件
Workbook workbook = new Workbook();
//取得工作表PageSetup的引用
PageSetup pageSetup = workbook.Worksheets[0].PageSetup;
//允許列印網格線
pageSetup.PrintGridlines = true;
//允許列印行/列標題
pageSetup.PrintHeadings = true;
//允許以黑白模式列印工作表
pageSetup.BlackAndWhite = true;
//允許列印工作表上顯示的註釋
pageSetup.PrintComments = PrintCommentsType.PrintInPlace;
//允許以草稿品質列印工作表
pageSetup.PrintDraft = true;
//允許將儲存格錯誤列印為 N/A
pageSetup.PrintErrors = PrintErrorsType.PrintErrorsNA;
//儲存工作簿。
workbook.Save(dataDir + "OtherPrintOptions_out.xls");
```
## 結論

現在您已經了解如何使用 Aspose.Cells for .NET 設定 Excel 工作簿的列印選項。這個功能強大且使用者友善的程式庫可讓您以簡單有效的方式自訂 Excel 工作簿的列印設定。

### 常見問題解答


#### 1. 我可以進一步自訂列印選項，例如邊距或頁面方向嗎？

是的，Aspose.Cells for .NET 提供了廣泛的自訂列印選項，例如邊距、頁面方向、比例等。

#### 2. Aspose.Cells for .NET支援其他Excel檔案格式嗎？

是的，Aspose.Cells for .NET 支援多種 Excel 檔案格式，例如 XLSX、XLS、CSV、HTML、PDF 等。

#### 3. Aspose.Cells for .NET 是否與所有版本的.NET Framework 相容？

Aspose.Cells for .NET 與 .NET Framework 2.0 或更高版本相容，包括版本 3.5、4.0、4.5、4.6 等。