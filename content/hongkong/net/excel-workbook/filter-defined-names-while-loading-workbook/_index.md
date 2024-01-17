---
title: 載入工作簿時過濾定義的名稱
linktitle: 載入工作簿時過濾定義的名稱
second_title: Aspose.Cells for .NET API 參考
description: 了解如何在使用 Aspose.Cells for .NET 載入 Excel 工作簿時過濾定義的名稱。
type: docs
weight: 100
url: /zh-hant/net/excel-workbook/filter-defined-names-while-loading-workbook/
---
在 .NET 應用程式中使用 Excel 工作簿時，通常需要在載入時過濾資料。 Aspose.Cells for .NET 是一個功能強大的函式庫，可以輕鬆操作 Excel 工作簿。在本指南中，我們將向您展示如何過濾使用 Aspose.Cells for .NET 載入工作簿時定義的名稱。請按照以下簡單步驟即可獲得所需結果：

## 第 1 步：指定載入選項

首先，您需要指定載入選項來定義工作簿的載入行為。在我們的例子中，我們想要忽略載入時設定的名稱。以下是使用 Aspose.Cells 執行此操作的方法：

```csharp
//指定載入選項
LoadOptions opts = new LoadOptions();

//不載入定義的名稱
opts. LoadFilter = new LoadFilter(~LoadDataFilterOptions.DefinedNames);
```

## 第 2 步：載入工作簿

配置載入選項後，您可以從來源檔案載入 Excel 工作簿。請務必指定正確的檔案路徑。這是範例程式碼：

```csharp
//載入工作簿
Workbook wb = new Workbook(sourceDir + "sampleFilterDefinedNamesWhileLoadingWorkbook.xlsx", opts);
```

## 步驟 3：儲存篩選後的工作簿

載入工作簿後，您可以根據需要執行其他操作或編輯。然後，您可以將篩選後的工作簿儲存到輸出檔案中。就是這樣：

```csharp
//儲存篩選後的 Excel 工作簿
wb.Save(outputDir + "outputFilterDefinedNamesWhileLoadingWorkbook.xlsx");
```

### 使用 Aspose.Cells for .NET 載入工作簿時篩選定義名稱的範例原始程式碼 
```csharp
//指定載入選項
LoadOptions opts = new LoadOptions();
//我們不想載入定義的名稱
opts.LoadFilter = new LoadFilter(~LoadDataFilterOptions.DefinedNames);
//載入工作簿
Workbook wb = new Workbook(sourceDir + "sampleFilterDefinedNamesWhileLoadingWorkbook.xlsx", opts);
//儲存輸出Excel文件，它會破壞C1中的公式
wb.Save(outputDir + "outputFilterDefinedNamesWhileLoadingWorkbook.xlsx");
Console.WriteLine("FilterDefinedNamesWhileLoadingWorkbook executed successfully.");
```

## 結論

載入 Excel 工作簿時過濾定義的名稱對於許多應用程式來說至關重要。 Aspose.Cells for .NET 透過提供載入和過濾資料的靈活選項使這項任務變得更容易。透過遵循本指南中的步驟，您將能夠有效地過濾掉定義的名稱並在 Excel 工作簿中獲得所需的結果。


### 常見問題解答

#### Q：Aspose.Cells 是否支援 C# 以外的其他程式語言？
    
答：是的，Aspose.Cells是一個跨平台函式庫，支援Java、Python、C等多種程式語言++， 還有很多。

#### Q：使用 Aspose.Cells 載入工作簿時可以過濾其他資料類型嗎？
    
答：是的，Aspose.Cells 提供了一系列資料過濾選項，包括公式、樣式、巨集等。

#### Q：Aspose.Cells 是否保留原始工作簿的格式和屬性？
    
答：是的，在處理 Excel 檔案時，Aspose.Cells 會保留原始工作簿的格式、樣式、公式和其他屬性。