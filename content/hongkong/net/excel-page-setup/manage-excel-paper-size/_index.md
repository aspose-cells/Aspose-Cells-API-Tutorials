---
title: 管理 Excel 紙張尺寸
linktitle: 管理 Excel 紙張尺寸
second_title: Aspose.Cells for .NET API 參考
description: 了解如何使用 Aspose.Cells for .NET 在 Excel 中管理紙張尺寸。帶有 C# 原始程式碼的逐步教程。
type: docs
weight: 70
url: /zh-hant/net/excel-page-setup/manage-excel-paper-size/
---
在本教學中，我們將逐步指導您如何使用 Aspose.Cells for .NET 管理 Excel 文件中的紙張尺寸。我們將向您展示如何使用 C# 原始碼配置紙張尺寸。

## 第一步：建構環境

請確定您的電腦上安裝了 Aspose.Cells for .NET。也可以在您首選的開發環境中建立一個新專案。

## 第二步：導入必要的函式庫

在您的程式碼檔案中，匯入使用 Aspose.Cells 所需的程式庫。這是對應的程式碼：

```csharp
using Aspose.Cells;
```

## 第三步：設定文檔目錄

設定要使用的 Excel 文件所在的目錄。使用以下程式碼設定目錄：

```csharp
string dataDir = "YOUR DOCUMENTS DIRECTORY";
```

請務必指定完整的目錄路徑。

## 第 4 步：建立工作簿對象

Workbook 物件代表您將使用的 Excel 文件。您可以使用以下程式碼建立它：

```csharp
Workbook workbook = new Workbook();
```

這將建立一個新的空 Workbook 物件。

## 第 5 步：存取第一個工作表

若要存取 Excel 文件的第一個電子表格，請使用以下程式碼：

```csharp
Worksheet worksheet = workbook.Worksheets[0];
```

這將允許您使用工作簿中的第一個工作表。

## 第 6 步：紙張尺寸設置

使用 Worksheet 物件的 PageSetup.PaperSize 屬性來設定紙張大小。在本例中，我們將紙張尺寸設定為 A4。這是對應的程式碼：

```csharp
worksheet.PageSetup.PaperSize = PaperSizeType.PaperA4;
```

這會將電子表格紙張尺寸設為 A4。

## 第 7 步：儲存工作簿

若要儲存工作簿的更改，請使用 Workbook 物件的 Save() 方法。這是對應的程式碼：

```csharp
workbook.Save(dataDir + "ManagePaperSize_out.xls");
```

這會將工作簿及其變更儲存到指定目錄。

### 使用 Aspose.Cells for .NET 管理 Excel 紙張大小的範例原始程式碼 
```csharp
//文檔目錄的路徑。
string dataDir = "YOUR DOCUMENT DIRECTORY";
//實例化 Workbook 物件
Workbook workbook = new Workbook();
//存取 Excel 文件中的第一個工作表
Worksheet worksheet = workbook.Worksheets[0];
//將紙張尺寸設定為A4
worksheet.PageSetup.PaperSize = PaperSizeType.PaperA4;
//儲存工作簿。
workbook.Save(dataDir + "ManagePaperSize_out.xls");
```
## 結論

現在您已經了解如何使用 Aspose.Cells for .NET 管理 Excel 文件中的紙張尺寸。本教學將引導您完成流程的每一步，從設定環境到儲存變更。現在您可以使用這些知識來自訂 Excel 文件的紙張尺寸。

### 常見問題解答

#### Q1：我可以設定A4以外的自訂紙張尺寸嗎？

A1：是的，Aspose.Cells 支援各種預先定義的紙張尺寸，並且能夠透過指定所需的尺寸來設定自訂紙張尺寸。

#### Q2：如何知道Excel文件中目前的紙張尺寸？

 A2：您可以使用`PageSetup.PaperSize`的財產`Worksheet`物件取得目前設定的紙張尺寸。

#### Q3：可以依照紙張尺寸設定額外頁邊距嗎？

 A3：是的，您可以使用`PageSetup.LeftMargin`, `PageSetup.RightMargin`, `PageSetup.TopMargin`和`PageSetup.BottomMargin`除了紙張尺寸之外，還可以設定其他頁邊距屬性。

#### 問題 4：此方法是否適用於所有 Excel 檔案格式，例如 .xls 和 .xlsx？

A4：是的，此方法適用於 .xls 和 .xlsx 檔案格式。

#### Q5：我可以對同一工作簿中的不同工作表套用不同的紙張尺寸嗎？

 A5：是的，您可以使用以下命令將不同的紙張尺寸應用於同一工作簿中的不同工作表：`PageSetup.PaperSize`每個工作表的屬性。