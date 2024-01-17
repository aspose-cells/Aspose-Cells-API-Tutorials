---
title: 適合 Excel 頁面選項
linktitle: 適合 Excel 頁面選項
second_title: Aspose.Cells for .NET API 參考
description: 了解如何使用 Aspose.Cells for .NET 自動調整 Excel 試算表中的頁面。
type: docs
weight: 30
url: /zh-hant/net/excel-page-setup/fit-to-excel-pages-options/
---
在本文中，我們將帶您逐步說明以下 C# 原始程式碼：使用 Aspose.Cells for .NET 適合 Excel 頁面選項。我們將使用 .NET 的 Aspose.Cells 函式庫來執行此操作。請依照以下步驟在 Excel 中配置適合頁面。

## 第 1 步：建立工作簿
第一步是建立工作簿。我們將實例化一個 Workbook 物件。以下是建立工作簿的程式碼：

```csharp
//文檔目錄的路徑
string dataDir = "YOUR_DIRECTORY_OF_DOCUMENTS";

//實例化 Workbook 物件
Workbook workbook = new Workbook();
```

## 第 2 步：訪問工作表
現在我們已經建立了工作簿，我們需要導航到第一個工作表。我們將使用索引 0 來存取第一張表。這是存取它的程式碼：

```csharp
//訪問工作簿中的第一個工作表
Worksheet worksheet = workbook.Worksheets[0];
```

## 第 3 步：設定適合頁面
在此步驟中，我們將配置對工作表頁面的調整。我們將使用`FitToPagesTall`和`FitToPagesWide`的屬性`PageSetup`物件來指定工作表的高度和寬度所需的頁數。這是代碼：

```csharp
//配置工作表高度的頁數
worksheet.PageSetup.FitToPagesTall = 1;

//配置工作表寬度的頁數
worksheet.PageSetup.FitToPagesWide = 1;
```

## 第 4 步：儲存工作簿
現在我們已經配置了適合頁面，我們可以儲存工作簿。我們將使用`Save`Workbook 物件的方法用於此目的。這是儲存工作簿的代碼：

```csharp
//儲存工作簿
workbook.Save(dataDir + "FitToPagesOptions_out.xls");
```

### 使用 Aspose.Cells for .NET 的適合 Excel 頁面選項的範例原始程式碼 
```csharp
//文檔目錄的路徑。
string dataDir = "YOUR DOCUMENT DIRECTORY";
//實例化 Workbook 物件
Workbook workbook = new Workbook();
//存取 Excel 文件中的第一個工作表
Worksheet worksheet = workbook.Worksheets[0];
//設定工作表長度所跨越的頁數
worksheet.PageSetup.FitToPagesTall = 1;
//設定工作表寬度所跨越的頁數
worksheet.PageSetup.FitToPagesWide = 1;
//儲存工作簿。
workbook.Save(dataDir + "FitToPagesOptions_out.xls");
```

## 結論
在本文中，我們學習如何使用 Aspose.Cells for .NET 在 Excel 中配置適合頁面的大小。我們完成了以下步驟：建立工作簿、存取工作表、配置適合頁面以及儲存工作簿。現在您可以使用這些知識將電子表格調整到所需的頁面。

### 常見問題解答

#### Q：如何安裝 Aspose.Cells for .NET？

答：要安裝 Aspose.Cells for .NET，您可以使用 Visual Studio 中的 NuGet 套件管理器。找到“Aspose.Cells”包並將其安裝到您的專案中。

#### Q：我可以同時調整頁面的高度和寬度嗎？

答：是的，您可以使用調整工作表的高度和寬度`FitToPagesTall`和`FitToPagesWide`特性。您可以為每個維度指定所需的頁數。

#### Q：如何自訂「適合頁面」選項？

答：除了指定頁數之外，您還可以自訂其他適合頁面的選項，例如工作表比例、紙張方向、邊距等。使用中可用的屬性`PageSetup`為此對象。

#### Q：我可以使用 Aspose.Cells for .NET 處理現有工作簿嗎？

答：是的，您可以使用 Aspose.Cells for .NET 開啟和編輯現有工作簿。您可以存取工作表、儲存格、公式、樣式和其他工作簿項目來執行各種操作。