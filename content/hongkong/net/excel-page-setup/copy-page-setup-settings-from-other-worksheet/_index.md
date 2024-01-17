---
title: 從其他工作表複製頁面設定設置
linktitle: 從其他工作表複製頁面設定設置
second_title: Aspose.Cells for .NET API 參考
description: 了解如何使用 Aspose.Cells for .NET 將頁面配置設定從一個電子表格複製到另一個電子表格。優化該庫的使用的分步指南。
type: docs
weight: 10
url: /zh-hant/net/excel-page-setup/copy-page-setup-settings-from-other-worksheet/
---
在本文中，我們將帶您逐步解釋以下 C# 原始程式碼：使用 Aspose.Cells for .NET 從另一個電子表格複製頁面配置設定。我們將使用 .NET 的 Aspose.Cells 函式庫來執行此操作。如果您要將頁面設定設定從一個工作表複製到另一個工作表，請依照下列步驟操作。

## 第 1 步：建立工作簿
第一步是建立工作簿。在我們的範例中，我們將使用 Aspose.Cells 函式庫提供的 Workbook 類別。以下是建立工作簿的程式碼：

```csharp
Workbook wb = new Workbook();
```

## 第 2 步：新增測試工作表
建立工作簿後，我們需要新增測試工作表。在此範例中，我們將新增兩個工作表。以下是新增兩個工作表的程式碼：

```csharp
wb.Worksheets.Add("TestSheet1");
wb.Worksheets.Add("TestSheet2");
```

## 第 3 步：訪問工作表
現在我們已經添加了工作表，我們需要訪問它們才能更改其設定。我們將使用「TestSheet1」和「TestSheet2」工作表的名稱來存取它們。這是存取它的程式碼：

```csharp
Worksheet TestSheet1 = wb. Worksheets["TestSheet1"];
Worksheet TestSheet2 = wb. Worksheets["TestSheet2"];
```

## 步驟 4：設定紙張尺寸
在此步驟中，我們將設定「TestSheet1」工作表的紙張大小。我們將使用`PageSetup.PaperSize`屬性來設定紙張尺寸。例如，我們將紙張尺寸設定為「PaperA3ExtraTransverse」。這是代碼：

```csharp
TestSheet1.PageSetup.PaperSize = PaperSizeType.PaperA3ExtraTransverse;
```

## 步驟 5：複製頁面設置
現在我們將頁面配置設定從「TestSheet1」工作表複製到「TestSheet2」。我們將使用`PageSetup.Copy`方法來執行此操作。這是代碼：

```csharp
TestSheet2.PageSetup.Copy(TestSheet1.PageSetup, new CopyOptions());
```

## 步驟 6：列印紙張尺寸
複製頁面設定設定後，我們將列印兩個工作表的紙張尺寸。我們將使用`Console.WriteLine`顯示紙張尺寸。這是代碼：

```csharp
Console.WriteLine("Before Paper Size: " + TestSheet1.PageSetup.PaperSize);
Console.WriteLine("Before Paper Size: " + TestSheet2.PageSetup.PaperSize);
```

### 使用 Aspose.Cells for .NET 從其他工作表複製頁面設定設定的範例原始程式碼 
```csharp
//建立工作簿
Workbook wb = new Workbook();
//新增兩個測試工作表
wb.Worksheets.Add("TestSheet1");
wb.Worksheets.Add("TestSheet2");
//存取兩個工作表作為 TestSheet1 和 TestSheet2
Worksheet TestSheet1 = wb.Worksheets["TestSheet1"];
Worksheet TestSheet2 = wb.Worksheets["TestSheet2"];
//將 TestSheet1 的紙張尺寸設定為 PaperA3ExtraTransverse
TestSheet1.PageSetup.PaperSize = PaperSizeType.PaperA3ExtraTransverse;
//列印兩張工作紙的紙張尺寸
Console.WriteLine("Before Paper Size: " + TestSheet1.PageSetup.PaperSize);
Console.WriteLine("Before Paper Size: " + TestSheet2.PageSetup.PaperSize);
Console.WriteLine();
//將 PageSetup 從 TestSheet1 複製到 TestSheet2
TestSheet2.PageSetup.Copy(TestSheet1.PageSetup, new CopyOptions());
//列印兩張工作紙的紙張尺寸
Console.WriteLine("After Paper Size: " + TestSheet1.PageSetup.PaperSize);
Console.WriteLine("After Paper Size: " + TestSheet2.PageSetup.PaperSize);
Console.WriteLine();
Console.WriteLine("CopyPageSetupSettingsFromSourceWorksheetToDestinationWorksheet executed successfully.\r\n");
```

## 結論
在本文中，我們學習如何使用 Aspose.Cells for .NET 將頁面配置設定從一個工作表複製到另一個工作表。我們完成了以下步驟：建立工作簿、新增測試工作表、存取工作表、設定紙張尺寸、複製頁面設定設定和列印紙張尺寸。現在您可以使用這些知識將頁面配置設定複製到您自己的專案中。

### 常見問題解答

#### Q：我可以在不同的工作簿實例之間複製頁面配置設定嗎？

答：是的，您可以使用以下命令在不同工作簿實例之間複製頁面設定設定`PageSetup.Copy`Aspose.Cells 函式庫的方法。

#### Q：我可以複製其他頁面設置，例如方向或邊距嗎？

答：是的，您可以使用複製其他頁面設定設置`PageSetup.Copy`方法與適當的選項。例如，您可以使用複製方向`CopyOptions.Orientation`和邊距使用`CopyOptions.Margins`.

#### Q：我如何知道紙張尺寸有哪些可用選項？

答：您可以查看 Aspose.Cells 庫 API 參考以取得可用的紙張尺寸選項。有一個列舉叫做`PaperSizeType`其中列出了支援的不同紙張尺寸。

#### Q：如何下載 .NET 的 Aspose.Cells 函式庫？

答：您可以從以下位置下載 .NET 的 Aspose.Cells 函式庫：[Aspose 發布](https://releases.aspose.com/cells/net)。有免費試用版以及商業用途的付費許可證。

#### Q：Aspose.Cells 函式庫支援其他程式語言嗎？

答：是的，Aspose.Cells 函式庫支援多種程式語言，包括 C#、Java、Python 等。