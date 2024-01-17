---
title: 保護 Excel 工作表中的儲存格
linktitle: 保護 Excel 工作表中的儲存格
second_title: Aspose.Cells for .NET API 參考
description: 了解如何使用 Aspose.Cells for .NET 來保護 Excel 中的特定儲存格。 C# 逐步教學。
type: docs
weight: 30
url: /zh-hant/net/protect-excel-file/protect-cells-in-excel-worksheet/
---
Microsoft Excel 是一種廣泛使用的用於建立和管理電子表格的工具。 Excel 的核心功能之一是能夠保護某些儲存格以保持資料完整性。在本教學中，我們將逐步指導您使用 Aspose.Cells for .NET 保護 Excel 電子表格中的特定儲存格。 Aspose.Cells for .NET 是一個功能強大的程式庫，可輕鬆操作 Excel 文件，具有極大的靈活性和進階功能。請按照提供的步驟了解如何保護您的重要單元並確保您的資料安全。

## 第一步：建構環境

確保您的開發環境中安裝了 Aspose.Cells for .NET。從Aspose官方網站下載庫並查看文件以取得安裝說明。

## 步驟2：初始化工作簿和工作表

首先，我們需要建立一個新工作簿並取得要保護儲存格的工作表的參考。使用以下程式碼：

```csharp
//文檔目錄的路徑。
string dataDir = "YOUR DOCUMENTS DIRECTORY";
//如果該目錄尚不存在，則建立該目錄。
bool exists = System.IO.Directory.Exists(dataDir);
if (! exists)
     System.IO.Directory.CreateDirectory(dataDir);

//建立新工作簿
Workbook workbook = new Workbook();

//取得第一個工作表
Worksheet sheet = workbook.Worksheets[0];
```

在此程式碼片段中，我們首先定義儲存 Excel 檔案的目錄路徑。接下來，我們建立一個新的實例`Workbook`類別並使用以下命令取得第一個工作表的引用`Worksheets`財產。

## 第 3 步：定義單元格樣式

現在我們需要定義我們想要保護的單元格的樣式。使用以下程式碼：

```csharp
//定義樣式對象
Styling styling;

//循環遍歷工作表中的所有列並解鎖它們
for (int i = 0; i <= 255; i++)
{
     style = sheet.Cells.Columns[(byte)i].Style;
     style. IsLocked = false;
     leaf.Cells.Columns[(byte)i].ApplyStyle(style, new StyleFlag { Locked = true });
}
```

在此程式碼中，我們使用循環來遍歷工作表中的所有列，並透過設定樣式來解鎖它們的儲存格`IsLocked`財產給`false`。然後我們使用`ApplyStyle`方法將樣式套用到列`StyleFlag`標記以鎖定單元格。

## 第 4 步：保護特定細胞

現在我們要保護我們想要鎖定的特定單元格。使用以下程式碼：

```csharp
//鎖定三個儲存格：A1、B1、C1
style = sheet.Cells["A1"].GetStyle();
style. IsLocked = true;
sheet.Cells["A1"].SetStyle(style);

style = sheet.Cells["B1"].GetStyle();
style. IsLocked = true;
sheet.Cells["B1"].SetStyle(style);

style = sheet.Cells["C1"].GetStyle();
style. IsLocked = true;
sheet.Cells["C1"].SetStyle(style);
```

在此程式碼中，我們使用以下方法來取得每個特定單元格的樣式`GetStyle`方法，然後我們設定`IsLocked`樣式的屬性為`true`鎖定單元格。最後，我們使用更新的樣式應用到每個單元格`SetStyle`方法。

## 步驟 5：保護工作表

現在我們已經定義了要保護的儲存格，我們可以保護工作表本身。使用以下程式碼：

```csharp
//保護工作表
leaf.Protect(ProtectionType.All);
```

這段程式碼使用了`Protect`使用指定保護類型保護工作表的方法，在本例中`ProtectionType.All`它保護工作表中的所有項目。

## 第 6 步：儲存 Excel 文件

最後，我們儲存所做更改的 Excel 檔案。使用以下程式碼：

```csharp
//儲存 Excel 文件
workbook.Save(dataDir + "output.xls", SaveFormat.Excel97To2003);
```

在此程式碼中，我們使用`Save`方法將工作簿保存在指定目錄中`Excel97To2003`格式。

### 使用 Aspose.Cells for .NET 保護 Excel 工作表中的儲存格的範例原始程式碼 
```csharp
//文檔目錄的路徑。
string dataDir = "YOUR DOCUMENT DIRECTORY";
//如果目錄尚不存在，則建立該目錄。
bool IsExists = System.IO.Directory.Exists(dataDir);
if (!IsExists)
    System.IO.Directory.CreateDirectory(dataDir);
//建立一個新工作簿。
Workbook wb = new Workbook();
//建立一個工作表物件並取得第一個工作表。
Worksheet sheet = wb.Worksheets[0];
//定義樣式物件。
Style style;
//定義 styleflag 對象
StyleFlag styleflag;
//循環遍歷工作表中的所有列並解鎖它們。
for (int i = 0; i <= 255; i++)
{
    style = sheet.Cells.Columns[(byte)i].Style;
    style.IsLocked = false;
    styleflag = new StyleFlag();
    styleflag.Locked = true;
    sheet.Cells.Columns[(byte)i].ApplyStyle(style, styleflag);
}
//鎖定三個儲存格...即 A1、B1、C1。
style = sheet.Cells["A1"].GetStyle();
style.IsLocked = true;
sheet.Cells["A1"].SetStyle(style);
style = sheet.Cells["B1"].GetStyle();
style.IsLocked = true;
sheet.Cells["B1"].SetStyle(style);
style = sheet.Cells["C1"].GetStyle();
style.IsLocked = true;
sheet.Cells["C1"].SetStyle(style);
//最後，現在保護紙張。
sheet.Protect(ProtectionType.All);
//儲存 Excel 檔案。
wb.Save(dataDir + "output.xls", SaveFormat.Excel97To2003);
```

## 結論

恭喜！您已了解如何使用 Aspose.Cells for .NET 保護 Excel 電子表格中的特定儲存格。現在您可以在自己的專案中應用此技術並提高 Excel 檔案的安全性。


### 常見問題解答

#### Q：為什麼我應該使用 Aspose.Cells for .NET 來保護 Excel 電子表格中的儲存格？

答：Aspose.Cells for .NET 是一個功能強大的函式庫，可以輕鬆處理 Excel 檔案。它提供了保護單元、解鎖範圍等高級功能。

#### 問：是否可以保護一定範圍的細胞而不是單一細胞？

答：是的，您可以使用下列命令定義要保護的特定儲存格範圍：`ApplyStyle`方法與適當的`StyleFlag`.

#### Q：儲存後如何開啟受保護的 Excel 檔案？

答：當您開啟受保護的 Excel 檔案時，您需要提供保護工作表時指定的密碼。

#### Q：是否可以對 Excel 電子表格套用其他類型的保護？

答：是的，Aspose.Cells for .NET 支援多種類型的保護，例如結構保護、視窗保護等。您可以根據需要選擇適當的保護類型。