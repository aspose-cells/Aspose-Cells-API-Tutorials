---
title: 設定 Excel 頁首和頁尾
linktitle: 設定 Excel 頁首和頁尾
second_title: Aspose.Cells for .NET API 參考
description: 了解如何使用 Aspose.Cells for .NET 在 Excel 中設定頁首和頁尾。
type: docs
weight: 100
url: /zh-hant/net/excel-page-setup/set-excel-headers-and-footers/
---

在本教學中，我們將逐步向您展示如何使用 Aspose.Cells for .NET 在 Excel 中設定頁首和頁尾。我們將使用 C# 原始程式碼來說明該過程。

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
Workbook excel = new Workbook();
PageSetup pageSetup = excel.Worksheets[0].PageSetup;
```

這將建立一個帶有工作表的空白工作簿，並提供對該工作表的 PageSetup 物件的存取。

## 第5步：設定標題

使用以下命令設定電子表格標題`SetHeader`PageSetup 物件的方法。這是範例程式碼：

```csharp
pageSetup.SetHeader(0, "&A");
pageSetup.SetHeader(1, "&\"Times New Roman,Bold\"&D-&T");
pageSetup.SetHeader(2, "&\"Times New Roman,Bold\"&12&F");
```

這將分別在標題中設定工作表名稱、當前日期和時間以及檔案名稱。

## 第 6 步：定義頁腳

使用設定電子表格頁腳`SetFooter`PageSetup 物件的方法。這是範例程式碼：

```csharp
pageSetup.SetFooter(0, "Hello World! &\"Courier New\"&14 123");
pageSetup.SetFooter(1, "&P");
pageSetup.SetFooter(2, "&N");
```

這將分別在頁腳中設定文字字串、當前頁碼和總頁數。

## 步驟7：儲存修改後的工作簿

使用以下程式碼儲存修改後的工作簿：

```csharp
excel.Save(dataDir + "OutputFileName.xls");
```

這會將修改後的工作簿儲存到指定的資料目錄。

### 使用 Aspose.Cells for .NET 設定 Excel 頁首和頁尾的範例原始碼 
```csharp
//文檔目錄的路徑。
string dataDir = "YOUR DOCUMENT DIRECTORY";
//實例化 Workbook 物件
Workbook excel = new Workbook();
//取得工作表PageSetup的引用
PageSetup pageSetup = excel.Worksheets[0].PageSetup;
//在標題左側設定工作表名稱
pageSetup.SetHeader(0, "&A");
//在標題的中央部分設定當前日期和當前時間
//並更改標題的字體
pageSetup.SetHeader(1, "&\"Times New Roman,Bold\"&D-&T");
//在標題的右側設定目前檔案名稱並更改
//標題的字體
pageSetup.SetHeader(2, "&\"Times New Roman,Bold\"&12&F");
//在頁腳左側設定字串並更改字體
//該字串的一部分（“123”）
pageSetup.SetFooter(0, "Hello World! &\"Courier New\"&14 123");
//在頁腳的中央部分設定目前頁碼
pageSetup.SetFooter(1, "&P");
//在頁腳右側設定頁數
pageSetup.SetFooter(2, "&N");
//儲存工作簿。
excel.Save(dataDir + "SetHeadersAndFooters_out.xls");
```


## 結論

現在您已經了解如何使用 Aspose.Cells for .NET 在 Excel 中設定頁首和頁尾。本教學將引導您完成流程的每一步，從設定環境到儲存修改後的工作簿。請隨意進一步探索 Aspose.Cells 的功能，以在 Excel 檔案中執行進一步的操作。

### 常見問題 (FAQ)

#### 1. 如何在我的系統上安裝 Aspose.Cells for .NET？
要安裝Aspose.Cells for .NET，您需要從Aspose官方網站下載安裝包並按照文件中提供的說明進行操作。

#### 2. 這個方法適用於所有版本的Excel嗎？
是的，使用 Aspose.Cells for .NET 設定頁首和頁尾的方法適用於所有支援的 Excel 版本。

#### 3. 我可以進一步自訂頁首和頁尾嗎？
是的，Aspose.Cells 提供了廣泛的功能來自訂頁首和頁腳，包括文字位置、顏色、字體、頁碼等。

#### 4. 如何為頁首和頁尾新增動態資訊？
您可以使用特殊變數和格式化程式碼將動態資訊（例如當前日期、時間、檔案名稱、頁碼等）新增至頁首和頁尾。

#### 5. 設定頁首和頁尾後可以刪除嗎？
是的，您可以使用以下命令刪除頁首和頁尾`ClearHeaderFooter`的方法`PageSetup`目的。這將恢復預設的頁首和頁尾。