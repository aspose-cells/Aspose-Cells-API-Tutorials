---
title: Excel 在工作簿之間複製工作表
linktitle: Excel 在工作簿之間複製工作表
second_title: Aspose.Cells for .NET API 參考
description: 使用 Aspose.Cells for .NET 在 Excel 工作簿之間輕鬆複製工作表。
type: docs
weight: 30
url: /zh-hant/net/excel-copy-worksheet/excel-copy-worksheets-between-workbooks/
---
在本教學中，我們將引導您完成使用 .NET 的 Aspose.Cells 庫在 Excel 工作簿之間複製工作表的步驟。請按照以下說明完成此任務。

## 第 1 步：準備

確保您已安裝 Aspose.Cells for .NET 並在您首選的整合開發環境 (IDE) 中建立了 C# 專案。

## 第二步：設定文檔目錄路徑

聲明一個`dataDir`變數並使用文檔目錄的路徑對其進行初始化。例如 ：

```csharp
string dataDir = "YOUR_DIRECTORY_OF_DOCUMENTS";
```

一定要更換`"YOUR_DOCUMENTS_DIRECTORY"`與目錄的實際路徑。

## 第三步：定義輸入檔路徑

聲明一個`InputPath`變數並使用要從中複製電子表格的 Excel 檔案的完整路徑對其進行初始化。例如 ：

```csharp
string InputPath = dataDir + "book1.xls";
```

確保您有 Excel 文件`book1.xls`在您的文件目錄中或指定正確的檔案名稱和位置。

## 步驟 4：建立第一個 Excel 工作簿

使用`Workbook`Aspose.Cells 類別建立第一個 Excel 工作簿並開啟指定檔案：

```csharp
Workbook excelWorkbook0 = new Workbook(InputPath);
```

## 步驟 5：建立第二個 Excel 工作簿

建立第二個 Excel 工作簿：

```csharp
Workbook excelWorkbook1 = new Workbook();
```

## 步驟 6：將工作表從第一個工作簿複製到第二個工作簿

使用`Copy`將第一個工作表從第一個工作簿複製到第二個工作簿的方法：

```csharp
excelWorkbook1.Worksheets[0].Copy(excelWorkbook0.Worksheets[0]);
```

## 步驟7：保存Excel文件

儲存包含複製的電子表格的 Excel 檔案：

```csharp
excelWorkbook1.Save(dataDir + "Copy WorksheetsBetweenWorkbooks_out.xls");
```

請務必指定輸出檔案所需的路徑和檔案名稱。

### 使用 Aspose.Cells for .NET 在工作簿之間複製工作表的 Excel 範例原始程式碼 
```csharp
//文檔目錄的路徑。
string dataDir = "YOUR DOCUMENT DIRECTORY";
string InputPath = dataDir + "book1.xls";
//建立工作簿。
//開啟第一本書中的文件。
Workbook excelWorkbook0 = new Workbook(InputPath);
//建立另一個工作簿。
Workbook excelWorkbook1 = new Workbook();
//將第一本書的第一頁複製到第二本書。
excelWorkbook1.Worksheets[0].Copy(excelWorkbook0.Worksheets[0]);
//儲存文件。
excelWorkbook1.Save(dataDir + "CopyWorksheetsBetweenWorkbooks_out.xls");
```

## 結論

恭喜！現在您已經了解如何使用 Aspose.Cells for .NET 在 Excel 工作簿之間複製工作表。請隨意在您自己的專案中使用此方法來有效地操作 Excel 文件。

### 常見問題解答

#### Q：使用 Aspose.Cells for .NET 需要哪些函式庫？

A. 若要使用 Aspose.Cells for .NET，您必須在專案中包含 Aspose.Cells 函式庫。確保您在整合開發環境 (IDE) 中正確引用了該程式庫。

#### Q：Aspose.Cells 是否支援其他 Excel 檔案格式，例如 XLSX？

A. 是的，Aspose.Cells 支援各種 Excel 檔案格式，包括 XLSX、XLS、CSV、HTML 等。您可以使用 Aspose.Cells for .NET 的功能來操作這些檔案格式。

#### Q：複製電子表格時我可以自訂版面選項嗎？

A. 是的，您可以在使用電子表格的屬性複製電子表格時自訂頁面設定選項。`PageSetup`目的。您可以指定頁首、頁尾、邊距、方向等。