---
title: 設定 Excel 頁面順序
linktitle: 設定 Excel 頁面順序
second_title: Aspose.Cells for .NET API 參考
description: 使用 Aspose.Cells for .NET 在 Excel 中設定頁面順序的逐步指南。包括詳細的說明和原始程式碼。
type: docs
weight: 120
url: /zh-hant/net/excel-page-setup/set-excel-page-order/
---
在本文中，我們將逐步指導您解釋以下 C# 原始程式碼，以使用 Aspose.Cells for .NET 設定 Excel 頁面順序。我們將向您展示如何設定文件目錄、實例化 Workbook 物件、取得 PageSetup 參考、設定頁面列印順序以及儲存工作簿。

## 第 1 步：文檔目錄設置

在開始之前，您需要設定要儲存 Excel 檔案的文檔目錄。您可以透過替換值來指定目錄路徑`dataDir`變數與您自己的路徑。

```csharp
//文檔目錄的路徑。
string dataDir = "YOUR_DIRECTORY_OF_DOCUMENTS";
```

## 第 2 步：實例化工作簿對象

第一步是實例化 Workbook 物件。這代表我們將使用的 Excel 工作簿。

```csharp
//實例化 Workbook 物件
Workbook workbook = new Workbook();
```

## 步驟 3：取得 PageSetup 引用

接下來，我們需要取得要設定頁面順序的工作表的 PageSetup 物件參考。

```csharp
//取得工作表的PageSetup引用
PageSetup pageSetup = workbook.Worksheets[0].PageSetup;
```

## 步驟 4：設定頁面列印順序

現在我們可以設定頁面的列印順序。在此範例中，我們使用“OverThenDown”選項，這意味著頁面將從左到右列印，然後從上到下列印。

```csharp
//將頁面列印順序設定為“OverThenDown”
pageSetup.Order = PrintOrderType.OverThenDown;
```

## 第 5 步：儲存工作簿

最後，我們儲存頁面順序變更後的 Excel 工作簿。

```csharp
//儲存工作簿
workbook.Save(dataDir + "SetPageOrder_out.xls");
```

### 使用 Aspose.Cells for .NET 設定 Excel 頁面順序的範例原始程式碼 
```csharp
//文檔目錄的路徑。
string dataDir = "YOUR DOCUMENT DIRECTORY";
//實例化 Workbook 物件
Workbook workbook = new Workbook();
//取得工作表PageSetup的引用
PageSetup pageSetup = workbook.Worksheets[0].PageSetup;
//將頁面的列印順序設定為從上到下
pageSetup.Order = PrintOrderType.OverThenDown;
//儲存工作簿。
workbook.Save(dataDir + "SetPageOrder_out.xls");
```

## 結論

在本教學中，我們解釋如何使用 Aspose.Cells for .NET 在 Excel 檔案中設定頁面順序。透過依照提供的步驟操作，您可以輕鬆設定文件目錄、實例化 Workbook 物件、取得 PageSetup 參考、設定頁面列印順序以及儲存工作簿。

### 常見問題解答

#### Q1：為什麼在 Excel 檔案中設定頁面順序很重要？

定義 Excel 文件中的頁面順序非常重要，因為它決定了頁面的列印或顯示方式。透過指定特定順序，您可以邏輯地組織資料並使文件更易於閱讀或列印。

#### Q2：我可以在 Aspose.Cells for .NET 中使用其他頁面列印指令嗎？

是的，Aspose.Cells for .NET 支援多頁列印順序，例如「DownThenOver」、「OverThenDown」、「DownThenOverThenDownAgain」等。您可以選擇最適合您需求的一種。

#### Q3：我可以設定使用 Aspose.Cells for .NET 列印頁面的附加選項嗎？

是的，您可以使用 Aspose.Cells for .NET 中的 PageSetup 物件的屬性來設定各種頁面列印選項，例如比例、方向、邊距等。

#### Q4：Aspose.Cells for .NET 支援其他 Excel 檔案格式嗎？

是的，Aspose.Cells for .NET 支援多種 Excel 檔案格式，例如 XLSX、XLS、CSV、HTML、PDF 等。您可以使用該程式庫提供的功能輕鬆在這些格式之間進行轉換。