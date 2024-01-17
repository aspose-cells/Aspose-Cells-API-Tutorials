---
title: Excel 新增分頁符
linktitle: Excel 新增分頁符
second_title: Aspose.Cells for .NET API 參考
description: 了解如何使用 Aspose.Cells for .NET 在 Excel 中新增分頁符號。產生結構良好的報告的逐步教程。
type: docs
weight: 10
url: /zh-hant/net/excel-page-breaks/excel-add-page-breaks/
---
建立大型報表或文件時，在 Excel 檔案中新增分頁符號是一項基本功能。在本教學中，我們將探討如何使用 .NET 的 Aspose.Cells 函式庫在 Excel 檔案中加入分頁符號。我們將逐步指導您理解並實現所提供的 C# 原始程式碼。

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

## 第四步：新增水平分頁符

現在讓我們在 Excel 工作表中新增水平分頁符號。在範例程式碼中，我們為第一個工作表的儲存格「Y30」新增水平分頁符號。

```csharp
workbook.Worksheets[0].HorizontalPageBreaks.Add("Y30");
```

## 步驟 5：新增垂直分頁符

同樣，我們可以使用以下命令添加垂直分頁符`VerticalPageBreaks.Add()`方法。在我們的範例中，我們在第一個工作表的儲存格「Y30」中新增垂直分頁符號。

```csharp
workbook.Worksheets[0].VerticalPageBreaks.Add("Y30");
```

## 第 6 步：儲存 Excel 文件

現在我們已經新增了分頁符，我們需要儲存最終的 Excel 檔案。使用`Save()`方法來指定輸出檔案的完整路徑。

```csharp
//儲存 Excel 檔案。
workbook.Save(dataDir + "AddingPageBreaks_out.xls");
```
### 使用 Aspose.Cells for .NET 新增分頁符號的 Excel 範例原始程式碼 
```csharp
//文檔目錄的路徑。
string dataDir = "YOUR DOCUMENT DIRECTORY";
//實例化 Workbook 物件
Workbook workbook = new Workbook();
//在儲存格 Y30 處新增分頁符
workbook.Worksheets[0].HorizontalPageBreaks.Add("Y30");
workbook.Worksheets[0].VerticalPageBreaks.Add("Y30");
//儲存 Excel 檔案。
workbook.Save(dataDir + "AddingPageBreaks_out.xls");
```

## 結論

在本教程中，我們學習如何添加中斷

  使用 Aspose.Cells for .NET 的 Excel 檔案中的頁面。透過按照提供的步驟操作，您將能夠輕鬆地在動態生成的 Excel 檔案中插入水平和垂直分頁符號。請隨意嘗試更多 Aspose.Cells 庫，以發現它提供的其他強大功能。

### 常見問題解答

#### Q：Aspose.Cells for .NET 是免費函式庫嗎？

答：Aspose.Cells for .NET 是一個商業庫，但它提供了免費試用版，您可以使用它來評估其功能。

#### Q：我可以在 Excel 檔案中新增多個分頁符號嗎？

答：是的，您可以根據需要在電子表格的不同部分中添加任意數量的分頁符號。

#### Q：是否可以刪除先前新增的分頁符號？

答：是的，Aspose.Cells 允許您使用 Worksheet 物件的適當方法刪除現有分頁符號。

#### Q：此方法是否也適用於其他 Excel 檔案格式，例如 XLSX 或 XLSM？

答：是的，本教學中所述的方法適用於 Aspose.Cells 支援的各種 Excel 檔案格式。

#### Q：我可以自訂 Excel 中分頁符號的外觀嗎？

答：是的，Aspose.Cells 提供了一系列自訂分頁符號的功能，例如樣式、顏色和尺寸。
