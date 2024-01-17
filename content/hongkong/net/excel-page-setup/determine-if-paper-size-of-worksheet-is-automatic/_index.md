---
title: 確定工作表的紙張尺寸是否自動
linktitle: 確定工作表的紙張尺寸是否自動
second_title: Aspose.Cells for .NET API 參考
description: 了解如何使用 Aspose.Cells for .NET 確定電子表格的紙張尺寸是否自動。
type: docs
weight: 20
url: /zh-hant/net/excel-page-setup/determine-if-paper-size-of-worksheet-is-automatic/
---
在本文中，我們將帶您逐步解釋以下 C# 原始碼： 使用 Aspose.Cells for .NET 確定工作表的紙張尺寸是否自動。我們將使用 .NET 的 Aspose.Cells 函式庫來執行此操作。請依照下列步驟確定工作表的紙張尺寸是否為自動。

## 第 1 步：載入工作簿
第一步是載入工作簿。我們將有兩本工作簿：一本停用自動紙張尺寸，另一本啟用自動紙張尺寸。這是載入工作簿的程式碼：

```csharp
//來源目錄
string sourceDir = "YOUR_SOURCE_DIR";
//輸出目錄
string outputDir = "YOUR_OUTPUT_DIRECTORY";

//載入第一個工作簿並停用自動紙張尺寸
Workbook wb1 = new Workbook(sourceDir + "samplePageSetupIsAutomaticPaperSize-False.xlsx");

//載入啟用了自動紙張尺寸的第二個工作簿
Workbook wb2 = new Workbook(sourceDir + "samplePageSetupIsAutomaticPaperSize-True.xlsx");
```

## 第 2 步：存取電子表格
現在我們已經加載了工作簿，我們需要訪問工作表，以便檢查自動紙張尺寸。我們將轉到兩個工作簿中的第一個工作表。這是存取它的程式碼：

```csharp
//轉到第一個工作簿的第一個工作表
Worksheet ws11 = wb1.Worksheets[0];

//轉到第二個工作簿的第一個工作表
Worksheet ws12 = wb2.Worksheets[0];
```

## 步驟 3：檢查自動紙張尺寸
在此步驟中，我們將檢查工作表紙張尺寸是否是自動的。我們將使用`PageSetup.IsAutomaticPaperSize`屬性來取得此資訊。然後我們將顯示結果。這是代碼：

```csharp
//顯示第一個工作簿中第一個工作表的 IsAutomaticPaperSize 屬性
Console.WriteLine("First worksheet in first workbook - IsAutomaticPaperSize: " + ws11.PageSetup.IsAutomaticPaperSize);

//在第二個工作簿中顯示第一個工作表的 IsAutomaticPaperSize 屬性
Console.WriteLine("First worksheet of second workbook - IsAutomaticPaperSize: " + ws12.PageSetup.IsAutomaticPaperSize);

```

### 使用 Aspose.Cells for .NET 確定工作表的紙張尺寸是否自動的範例原始碼 
```csharp
//原始碼目錄
string sourceDir = "YOUR_SOURCE_DIRECTORY";
//輸出目錄
string outputDir = "YOUR_OUTPUT_DIRECTORY";
//裝入第一個自動紙張尺寸為 false 的工作簿
Workbook wb1 = new Workbook(sourceDir + "samplePageSetupIsAutomaticPaperSize-False.xlsx");
//載入自動紙張尺寸為 true 的第二本工作簿
Workbook wb2 = new Workbook(sourceDir + "samplePageSetupIsAutomaticPaperSize-True.xlsx");
//訪問兩個工作簿的第一個工作表
Worksheet ws11 = wb1.Worksheets[0];
Worksheet ws12 = wb2.Worksheets[0];
//列印兩個工作表的 PageSetup.IsAutomaticPaperSize 屬性
Console.WriteLine("First Worksheet of First Workbook - IsAutomaticPaperSize: " + ws11.PageSetup.IsAutomaticPaperSize);
Console.WriteLine("First Worksheet of Second Workbook - IsAutomaticPaperSize: " + ws12.PageSetup.IsAutomaticPaperSize);
Console.WriteLine();
Console.WriteLine("DetermineIfPaperSizeOfWorksheetIsAutomatic executed successfully.\r\n");
```


## 結論
在本文中，我們學習如何使用 Aspose.Cells for .NET 自動決定工作表的紙張尺寸。我們遵循以下步驟：載入工作簿，

存取電子表格和自動紙張尺寸檢查。現在，您可以使用這些知識來確定電子表格的紙張尺寸是否是自動的。

### 常見問題解答

#### Q：如何使用 Aspose.Cells for .NET 載入工作簿？

答：您可以使用 Aspose.Cells 庫中的 Workbook 類別來載入工作簿。使用 Workbook.Load 方法從檔案載入工作簿。

#### Q：我可以檢查其他電子表格的自動紙張尺寸嗎？

答：是的，您可以透過存取對應 Worksheet 物件的 PageSetup.IsAutomaticPaperSize 屬性來檢查任何工作表的自動紙張尺寸。

#### Q：如何更改電子表格的自動紙張尺寸？

答：要變更工作表的自動紙張大小，您可以使用 PageSetup.IsAutomaticPaperSize 屬性並將其設定為所需的值（true 或 false）。

#### Q：Aspose.Cells for .NET 還提供哪些其他功能？

答：Aspose.Cells for .NET 提供了許多用於處理電子表格的功能，例如建立、修改和轉換工作簿，以及操作資料、公式和格式。