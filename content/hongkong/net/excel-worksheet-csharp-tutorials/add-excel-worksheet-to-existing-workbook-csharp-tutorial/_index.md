---
title: 將 Excel 工作表新增至現有工作簿 C# 教學課程
linktitle: 將 Excel 工作表新增至現有工作簿
second_title: Aspose.Cells for .NET API 參考
description: 使用 Aspose.Cells for .NET 輕鬆將新工作表新增至現有 Excel 工作簿。帶有程式碼範例的分步教程。
type: docs
weight: 10
url: /zh-hant/net/excel-worksheet-csharp-tutorials/add-excel-worksheet-to-existing-workbook-csharp-tutorial/
---
在本教程中，我們將逐步向您解釋下面的 C# 原始程式碼，有助於使用 Aspose.Cells for .NET 將新工作表新增至現有 Excel 工作簿。我們將為每個步驟提供範例程式碼，以幫助您詳細了解流程。

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

## 步驟 4：在工作簿新增工作表

若要將新工作表新增至工作簿中，您可以使用`Worksheets.Add()`的方法`Workbook`目的。此方法傳回新新增的工作表的索引。

```csharp
//將新工作表新增至 Workbook 工作簿
int i = workbook. Worksheets. Add();
```

## 第5步：設定新工作表名稱

您可以使用以下命令設定新新增的工作表的名稱`Name`的財產`Worksheet`目的。

```csharp
//透過傳遞sheet索引來取得新加入的sheet的引用
Worksheet worksheet = workbook.Worksheets[i];
//定義新工作表的名稱
worksheet.Name = "My Worksheet";
```

## 第 6 步：儲存 Excel 文件

新增工作表並設定其名稱後，您可以使用以下命令儲存修改後的 Excel 檔案：`Save()`的方法`Workbook`目的。

```csharp
//儲存 Excel 文件
workbook.Save(dataDir + "output.out.xls");
```

## 步驟7：關閉文件流並釋放資源

最後，關閉文件流以釋放與其關聯的所有資源非常重要。

```csharp
//關閉文件流以釋放所有資源
fstream.Close();
```

### 使用 Aspose.Cells for .NET 將 Excel 工作表新增至現有工作簿 C# 教學課程的範例原始程式碼 
```csharp
//文檔目錄的路徑。
string dataDir = "YOUR DOCUMENT DIRECTORY";
//建立包含要開啟的 Excel 檔案的檔案流
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
//實例化 Workbook 物件
//透過檔案流程開啟Excel文件
Workbook workbook = new Workbook(fstream);
//將新工作表新增至 Workbook 對象
int i = workbook.Worksheets.Add();
//透過傳遞工作表索引來取得新新增的工作表的引用
Worksheet worksheet = workbook.Worksheets[i];
//設定新新增的工作表名稱
worksheet.Name = "My Worksheet";
//儲存 Excel 文件
workbook.Save(dataDir + "output.out.xls");
//關閉文件流以釋放所有資源
fstream.Close();
```

## 結論

在本教學中，我們逐步介紹了使用 Aspose.Cells for .NET 將新的 Fire Connect 新增至現有 Excel 工作簿的過程。透過遵循提供的程式碼範例和說明，您現在應該很好地了解如何在 C# 應用程式中執行此任務。 Aspose.Cells for .NET 提供了一整套用於處理 Excel 檔案的功能，讓您能夠有效率地自動執行各種與 Excel 相關的任務。

### 常見問題 (FAQ)

#### 什麼是 Aspose.Cells for .NET？

Aspose.Cells for .NET 是一個功能強大的 .NET 程式庫，可讓開發人員在其應用程式中建立、操作和轉換 Excel 檔案。它提供了廣泛的功能來處理電子表格、儲存格、公式、樣式等。

#### 如何安裝 Aspose.Cells for .NET？

要安裝 Aspose.Cells for .NET，您可以從 Aspose Releases (https://releases.aspose.com/cells/net）並按照提供的安裝說明進行操作。您還需要有效的許可證才能在應用程式中使用該程式庫。

#### 我可以使用 Aspose.Cells for .NET 新增多個電子表格嗎？

是的，您可以使用 Aspose.Cells for .NET 將多個工作表新增至一個 Excel 檔案。您可以使用`Worksheets.Add()`的方法`Workbook`物件在工作簿中的不同位置新增工作表。

#### 如何設定 Excel 文件中儲存格的格式？

Aspose.Cells for .NET 提供了不同的方法和屬性來格式化 Excel 檔案中的儲存格。您可以設定儲存格值，套用格式選項，例如字型樣式、顏色、對齊方式、邊框等。有關單元格格式設定的更多詳細信息，請參閱 Aspose.Cells 提供的文件和範例程式碼。

#### Aspose.Cells for .NET 是否與不同版本的 Excel 相容？

是的，Aspose.Cells for .NET 與不同版本的Excel 相容，包括Excel 2003、Excel 2007、Excel 2010、Excel 2013、Excel 2016、Excel 2019 和Excel for Office 365。它支援.xls 格式和較新的. xls 格式。xlsx 格式。