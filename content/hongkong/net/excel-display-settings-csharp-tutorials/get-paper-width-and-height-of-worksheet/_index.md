---
title: 取得工作表的紙張寬度和高度
linktitle: 取得工作表的紙張寬度和高度
second_title: Aspose.Cells for .NET API 參考
description: 建立逐步指南來解釋以下 C# 原始程式碼，以使用 Aspose.Cells for .NET 取得電子表格的紙張寬度和高度。
type: docs
weight: 80
url: /zh-hant/net/excel-display-settings-csharp-tutorials/get-paper-width-and-height-of-worksheet/
---
在本教程中，我們將逐步向您解釋以下 C# 原始程式碼，以使用 Aspose.Cells for .NET 取得工作表的紙張寬度和高度。請依照以下步驟操作：

## 第 1 步：建立工作簿
首先使用建立一個新工作簿`Workbook`班級：

```csharp
Workbook wb = new Workbook();
```

## 第 2 步：存取第一個工作表
接下來，使用導覽至工作簿中的第一個工作表`Worksheet`班級：

```csharp
Worksheet ws = wb.Worksheets[0];
```

## 步驟 3：將紙張尺寸設為 A2 並以英吋為單位顯示紙張寬度和高度
使用`PaperSize`的財產`PageSetup`物件將紙張尺寸設為 A2，然後使用`PaperWidth`和`PaperHeight`屬性分別取得紙張的寬度和高度。使用以下命令顯示這些值`Console.WriteLine`方法：

```csharp
ws.PageSetup.PaperSize = PaperSizeType.PaperA2;
Console.WriteLine("PaperA2: " + ws.PageSetup.PaperWidth + "x" + ws.PageSetup.PaperHeight);
```

## 步驟 4：對其他紙張尺寸重複步驟
重複前面的步驟，將紙張尺寸變更為 A3、A4 和 Letter，然後顯示每種尺寸的紙張寬度和高度值：

```csharp
ws.PageSetup.PaperSize = PaperSizeType.PaperA3;
Console.WriteLine("PaperA3: " + ws.PageSetup.PaperWidth + "x" + ws.PageSetup.PaperHeight);

ws.PageSetup.PaperSize = PaperSizeType.PaperA4;
Console.WriteLine("PaperA4: " + ws.PageSetup.PaperWidth + "x" + ws.PageSetup.PaperHeight);

ws.PageSetup.PaperSize = PaperSizeType.PaperLetter;
Console.WriteLine("PaperLetter: " + ws.PageSetup.PaperWidth + "x" + ws.PageSetup.PaperHeight);
```

### 使用 Aspose.Cells for .NET 取得工作表紙張寬度和高度的範例原始程式碼 

```csharp
//建立工作簿
Workbook wb = new Workbook();
//訪問第一個工作表
Worksheet ws = wb.Worksheets[0];
//將紙張尺寸設定為 A2 並以英吋為單位列印紙張寬度和高度
ws.PageSetup.PaperSize = PaperSizeType.PaperA2;
Console.WriteLine("PaperA2: " + ws.PageSetup.PaperWidth + "x" + ws.PageSetup.PaperHeight);
//將紙張尺寸設為 A3 並以英吋為單位列印紙張寬度和高度
ws.PageSetup.PaperSize = PaperSizeType.PaperA3;
Console.WriteLine("PaperA3: " + ws.PageSetup.PaperWidth + "x" + ws.PageSetup.PaperHeight);
//將紙張尺寸設為 A4 並以英吋為單位列印紙張寬度和高度
ws.PageSetup.PaperSize = PaperSizeType.PaperA4;
Console.WriteLine("PaperA4: " + ws.PageSetup.PaperWidth + "x" + ws.PageSetup.PaperHeight);
//將紙張尺寸設為 Letter 並列印紙張寬度和高度（以英吋為單位）
ws.PageSetup.PaperSize = PaperSizeType.PaperLetter;
Console.WriteLine("PaperLetter: " + ws.PageSetup.PaperWidth + "x" + ws.PageSetup.PaperHeight);
```


## 結論

您學習如何使用 Aspose.Cells for .NET 取得電子表格的紙張寬度和高度。此功能對於 Excel 文件的配置和精確佈局非常有用。

### 常見問題 (FAQ)

#### 什麼是 Aspose.Cells for .NET？

Aspose.Cells for .NET 是一個功能強大的程式庫，用於在 .NET 應用程式中操作和處理 Excel 檔案。它提供了許多用於建立、修改、轉換和分析 Excel 文件的功能。

#### 如何使用 Aspose.Cells for .NET 取得電子表格的紙張尺寸？

您可以使用`PageSetup`的類別`Worksheet`對象訪問紙張尺寸。使用`PaperSize`屬性來設定紙張尺寸和`PaperWidth`和`PaperHeight`屬性分別取得紙張的寬度和高度。

#### Aspose.Cells for .NET 支援哪些紙張尺寸？

Aspose.Cells for .NET 支援各種常用的紙張尺寸，例如 A2、A3、A4 和 Letter，以及許多其他自訂尺寸。

#### 我可以使用 Aspose.Cells for .NET 自訂電子表格的紙張尺寸嗎？

是的，您可以透過使用指定精確的寬度和高度尺寸來設定自訂紙張尺寸`PaperWidth`和`PaperHeight`的屬性`PageSetup`班級。