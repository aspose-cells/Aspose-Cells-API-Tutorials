---
title: Excel 複製工作表
linktitle: Excel 複製工作表
second_title: Aspose.Cells for .NET API 參考
description: 使用 Aspose.Cells for .NET 將一個 Excel 工作表複製到另一個。
type: docs
weight: 20
url: /zh-hant/net/excel-copy-worksheet/excel-copy-worksheet/
---

在本指南中，我們將說明如何使用 .NET 的 Aspose.Cells 庫複製 Excel 工作表。我們將為您提供 C# 原始程式碼，並引導您完成完成此任務所需的步驟。最後，我們將向您展示預期的結果。請按照以下說明開始操作。

## 第 1 步：準備

在開始之前，請確保您已安裝 Aspose.Cells for .NET 並在您首選的整合開發環境 (IDE) 中建立了一個 C# 專案。另請確保您擁有要操作的 Excel 檔案的副本。

## 步驟2：導入所需的庫

在 C# 原始檔中，使用下列命令從 Aspose.Cells 匯入必要的庫`using`指示：

```csharp
using Aspose.Cells;
```

## 第三步：設定檔案路徑

聲明一個`dataDir`變數並使用包含 Excel 檔案的目錄對其進行初始化。例如 ：

```csharp
string dataDir = "PATH_TO_YOUR_DOCUMENT_DIRECTORY";
```

一定要更換`"PATH_TO_YOUR_DOCUMENT_DIRECTORY"`與目錄的實際路徑。

## 第 4 步：載入現有 Excel 文件

使用`Workbook`Aspose.Cells 中的類別來開啟現有的 Excel 檔案。使用`InputPath`變數來指定檔案路徑：

```csharp
string InputPath = dataDir + "book1.xls";
Workbook wb = new Workbook(InputPath);
```

確保您已更換`"book1.xls"`與 Excel 檔案的實際名稱。

## 第 5 步：複製工作表

現在我們將現有工作表複製到新工作表。使用`Worksheets`的財產`Workbook`物件來存取工作表集合：

```csharp
WorksheetCollection sheets = wb.Worksheets;
```

然後使用`AddCopy`方法複製指定的工作表。例如，要複製“Sheet1”：

```csharp
sheets.AddCopy("Sheet1");
```

## 第 6 步：儲存 Excel 文件

使用`Save`的方法`Workbook`物件將更改儲存到新文件：

```csharp
wb.Save(dataDir + "CopyWithinWorkbook_out.xls");
```

請務必指定輸出檔案所需的路徑和檔案名稱。

### 使用 Aspose.Cells for .NET 的 Excel 複製工作表的範例原始程式碼 

```csharp
//文檔目錄的路徑。
string dataDir = "YOUR DOCUMENT DIRECTORY";
string InputPath = dataDir + "book1.xls";
//開啟現有的 Excel 檔案。
Workbook wb = new Workbook(InputPath);
//建立一個 Worksheets 對象，參考
//工作簿的工作表。
WorksheetCollection sheets = wb.Worksheets;
//將資料從現有工作表複製到新工作表
//工作簿中的工作表。
sheets.AddCopy("Sheet1");
//儲存 Excel 檔案。
wb.Save(dataDir + "CopyWithinWorkbook_out.xls");
```

## 結論

恭喜！現在您已經了解如何使用 Aspose.Cells for .NET 複製 Excel 工作表。本逐步指南展示如何匯入必要的庫、載入現有 Excel 檔案、複製工作表以及儲存修改後的檔案。請隨意在您自己的專案中使用此方法來有效地操作 Excel 文件。

### 常見問題解答

#### Q：Aspose.Cells 與其他程式語言相容嗎？

A. 是的，Aspose.Cells 支援多種程式語言，包括 C#、Java、Python 等。

#### Q：我可以將工作表複製到另一個 Excel 工作簿嗎？

A. 是的，您可以使用`AddCopy`方法將一個工作表複製到另一個 Excel 工作簿。

#### Q：複製工作表時，Aspose.Cells 是否保留公式和格式？

A. 是的，Aspose.Cells 在複製工作表時保留公式、格式和其他屬性。

#### Q：Aspose.Cells 是否需要商業使用許可證？

A. 是的，Aspose.Cells 是一個商業產品，需要購買商業用途的授權。您可以在 Aspose 的官方網站上找到更多許可資訊。