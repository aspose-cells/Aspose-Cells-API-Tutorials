---
title: 依索引刪除 Excel 工作表 C# 教學課程
linktitle: 依索引刪除 Excel 工作表
second_title: Aspose.Cells for .NET API 參考
description: 使用 Aspose.Cells for .NET 輕鬆刪除特定的 Excel 工作表。帶有程式碼範例的詳細教學。
type: docs
weight: 30
url: /zh-hant/net/excel-worksheet-csharp-tutorials/delete-excel-worksheet-by-index-csharp-tutorial/
---
在本教學中，我們將一步步向您講解下面的 C# 原始程式碼，該程式碼是使用 Aspose.Cells for .NET 刪除 Excel 工作表。我們將為每個步驟提供範例程式碼，以幫助您詳細了解流程。

## 第 1 步：定義文檔目錄

首先，您需要設定 Excel 檔案所在的目錄路徑。將程式碼中的「YOUR DOCUMENT DIRECTORY」替換為 Excel 檔案的實際路徑。

```csharp
//文檔目錄的路徑。
string dataDir = "YOUR DOCUMENT DIRECTORY";
```

## 步驟 2：建立文件流程並開啟 Excel 文件

接下來，您需要建立一個文件流並使用以下命令開啟 Excel 文件`FileStream`班級。

```csharp
//建立包含要開啟的 Excel 檔案的檔案流
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
```

## 第 3 步：實例化工作簿對象

開啟Excel檔案後，需要實例化一個`Workbook`目的。此物件代表 Excel 工作簿並提供各種方法和屬性來操作工作簿。

```csharp
//實例化 Workbook 物件
//透過文件流程開啟Excel文件
Workbook workbook = new Workbook(fstream);
```

## 步驟 4：依索引刪除工作表

若要從索引中刪除工作表，您可以使用`RemoveAt()`的方法`Worksheets`的對象`Workbook`目的。您要刪除的工作表的索引必須作為參數傳遞。

```csharp
//使用工作表索引刪除工作表
workbook.Worksheets.RemoveAt(0);
```

## 第 5 步：儲存工作簿

刪除工作表後，您可以使用下列命令儲存修改後的 Excel 工作簿`Save()`的方法`Workbook`目的。

```csharp
//儲存 Excel 工作簿
workbook.Save(dataDir + "output.out.xls");
```


### 使用 Aspose.Cells for .NET 以索引刪除 Excel 工作表的範例原始程式碼 C# 教學課程 
```csharp
//文檔目錄的路徑。
string dataDir = "YOUR DOCUMENT DIRECTORY";
//建立包含要開啟的 Excel 檔案的檔案流
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
//實例化 Workbook 物件
//透過檔案流程開啟Excel文件
Workbook workbook = new Workbook(fstream);
//使用工作表索引刪除工作表
workbook.Worksheets.RemoveAt(0);
//儲存工作簿
workbook.Save(dataDir + "output.out.xls");
```

## 結論

在本教程中，我們介紹了使用 Aspose.Cells for .NET 按索引刪除 Excel 工作表的逐步過程。透過遵循提供的程式碼範例和說明，您現在應該很好地了解如何在 C# 應用程式中執行此任務。 Aspose.Cells for .NET 提供了一整套用於處理 Excel 檔案的功能，讓您可以輕鬆操作工作表和相關資料。

### 常見問題 (FAQ)

#### 什麼是 Aspose.Cells for .NET？

Aspose.Cells for .NET 是一個功能強大的程式庫，可讓開發人員在其 .NET 應用程式中建立、操作和轉換 Excel 檔案。它提供了廣泛的功能來處理工作表、儲存格、公式、樣式等。

#### 如何安裝 Aspose.Cells for .NET？

要安裝 Aspose.Cells for .NET，您可以從 Aspose Releases (https://releases.aspose.com/cells/net）並按照提供的說明進行操作。您需要有效的許可證才能在應用程式中使用該庫。

#### 我可以一次刪除多個工作表嗎？

是的，您可以使用 Aspose.Cells for .NET 刪除多個工作表。您只需對要刪除的每個工作表重複刪除步驟即可。

#### 是否可以恢復已刪除的工作表？

不幸的是，一旦工作表被刪除，就無法直接從 Excel 檔案中復原。建議在刪除工作表之前建立 Excel 檔案的備份，以避免資料遺失。

#### Aspose.Cells for .NET 是否與不同版本的 Excel 相容？

是的，Aspose.Cells for .NET 與不同版本的 Excel 相容，包括 Excel 2003、Excel 2007、Excel 2010、Excel 2013、Excel 2016、Excel 2019 和 Excel for Office 365。它支援檔案格式 .xxls 和 .xls。