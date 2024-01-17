---
title: Excel 從其他工作簿複製工作表
linktitle: Excel 從其他工作簿複製工作表
second_title: Aspose.Cells for .NET API 參考
description: 使用 Aspose.Cells for .NET 輕鬆將 Excel 工作表從一個工作簿複製到另一個工作簿。
type: docs
weight: 10
url: /zh-hant/net/excel-copy-worksheet/excel-copy-worksheet-from-other-workbook/
---
在本教學中，我們將引導您完成使用 .NET 的 Aspose.Cells 庫從另一個工作簿複製 Excel 工作表的步驟。請按照以下說明完成此任務。

## 第 1 步：準備

在開始之前，請確保您已安裝 Aspose.Cells for .NET 並在您首選的整合開發環境 (IDE) 中建立了一個 C# 專案。

## 第二步：設定文檔目錄路徑

聲明一個`dataDir`變數並使用文檔目錄的路徑對其進行初始化。例如 ：

```csharp
string dataDir = "YOUR_DIRECTORY_OF_DOCUMENTS";
```

一定要更換`"YOUR_DOCUMENTS_DIRECTORY"`與目錄的實際路徑。

## 步驟 3：建立新的 Excel 工作簿

使用`Workbook`來自 Aspose.Cells 的類別來建立新的 Excel 工作簿：

```csharp
Workbook excelWorkbook0 = new Workbook();
```

## 步驟 4：取得工作簿中的第一個工作表

使用索引 0 導覽至工作簿中的第一個工作表：

```csharp
Worksheet ws0 = excelWorkbook0.Worksheets[0];
```

## 步驟 5：將資料新增至標題行 (A1:A4)

用一個`for`循環將資料新增至標題行 (A1:A4)：

```csharp
for (int i = 0; i < 5; i++)
{
     ws0.Cells[i, 0].PutValue(string.Format("Header row {0}", i));
}
```

## 步驟 6：新增詳細資料 (A5:A999)

使用另一個`for`循環添加詳細數據（A5：A999）：

```csharp
for (int i = 5; i < 1000; i++)
{
     ws0.Cells[i, 0].PutValue(string.Format("Detail row {0}", i));
}
```

## 第 7 步：設定佈局選項

使用以下命令設定工作表的頁面設定選項`PageSetup`目的：

```csharp
PageSetup pagesetup = ws0.PageSetup;
pagesetup.PrintTitleRows = "$1:$5";
```

## 步驟 8：建立另一個 Excel 工作簿

建立另一個 Excel 工作簿：

```csharp
Workbook excelWorkbook1 = new Workbook();
```

## 步驟 9：從第二個工作簿中取得第一個工作表

導覽至第二個工作簿中的第一個工作表：

```csharp
Worksheet ws1 = excelWorkbook1.Worksheets[0];
```

## 第 10 步：為工作表命名

為火命名

計算島：

```csharp
ws1.Name = "MySheet";
```

## 步驟 11：將資料從第一個工作簿的第一個工作表複製到第二個工作簿的第一個工作表

將資料從第一個工作簿的第一個工作表複製到第二個工作簿的第一個工作表：

```csharp
ws1.Copy(ws0);
```

## 步驟12：儲存Excel文件

儲存 Excel 檔案：

```csharp
excelWorkbook1.Save(dataDir + "CopyWorkbookSheetToOther_out.xls");
```

請務必指定輸出檔案所需的路徑和檔案名稱。

### 使用 Aspose.Cells for .NET 從其他工作簿複製工作表的 Excel 範例原始程式碼 
```csharp
//文檔目錄的路徑。
string dataDir = "YOUR DOCUMENT DIRECTORY";
//建立一個新的工作簿。
Workbook excelWorkbook0 = new Workbook();
//取得本書中的第一個工作表。
Worksheet ws0 = excelWorkbook0.Worksheets[0];
//將一些資料放入標題行 (A1:A4)
for (int i = 0; i < 5; i++)
{
	ws0.Cells[i, 0].PutValue(string.Format("Header Row {0}", i));
}
//放一些詳細數據（A5：A999）
for (int i = 5; i < 1000; i++)
{
	ws0.Cells[i, 0].PutValue(string.Format("Detail Row {0}", i));
}
//根據第一個工作表定義 pagesetup 物件。
PageSetup pagesetup = ws0.PageSetup;
//前五行在每頁重複...
//可以在列印預覽中看到。
pagesetup.PrintTitleRows = "$1:$5";
//建立另一個工作簿。
Workbook excelWorkbook1 = new Workbook();
//取得本書中的第一個工作表。
Worksheet ws1 = excelWorkbook1.Worksheets[0];
//為工作表命名。
ws1.Name = "MySheet";
//將第一個工作簿的第一個工作表中的資料複製到
//第二個工作簿的第一個工作表。
ws1.Copy(ws0);
//儲存 Excel 檔案。
excelWorkbook1.Save(dataDir + "CopyWorksheetFromWorkbookToOther_out.xls");
```

## 結論

恭喜！現在您已經了解如何使用 Aspose.Cells for .NET 從另一個工作簿複製 Excel 工作表。請隨意在您自己的專案中使用此方法來有效地操作 Excel 文件。

### 常見問題解答

#### Q：使用 Aspose.Cells for .NET 需要哪些函式庫？

A. 若要使用 Aspose.Cells for .NET，您必須在專案中包含 Aspose.Cells 函式庫。確保您在整合開發環境 (IDE) 中正確引用了該程式庫。

#### Q：Aspose.Cells 是否支援其他 Excel 檔案格式，例如 XLSX？

A. 是的，Aspose.Cells 支援各種 Excel 檔案格式，包括 XLSX、XLS、CSV、HTML 等。您可以使用 Aspose.Cells for .NET 的功能來操作這些檔案格式。

#### Q：複製工作表時我可以自訂佈局選項嗎？

A. 是的，您可以在複製工作表時使用工作表的屬性自訂頁面設定選項。`PageSetup`目的。您可以指定頁首、頁尾、邊距、方向等。