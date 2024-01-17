---
title: 保護 Excel 工作表
linktitle: 保護 Excel 工作表
second_title: Aspose.Cells for .NET API 參考
description: 在本教學中了解如何使用 Aspose.Cells for .NET 保護 Excel 電子表格。 C# 的逐步指南。
type: docs
weight: 50
url: /zh-hant/net/protect-excel-file/protect-excel-worksheet/
---
在本教學中，我們將查看一些使用 Aspose.Cells 函式庫來保護 Excel 電子表格的 C# 原始碼。我們將逐步完成程式碼的每個步驟並解釋其工作原理。請務必仔細按照說明進行操作，以獲得所需的結果。

## 第 1 步：先決條件

在開始之前，請確保您已安裝適用於 .NET 的 Aspose.Cells 庫。您可以從Aspose官方網站取得它。請同時確保您擁有最新版本的 Visual Studio 或任何其他 C# 開發環境。

## 步驟2：導入所需的命名空間

要使用 Aspose.Cells 函式庫，我們需要將必要的命名空間匯入到我們的程式碼中。將以下行新增至 C# 來源檔案的頂部：

```csharp
using Aspose.Cells;
using System.IO;
```

## 步驟 3：載入 Excel 文件

在此步驟中，我們將載入要保護的 Excel 檔案。請務必指定包含 Excel 檔案的目錄的正確路徑。使用以下程式碼上傳檔案：

```csharp
//文檔目錄的路徑。
string dataDir = "YOUR_DIRECTORY_OF_DOCUMENTS";

//建立包含要開啟的 Excel 檔案的檔案流。
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);

//實例化一個 Workbook 物件。
//透過文件流程開啟 Excel 文件。
Workbook excel = new Workbook(fstream);
```

一定要更換`"YOUR_DOCUMENTS_DIR"`與您的文件目錄的適當路徑。

## 第 4 步：存取電子表格

現在我們已經載入了 Excel 文件，我們可以存取第一個工作表。使用以下程式碼存取第一個工作表：

```csharp
//存取 Excel 文件中的第一個工作表。
Worksheet worksheet = excel.Worksheets[0];
```

## 步驟 5：保護工作表

在此步驟中，我們將使用密碼保護電子表格。使用以下程式碼來保護電子表格：

```csharp
//使用密碼保護工作表。
worksheet.Protect(ProtectionType.All, "YOUR_PASSWORD", null);
```

代替`"YOUR_PASSWORD"`以及您想要用來保護電子表格的密碼。

## 步驟6：保存修改後的Excel檔案現在我們已經保護了

é 電子表格，我們將以預設格式儲存修改後的 Excel 檔案。使用以下程式碼儲存Excel檔案：

```csharp
//以預設格式儲存修改後的 Excel 檔案。
excel.Save(dataDir + "output.out.xls", SaveFormat.Excel97To2003);
```

確保指定正確的路徑來儲存修改後的 Excel 檔案。

## 步驟7：關閉文件流

要釋放所有資源，我們需要關閉用於載入 Excel 檔案的檔案流。使用以下程式碼關閉檔案流：

```csharp
//關閉檔案流以釋放所有資源。
fstream.Close();
```

請務必將此步驟包含在程式碼末尾。


### 使用 Aspose.Cells for .NET 保護 Excel 工作表的範例原始程式碼 
```csharp
//文檔目錄的路徑。
string dataDir = "YOUR DOCUMENT DIRECTORY";
//建立包含要開啟的 Excel 檔案的檔案流
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
//實例化 Workbook 物件
//透過檔案流程開啟Excel文件
Workbook excel = new Workbook(fstream);
//存取 Excel 文件中的第一個工作表
Worksheet worksheet = excel.Worksheets[0];
//使用密碼保護工作表
worksheet.Protect(ProtectionType.All, "aspose", null);
//以預設格式儲存修改後的 Excel 文件
excel.Save(dataDir + "output.out.xls", SaveFormat.Excel97To2003);
//關閉文件流以釋放所有資源
fstream.Close();
```

## 結論

恭喜！您現在擁有 C# 原始程式碼，可讓您使用 .NET 的 Aspose.Cells 庫保護 Excel 電子表格。請務必仔細遵循這些步驟並根據您的特定需求自訂程式碼。

### 常見問題（常見問題）

#### 是否可以在一個 Excel 檔案中保護多個工作表？

答：是的，您可以透過對每個工作表重複步驟 4-6 來保護一個 Excel 檔案中的多個工作表。

#### 如何為授權使用者指定特定權限？

答：您可以使用由`Protect`方法為授權使用者指定特定權限。有關更多信息，請參閱 Aspose.Cells 文件。

#### 我可以使用密碼來保護 Excel 檔案本身嗎？

答：是的，您可以使用 Aspose.Cells 函式庫提供的其他方法對 Excel 檔案本身進行密碼保護。具體範例請參考文件。

#### Aspose.Cells 函式庫是否支援其他 Excel 檔案格式？

答：是的，Aspose.Cells 函式庫支援多種 Excel 檔案格式，包括 XLSX、XLSM、XLSB、CSV 等。