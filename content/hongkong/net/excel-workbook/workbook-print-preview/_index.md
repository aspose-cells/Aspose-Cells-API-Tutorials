---
title: 工作簿列印預覽
linktitle: 工作簿列印預覽
second_title: Aspose.Cells for .NET API 參考
description: 了解如何使用 Aspose.Cells for .NET 產生工作簿的列印預覽。
type: docs
weight: 170
url: /zh-hant/net/excel-workbook/workbook-print-preview/
---
使用 Aspose.Cells for .NET 處理 Excel 檔案時，工作簿的列印預覽是一項重要功能。您可以按照以下步驟輕鬆產生列印預覽：

## 第1步：指定來源目錄

首先，您需要指定要預覽的Excel檔案所在的來源目錄。操作方法如下：

```csharp
//來源目錄
string sourceDir = RunExamples.Get_SourceDirectory();
```

## 第 2 步：載入工作簿

然後需要從指定的Excel檔案載入Workbook工作簿。操作方法如下：

```csharp
//載入工作簿工作簿
Workbook workbook = new Workbook(sourceDir + "Book1.xlsx");
```

## 步驟 3：設定影像和列印選項

在產生列印預覽之前，您可以根據需要配置影像和列印選項。在此範例中，我們使用預設選項。操作方法如下：

```csharp
//圖像和列印選項
ImageOrPrintOptions imgOptions = new ImageOrPrintOptions();
```

## 步驟 4：產生工作簿的列印預覽

現在您可以使用 WorkbookPrintingPreview 類別產生 Workbook 工作簿的列印預覽。操作方法如下：

```csharp
//工作簿的列印預覽
WorkbookPrintingPreview preview = new WorkbookPrintingPreview(workbook, imgOptions);
Console.WriteLine("Workbook page count: " + preview.EvaluatedPageCount);
```

## 步驟 5：產生工作表的列印預覽

如果要產生特定工作表的列印預覽，可以使用 SheetPrintingPreview 類別。這是一個例子：

```csharp
//工作表的列印預覽
SheetPrintingPreview preview2 = new SheetPrintingPreview(workbook.Worksheets[0], imgOptions);
Console.WriteLine("Number of worksheet pages: " + preview2.EvaluatedPageCount);
```

### 使用 Aspose.Cells for .NET 的工作簿列印預覽的範例原始程式碼 
```csharp
//原始碼目錄
string sourceDir = RunExamples.Get_SourceDirectory();
Workbook workbook = new Workbook(sourceDir + "Book1.xlsx");
ImageOrPrintOptions imgOptions = new ImageOrPrintOptions();
WorkbookPrintingPreview preview = new WorkbookPrintingPreview(workbook, imgOptions);
Console.WriteLine("Workbook page count: " + preview.EvaluatedPageCount);
SheetPrintingPreview preview2 = new SheetPrintingPreview(workbook.Worksheets[0], imgOptions);
Console.WriteLine("Worksheet page count: " + preview2.EvaluatedPageCount);
Console.WriteLine("PrintPreview executed successfully.");
```

## 結論

產生工作簿的列印預覽是 Aspose.Cells for .NET 提供的強大功能。透過執行上面給出的步驟，您可以輕鬆預覽 Excel 工作簿並獲取有關要列印的頁數的資訊。

### 常見問題解答

#### Q：如何指定不同的來源目錄來載入我的工作簿？
    
答：您可以使用`Set_SourceDirectory`方法指定不同的來源目錄。例如：`RunExamples.Set_SourceDirectory("Path_to_the_source_directory")`.

#### Q：生成列印預覽時可以自訂影像和列印選項嗎？
    
答：是的，您可以透過更改圖像和列印選項的屬性來自訂圖像和列印選項。`ImageOrPrintOptions`目的。例如，您可以設定影像解析度、輸出檔案格式等。

#### Q：是否可以為工作簿中的多個工作表產生列印預覽？
    
答：是的，您可以迭代工作簿中的不同工作表，並使用`SheetPrintingPreview`班級。

#### Q：如何將列印預覽儲存為影像或 PDF 檔案？
    
答：你可以使用`ToImage`或者`ToPdf`的方法`WorkbookPrintingPreview`或者`SheetPrintingPreview`物件將列印預覽儲存為影像或 PDF 檔案。

#### Q：列印預覽生成後可以做什麼？
    
答：產生列印預覽後，您可以在螢幕上查看它，將其另存為圖像或 PDF 文件，或將其用於其他操作，例如透過電子郵件發送或列印。
	