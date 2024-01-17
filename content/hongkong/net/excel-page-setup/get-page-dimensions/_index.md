---
title: 取得頁面尺寸
linktitle: 取得頁面尺寸
second_title: Aspose.Cells for .NET API 參考
description: 了解如何使用 Aspose.Cells for .NET 在 Excel 中擷取頁面尺寸。帶有 C# 原始程式碼的逐步指南。
type: docs
weight: 40
url: /zh-hant/net/excel-page-setup/get-page-dimensions/
---
Aspose.Cells for .NET 是一個功能強大的程式庫，可讓開發人員以程式設計方式處理 Microsoft Excel 檔案。它提供了廣泛的用於操作 Excel 文件的功能，包括獲取頁面尺寸的功能。在本教學中，我們將引導您完成使用 Aspose.Cells for .NET 擷取頁面尺寸的步驟。

## 步驟 1：建立 Workbook 類別的實例

首先，我們需要建立 Workbook 類別的一個實例，它代表 Excel 工作簿。這可以使用以下程式碼來實現：

```csharp
Workbook book = new Workbook();
```

## 第 2 步：存取電子表格

接下來，我們需要導覽到工作簿中要設定頁面尺寸的工作表。在此範例中，假設我們要使用第一個工作表。我們可以使用以下程式碼存取它：

```csharp
Worksheet sheet = book.Worksheets[0];
```

## 步驟 3：將紙張尺寸設為 A2，並以英吋為單位列印寬度和高度

現在我們將紙張尺寸設為A2，並以英吋為單位列印頁面寬度和高度。這可以使用以下程式碼來實現：

```csharp
sheet.PageSetup.PaperSize = PaperSizeType.PaperA2;
Console.WriteLine("A2: " + sheet.PageSetup.PaperWidth + "x" + sheet.PageSetup.PaperHeight);
```

## 步驟 4：將紙張尺寸設為 A3，並以英吋為單位列印寬度和高度

接下來，我們將紙張尺寸設為 A3 並以英吋為單位列印頁面寬度和高度。這是對應的程式碼：

```csharp
sheet.PageSetup.PaperSize = PaperSizeType.PaperA3;
Console.WriteLine("A3: " + sheet.PageSetup.PaperWidth + "x" + sheet.PageSetup.PaperHeight);
```

## 步驟 5：將紙張尺寸設為 A4，並以英吋為單位列印寬度和高度

現在，我們將紙張尺寸設為 A4，並以英吋為單位列印頁面寬度和高度。這是代碼：

```csharp
sheet.PageSetup.PaperSize = PaperSizeType.PaperA4;
Console.WriteLine("A4: " + sheet.PageSetup.PaperWidth + "x" + sheet.PageSetup.PaperHeight);
```

## 步驟 6：將紙張尺寸設定為 Letter 並以英吋為單位列印寬度和高度

最後，我們將紙張尺寸設為 Letter 並以英吋為單位列印頁面寬度和高度。這是代碼：

```csharp
sheet.PageSetup.PaperSize = PaperSizeType.PaperLetter;
Console.WriteLine("Letter: " + sheet.PageSetup.PaperWidth + "x" + sheet.PageSetup.PaperHeight);
```

### 使用 Aspose.Cells for .NET 取得頁面尺寸的範例原始程式碼 
```csharp
//建立 Workbook 類別的實例
Workbook book = new Workbook();
//訪問第一個工作表
Worksheet sheet = book.Worksheets[0];
//將紙張尺寸設定為 A2 並以英吋為單位列印紙張寬度和高度
sheet.PageSetup.PaperSize = PaperSizeType.PaperA2;
Console.WriteLine("PaperA2: " + sheet.PageSetup.PaperWidth + "x" + sheet.PageSetup.PaperHeight);
//將紙張尺寸設為 A3 並以英吋為單位列印紙張寬度和高度
sheet.PageSetup.PaperSize = PaperSizeType.PaperA3;
Console.WriteLine("PaperA3: " + sheet.PageSetup.PaperWidth + "x" + sheet.PageSetup.PaperHeight);
//將紙張尺寸設為 A4 並以英吋為單位列印紙張寬度和高度
sheet.PageSetup.PaperSize = PaperSizeType.PaperA4;
Console.WriteLine("PaperA4: " + sheet.PageSetup.PaperWidth + "x" + sheet.PageSetup.PaperHeight);
//將紙張尺寸設為 Letter 並列印紙張寬度和高度（以英吋為單位）
sheet.PageSetup.PaperSize = PaperSizeType.PaperLetter;
Console.WriteLine("PaperLetter: " + sheet.PageSetup.PaperWidth + "x" + sheet.PageSetup.PaperHeight);
Console.WriteLine("GetPageDimensions executed successfully.\r\n");
```

## 結論

恭喜！您學習如何使用 Aspose.Cells for .NET 擷取頁面尺寸。當您需要根據 Excel 文件中的頁面尺寸執行特定操作時，此功能非常有用。

不要忘記進一步探索 Aspose.Cells 的文檔，以發現它提供的所有強大功能。

### 常見問題解答

#### 1. Aspose.Cells for .NET 支援哪些其他紙張尺寸？

Aspose.Cells for .NET 支援多種紙張尺寸，包括 A1、A5、B4、B5、Executive、Legal、Letter 等。您可以查看文件以取得支援的紙張尺寸的完整清單。

#### 2. 我可以使用 Aspose.Cells for .NET 設定自訂頁面尺寸嗎？

是的，您可以透過指定所需的寬度和高度來設定自訂頁面尺寸。 Aspose.Cells 提供了完全的靈活性，可以根據您的需求自訂頁面尺寸。

#### 3. 我可以獲得英吋以外的頁面尺寸嗎？

是的，Aspose.Cells for .NET 可讓您取得不同單位的頁面尺寸，包括英吋、公分、毫米和磅。

#### 4. Aspose.Cells for .NET支援其他頁面設定編輯功能嗎？

是的，Aspose.Cells 提供了編輯頁面設定的全套功能，包括設定邊距、方向、頁首和頁尾等。