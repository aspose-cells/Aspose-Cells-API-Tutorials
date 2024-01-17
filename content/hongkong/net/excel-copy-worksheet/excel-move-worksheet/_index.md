---
title: Excel 行動工作表
linktitle: Excel 行動工作表
second_title: Aspose.Cells for .NET API 參考
description: 使用 Aspose.Cells for .NET 輕鬆將工作表移至 Excel 工作簿中。
type: docs
weight: 40
url: /zh-hant/net/excel-copy-worksheet/excel-move-worksheet/
---
在本教學中，我們將引導您完成使用 .NET 的 Aspose.Cells 庫將工作表移至 Excel 工作簿的步驟。請按照以下說明完成此任務。


## 第 1 步：準備

確保您已安裝 Aspose.Cells for .NET 並在您首選的整合開發環境 (IDE) 中建立了 C# 專案。

## 第二步：設定文檔目錄路徑

聲明一個`dataDir`變數並使用文檔目錄的路徑對其進行初始化。例如 ：

```csharp
string dataDir = "YOUR_DIRECTORY_OF_DOCUMENTS";
```

一定要更換`"YOUR_DOCUMENTS_DIRECTORY"`與目錄的實際路徑。

## 第三步：定義輸入檔路徑

聲明一個`InputPath`變數並使用要修改的現有 Excel 檔案的完整路徑對其進行初始化。例如 ：

```csharp
string InputPath = dataDir + "book1.xls";
```

確保您有 Excel 文件`book1.xls`在您的文件目錄中或指定正確的檔案名稱和位置。

## 步驟 4：開啟 Excel 文件

使用`Workbook`Aspose.Cells 類別開啟指定的 Excel 檔案：

```csharp
Workbook wb = new Workbook(InputPath);
```

## 第 5 步：取得電子表格集合

創建一個`WorksheetCollection`物件引用工作簿中的工作表：

```csharp
WorksheetCollection sheets = wb.Worksheets;
```

## 第 6 步：取得第一個工作表

取得工作簿中的第一個工作表：

```csharp
Worksheet worksheet = sheets[0];
```

## 步驟 7：移動工作表

使用`MoveTo`將第一個工作表移至工作簿中的第三個位置的方法：

```csharp
worksheet.MoveTo(2);
```

## 步驟8：儲存修改後的Excel文件

儲存帶有移動的工作表的 Excel 檔案：

```csharp
wb.Save(dataDir + "MoveWorksheet_out.xls");
```

請務必指定輸出檔案所需的路徑和檔案名稱。

### 使用 Aspose.Cells for .NET 的 Excel 移動工作表的範例原始程式碼 
```csharp
//文檔目錄的路徑。
string dataDir = "YOUR DOCUMENT DIRECTORY";
string InputPath = dataDir + "book1.xls";
//開啟現有的 Excel 檔案。
Workbook wb = new Workbook(InputPath);
//建立一個 Worksheets 對象，參考
//工作簿的工作表。
WorksheetCollection sheets = wb.Worksheets;
//取得第一個工作表。
Worksheet worksheet = sheets[0];
//將第一張工作表移至工作簿中的第三個位置。
worksheet.MoveTo(2);
//儲存 Excel 檔案。
wb.Save(dataDir + "MoveWorksheet_out.xls");
```

## 結論

恭喜！現在您已經了解如何使用 Aspose.Cells for .NET 將工作表移至 Excel 工作簿。請隨意在您自己的專案中使用此方法來有效地操作 Excel 文件。

### 常見問題解答

#### Q：我可以將工作表移到同一 Excel 工作簿中的另一個位置嗎？

A. 是的，您可以使用下列命令將工作表移至相同 Excel 工作簿中的另一個位置`MoveTo`Worksheet 物件的方法。只需指定工作簿中目標位置的索引即可。

#### Q：我可以將工作表移至另一個 Excel 工作簿嗎？

A. 是的，您可以使用以下命令將工作表移至另一個 Excel 工作簿`MoveTo`Worksheet 物件的方法。只需指定目標工作簿中目標位置的索引即可。

#### Q：提供的原始程式碼是否可以與其他 Excel 檔案格式（例如 XLSX）一起使用？

A. 是的，提供的原始程式碼適用於其他 Excel 檔案格式，包括 XLSX。 Aspose.Cells for .NET 支援多種 Excel 檔案格式，可讓您操作工作表並將其移至不同的檔案類型。

#### Q：保存修改後的Excel檔案時如何指定輸出檔案路徑和名稱？

A. 儲存修改後的 Excel 檔案時，請使用`Save`Workbook 物件的方法，指定輸出檔案的完整路徑和名稱。請務必指定適當的檔案副檔名，例如`.xls`或者`.xlsx`，取決於所需的文件格式。