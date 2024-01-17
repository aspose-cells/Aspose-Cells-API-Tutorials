---
title: Excel 清除所有分頁符
linktitle: Excel 清除所有分頁符
second_title: Aspose.Cells for .NET API 參考
description: 了解如何使用 Aspose.Cells for .NET 刪除 Excel 中的所有分頁符號。清理 Excel 檔案的逐步教學。
type: docs
weight: 20
url: /zh-hant/net/excel-page-breaks/excel-clear-all-page-breaks/
---

刪除 Excel 檔案中的分頁符號是處理報表或電子表格時的重要步驟。在本教程中，我們將引導您逐步理解和實作所提供的 C# 原始程式碼，以使用適用於 .NET 的 Aspose.Cells 庫刪除 Excel 檔案中的所有分頁符號。

## 第一步：準備環境

在開始之前，請確保您的電腦上安裝了 Aspose.Cells for .NET。您可以從以下位置下載該程式庫[Aspose 發布](https://releases.aspose.com/cells/net)並按照提供的說明進行安裝。

安裝完成後，在您首選的整合開發環境 (IDE) 中建立新的 C# 項目，並匯入適用於 .NET 的 Aspose.Cells 庫。

## 第二步：配置文檔目錄路徑

在提供的原始程式碼中，您需要指定要儲存產生的Excel檔案的目錄路徑。修改`dataDir`變量，將“YOUR DOCUMENT DIRECTORY”替換為計算機上目錄的絕對路徑。

```csharp
//文檔目錄的路徑。
string dataDir = "PATH TO YOUR DOCUMENTS DIRECTORY";
```

## 第 3 步：建立工作簿對象

首先，我們需要建立一個代表 Excel 檔案的 Workbook 物件。這可以使用 Aspose.Cells 提供的 Workbook 類別來實現。

```csharp
//實例化 Workbook 物件
Workbook workbook = new Workbook();
```

## 步驟 4：刪除分頁符

現在我們要刪除 Excel 工作表中的所有分頁符號。在範例程式碼中，我們使用`Clear()`水平和垂直分頁符的方法將其全部刪除。

```csharp
workbook.Worksheets[0].HorizontalPageBreaks.Clear();
workbook.Worksheets[0].VerticalPageBreaks.Clear();
```

## 步驟 5：儲存 Excel 文件

刪除所有分頁符號後，我們可以儲存最終的 Excel 檔案。使用`Save()`方法來指定輸出檔案的完整路徑。

```csharp
//儲存 Excel 檔案。
workbook.Save(dataDir + "ClearingPageBreaks_out.xls");
```

### 使用 Aspose.Cells for .NET 清除所有分頁符號的 Excel 範例原始程式碼 

```csharp

//文檔目錄的路徑。
string dataDir = "YOUR DOCUMENT DIRECTORY";
//實例化 Workbook 物件
Workbook workbook = new Workbook();
//清除所有分頁符
workbook.Worksheets[0].HorizontalPageBreaks.Clear();
workbook.Worksheets[0].VerticalPageBreaks.Clear();
//儲存 Excel 檔案。
workbook.Save(dataDir + "ClearAllPageBreaks_out.xls");

```

## 結論

在本教學中，我們學習如何使用 Aspose.Cells for .NET 刪除 Excel 檔案中的所有分頁符號。透過按照提供的步驟操作，您可以輕鬆管理和清理動態產生的 Excel 檔案中不需要的分頁符號。請隨意進一步探索 Aspose.Cells 提供的功能以實現更高級的操作。

### 常見問題解答

#### Q：Aspose.Cells for .NET 是免費函式庫嗎？

答：Aspose.Cells for .NET 是一個商業庫，但它提供了免費試用版，您可以使用它來評估其功能。

#### Q：刪除分頁符號是否會影響其他工作表元素？

答：不會，刪除分頁符號只會更改分頁符號本身，不會影響工作表中的任何其他資料或格式。

#### Q：我可以選擇性地刪除 Excel 中的某些特定分頁符號嗎？

答：是的，使用 Aspose.Cells，您可以單獨存取每個分頁符，並在需要時使用適當的方法將其刪除。

#### Q：Aspose.Cells for .NET 支援哪些其他 Excel 檔案格式？

答：Aspose.Cells for .NET 支援各種 Excel 檔案格式，例如 XLSX、XLSM、CSV、HTML、PDF 等。

