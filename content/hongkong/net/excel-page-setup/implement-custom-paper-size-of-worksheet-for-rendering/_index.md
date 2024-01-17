---
title: 實現工作表的自訂紙張尺寸以進行渲染
linktitle: 實現工作表的自訂紙張尺寸以進行渲染
second_title: Aspose.Cells for .NET API 參考
description: 使用 Aspose.Cells for .NET 實作自訂工作表大小的逐步指南。設定尺寸、新增訊息並另存為 PDF。
type: docs
weight: 50
url: /zh-hant/net/excel-page-setup/implement-custom-paper-size-of-worksheet-for-rendering/
---
當您想要建立具有特定尺寸的 PDF 文件時，為工作表實作自訂尺寸非常有用。在本教學中，我們將學習如何使用 Aspose.Cells for .NET 設定工作表的自訂大小，然後將文件另存為 PDF。

## 第 1 步：建立輸出資料夾

在開始之前，您需要建立一個輸出資料夾，用於保存生成的 PDF 檔案。您可以為輸出資料夾使用任何您想要的路徑。

```csharp
//輸出目錄
string outputDir = "YOUR_OUTPUT_FOLDER";
```

確保指定輸出資料夾的正確路徑。

## 第 2 步：建立 Workbook 對象

首先，您需要使用 Aspose.Cells 建立一個 Workbook 物件。該物件代表您的電子表格。

```csharp
//建立工作簿對象
Workbook wb = new Workbook();
```

## 第 3 步：存取第一個工作表

建立 Workbook 物件後，您可以存取其中的第一個工作表。

```csharp
//訪問第一個工作表
Worksheet ws = wb.Worksheets[0];
```

## 步驟 4：設定自訂工作表大小

現在您可以使用設定自訂工作表大小`CustomPaperSize(width, height)`PageSetup 類別的方法。

```csharp
//設定自訂工作表尺寸（以英吋為單位）
ws.PageSetup.CustomPaperSize(6, 4);
```

在此範例中，我們將工作表尺寸設定為 6 英吋寬和 4 英吋高。

## 第 5 步：訪問 B4 單元

之後，我們可以存取工作表中的特定儲存格。在本例中，我們將存取儲存格 B4。

```csharp
//訪問 B4 單元格
Cell b4 = ws.Cells["B4"];
```

## 步驟 6：在儲存格 B4 中新增訊息

我們現在可以使用以下命令將訊息新增至儲存格 B4`PutValue(value)`方法。

```csharp
//在儲存格 B4 中新增訊息
b4.PutValue("PDF page size: 6.00 x 4.00 inches");
```

在此範例中，我們在儲存格 B4 中新增了訊息「PDF 頁面大小：6.00」x 4.00」。

## 步驟 7：將工作表儲存為 PDF 格式

最後，我們可以使用以下命令將工作表儲存為 PDF 格式：`Save(filePath)` Workbook 物件的方法。

```csharp
//將工作表儲存為 PDF 格式
wb.Save(outputDir + "outputCustomPaperSize.pdf");
```

使用先前建立的輸出資料夾指定生成的 PDF 檔案的所需路徑。

### 使用 Aspose.Cells for .NET 實作工作表的自訂紙張尺寸進行渲染的範例原始程式碼 
```csharp
//輸出目錄
string outputDir = "YOUR_OUTPUT_DIRECTORY";
//建立工作簿對象
Workbook wb = new Workbook();
//訪問第一個工作表
Worksheet ws = wb.Worksheets[0];
//以英吋為單位設定自訂紙張尺寸
ws.PageSetup.CustomPaperSize(6, 4);
//訪問 B4 單元
Cell b4 = ws.Cells["B4"];
//在儲存格 B4 中新增訊息
b4.PutValue("Pdf Page Dimensions: 6.00 x 4.00 in");
//將工作簿儲存為 pdf 格式
wb.Save(outputDir + "outputCustomPaperSize.pdf");
```

## 結論

在本教學中，您學習如何使用 Aspose.Cells for .NET 實作工作表的自訂大小。您可以使用這些步驟設定工作表的特定尺寸，然後將文件儲存為 PDF 格式。我們希望本指南有助於理解實現自訂電子表格大小的過程。

### 常見問題 (FAQ)

#### 問題1：我可以進一步自訂電子表格佈局嗎？

是的，Aspose.Cells 提供了許多選項來自訂您的工作表佈局。您可以設定自訂尺寸、頁面方向、邊距、頁首和頁尾等等。

#### 問題2：Aspose.Cells還支援哪些其他輸出格式？

Aspose.Cells 支援許多不同的輸出格式，包括 PDF、XLSX、XLS、CSV、HTML、TXT 等。您可以根據需要選擇所需的輸出格式。