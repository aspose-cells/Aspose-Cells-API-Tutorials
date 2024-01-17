---
title: 設定 Excel 首頁頁碼
linktitle: 設定 Excel 首頁頁碼
second_title: Aspose.Cells for .NET API 參考
description: 了解如何使用 Aspose.Cells for .NET 在 Excel 中設定首頁頁碼。
type: docs
weight: 90
url: /zh-hant/net/excel-page-setup/set-excel-first-page-number/
---
在本教學中，我們將引導您了解如何使用 Aspose.Cells for .NET 在 Excel 中設定首頁頁碼。我們將使用 C# 原始程式碼來說明該過程。

## 第一步：建構環境

請確定您的電腦上安裝了 Aspose.Cells for .NET。也可以在您首選的開發環境中建立一個新專案。

## 第二步：導入必要的函式庫

在您的程式碼檔案中，匯入使用 Aspose.Cells 所需的程式庫。這是對應的程式碼：

```csharp
using Aspose.Cells;
```

## 第三步：設定資料目錄

設定要儲存修改後的 Excel 檔案的資料目錄。使用以下程式碼：

```csharp
string dataDir = "YOUR DATA DIRECTORY";
```

請務必指定完整的目錄路徑。

## 步驟 4：建立工作簿和工作表

建立一個新的 Workbook 物件並使用以下程式碼導覽至工作簿中的第一個工作表：

```csharp
Workbook workbook = new Workbook();
Worksheet worksheet = workbook.Worksheets[0];
```

這將建立一個帶有工作表的空白工作簿。

## 第五步：設定首頁頁碼

使用以下程式碼設定工作表第一頁的頁碼：

```csharp
worksheet.PageSetup.FirstPageNumber = 2;
```

這會將首頁頁碼設定為 2。

## 步驟6：儲存修改後的工作簿

使用以下程式碼儲存修改後的工作簿：

```csharp
workbook.Save(dataDir + "OutputFileName.xls");
```

這會將修改後的工作簿儲存到指定的資料目錄。

### 使用 Aspose.Cells for .NET 設定 Excel 第一頁碼的範例原始碼 
```csharp
//文檔目錄的路徑。
string dataDir = "YOUR DOCUMENT DIRECTORY";
//實例化 Workbook 物件
Workbook workbook = new Workbook();
//存取 Excel 文件中的第一個工作表
Worksheet worksheet = workbook.Worksheets[0];
//設定工作表頁面的首頁頁碼
worksheet.PageSetup.FirstPageNumber = 2;
//儲存工作簿。
workbook.Save(dataDir + "SetFirstPageNumber_out.xls");
```

## 結論

現在您已經了解如何使用 Aspose.Cells for .NET 在 Excel 中設定首頁頁碼。本教學將引導您完成流程的每一步，從設定環境到設定首頁頁碼。現在，您可以使用這些知識來自訂 Excel 檔案中的頁碼。

### 常見問題解答

#### Q1：我可以為每個工作表設定不同的首頁頁碼嗎？

 A1：是的，您可以透過造訪為每個工作表設定不同的首頁頁碼`FirstPageNumber`各自工作表的屬性`PageSetup`目的。

#### Q2：如何查看現有電子表格的首頁頁碼？

 A2：您可以透過存取查看現有工作表的首頁頁碼`FirstPageNumber`的財產`PageSetup`與該工作表對應的物件。

#### Q3：頁碼預設都是從1開始嗎？

A3：是的，Excel 中頁碼預設從 1 開始。但是，您可以使用本教學中顯示的程式碼來設定不同的首頁頁碼。

#### 問題 4：首頁頁碼的變更會永久保留在編輯的 Excel 檔案中嗎？

A4：是的，對首頁頁碼所做的變更將永久保存在修改後的 Excel 檔案中。

#### Q5：此方法適用於所有 Excel 檔案格式，例如 .xls 和 .xlsx 嗎？

A5：是的，此方法適用於 Aspose.Cells 支援的所有 Excel 檔案格式，包括 .xls 和 .xlsx。