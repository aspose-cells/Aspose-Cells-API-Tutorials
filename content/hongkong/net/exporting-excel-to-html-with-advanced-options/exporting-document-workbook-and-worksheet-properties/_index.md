---
title: 以 HTML 格式匯出文件工作簿和工作表屬性
linktitle: 以 HTML 格式匯出文件工作簿和工作表屬性
second_title: Aspose.Cells .NET Excel 處理 API
description: 了解如何使用 Aspose.Cells for .NET 將 Excel 文件、工作簿和工作表屬性匯出為 HTML。包括簡單的逐步指南。
type: docs
weight: 11
url: /zh-hant/net/exporting-excel-to-html-with-advanced-options/exporting-document-workbook-and-worksheet-properties/
---
## 介紹

在處理電子表格時，我們經常發現自己需要將 Excel 檔案轉換為不同的格式以進行共享、儲存或簡報。一項常見任務是將工作簿和工作表屬性匯出為 HTML 格式。在本文中，我們將引導您了解如何使用 Aspose.Cells for .NET 來完成此任務。如果您是編碼或 Aspose 庫的新手，請不要擔心；我們將逐步分解它以使其易於理解！

## 先決條件

在我們深入研究程式碼之前，讓我們確保您擁有開始使用所需的一切：

1. .NET Framework：確保您的開發環境已使用 .NET Framework 設定。 Aspose.Cells 與 .NET Framework 4.8 版本相容。
   
2.  Aspose.Cells for .NET：您需要安裝Aspose.Cells。您可以從以下位置下載該程式庫[下載頁面](https://releases.aspose.com/cells/net/). 

3. IDE：像 Visual Studio 這樣合適的整合開發環境 (IDE) 將簡化您的程式設計體驗。

4. 範例 Excel 檔案：出於測試目的，請確保您有一個名為`sampleExportDocumentWorkbookAndWorksheetPropertiesInHTML.xlsx`在你的工作目錄中。

## 導入包

現在我們已經介紹了先決條件，讓我們開始在 C# 專案中匯入必要的套件。您可以按照以下方法執行此操作：

### 建立一個新項目

- 開啟 IDE 並建立新的 C# 專案。您可以選擇一個控制台應用程序，它非常適合運行此類任務。

### 加入 Aspose.Cells NuGet 包

若要新增 Aspose.Cells 包，請依照下列步驟操作：

- 在解決方案資源管理器中以滑鼠右鍵按一下您的項目，然後選擇「管理 NuGet 套件」。
- 在 NuGet 套件管理器中，搜尋「Aspose.Cells」並安裝它。
- 該套件將提供處理 Excel 文件所需的類別和方法。

### 導入命名空間

在主程式檔案的頂部，請確保包含以下命名空間：

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
```

這將使我們能夠訪問`Workbook`和`HtmlSaveOptions`類，我們將在我們的範例中使用它。

現在您已完成所有設置，讓我們將過程分解為簡單的步驟。

## 第 1 步：設定檔案目錄

首先，我們需要指定輸入和輸出檔案的位置。在您的程式碼中，像這樣初始化目錄：

```csharp
//原始碼目錄
string sourceDir = "Your Document Directory/";  //更新為您的實際路徑

//輸出目錄
string outputDir = "Your Document Directory/";  //更新為您的實際路徑
```

- 來源目錄：這是您輸入的 Excel 檔案的位置（`sampleExportDocumentWorkbookAndWorksheetPropertiesInHTML.xlsx`) 被儲存。
- 輸出目錄：這是儲存輸出 HTML 檔案的路徑。

## 第 2 步：載入 Excel 文件

現在我們需要使用以下命令來載入 Excel 文件`Workbook`班級：

```csharp
//載入範例 Excel 文件
Workbook workbook = new Workbook(sourceDir + "sampleExportDocumentWorkbookAndWorksheetPropertiesInHTML.xlsx");
```

- 工作簿實例：`Workbook`建構函數會取得 Excel 檔案的檔案路徑並建立一個可以操作的新實例。

## 第 3 步：設定 HTML 儲存選項

接下來，我們指定如何將 Excel 資料儲存為 HTML：

```csharp
//指定 Html 儲存選項
HtmlSaveOptions options = new HtmlSaveOptions();

//防止匯出文件、工作簿和工作表屬性
options.ExportDocumentProperties = false;
options.ExportWorkbookProperties = false;
options.ExportWorksheetProperties = false;
```

- HtmlSaveOptions：此類協助管理如何將 Excel 檔案轉換為 HTML。
- 我們設定了幾個選項`false`因為我們不想在 HTML 輸出中包含工作簿和工作表屬性。

## 步驟 4：將所有內容匯出為 HTML

現在我們準備好將工作簿儲存為 HTML 格式：

```csharp
//使用 Html 儲存選項將 Excel 檔案匯出為 Html
workbook.Save(outputDir + "outputExportDocumentWorkbookAndWorksheetPropertiesInHTML.html", options);
```

- 這`Save`方法有兩個參數：輸出 HTML 檔案的檔案路徑和我們設定的選項。運行此命令將在指定的輸出目錄中建立 HTML 檔案。

## 第5步：控制台回饋

最後，讓我們在控制台中提供一些回饋，以了解該過程已成功完成：

```csharp
Console.WriteLine("ExportDocumentWorkbookAndWorksheetPropertiesInHTML executed successfully.");
```

## 結論

就像這樣，您已經使用 Aspose.Cells for .NET 成功將工作簿和工作表屬性匯出到 HTML！從設定環境到匯出 Excel 數據，您遵循了一個簡單的流程。使用 Aspose.Cells 等函式庫的優點在於它簡化了複雜的任務，讓開發人員的工作更輕鬆。現在，您可以使用 HTML 更廣泛地共享電子表格，就像讓全世界都可以查看您的工作簿，而無需向他們提供整本書。

## 常見問題解答

### 如何安裝 Aspose.Cells for .NET？  
您可以透過 NuGet 套件管理器在 Visual Studio 專案中透過 NuGet 安裝 Aspose.Cells 庫。

### 我可以自訂 HTML 輸出嗎？  
是的，Aspose.Cells 提供了各種選項`HtmlSaveOptions`自訂將 Excel 檔案轉換為 HTML 的方式。

### 有沒有辦法在 HTML 匯出中包含文件屬性？  
您可以設定`ExportDocumentProperties`, `ExportWorkbookProperties` ， 和`ExportWorksheetProperties`到`true`在`HtmlSaveOptions`如果你想包括它們。

### 除了 HTML 之外，我還可以將 Excel 檔案匯出為哪些格式？  
Aspose.Cells 支援多種格式，包括 PDF、CSV、XML 等。

### 有試用版嗎？  
是的，您可以從 Aspose.Cells 取得免費試用版[網站](https://releases.aspose.com/).