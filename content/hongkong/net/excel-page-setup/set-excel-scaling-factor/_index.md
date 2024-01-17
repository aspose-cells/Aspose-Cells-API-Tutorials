---
title: 設定 Excel 縮放係數
linktitle: 設定 Excel 縮放係數
second_title: Aspose.Cells for .NET API 參考
description: 了解如何使用 Aspose.Cells for .NET 輕鬆操作 Excel 檔案並自訂縮放因子。
type: docs
weight: 180
url: /zh-hant/net/excel-page-setup/set-excel-scaling-factor/
---
在本指南中，我們將引導您了解如何使用 Aspose.Cells for .NET 在 Excel 試算表中設定縮放因子。請依照以下步驟完成此任務。

## 第一步：建構環境

確保您已設定開發環境並安裝 Aspose.Cells for .NET。您可以從Aspose官方網站下載最新版本的程式庫。

## 步驟2：導入所需的命名空間

在您的 C# 專案中，匯入必要的命名空間以使用 Aspose.Cells：

```csharp
using Aspose.Cells;
```

## 第三步：設定文檔目錄路徑

聲明一個`dataDir`變數來指定要儲存產生的 Excel 檔案的目錄的路徑：

```csharp
string dataDir = "YOUR_DIRECTORY_OF_DOCUMENTS";
```

一定要更換`"YOUR_DOCUMENT_DIRECTORY"`與系統上的正確路徑。

## 第 4 步：建立工作簿對象

實例化一個代表要建立的 Excel 工作簿的 Workbook 物件：

```csharp
Workbook workbook = new Workbook();
```

## 第 5 步：存取第一個工作表

使用下列程式碼導覽至 Excel 工作簿中的第一個工作表：

```csharp
Worksheet worksheet = workbook.Worksheets[0];
```

## 第 6 步：設定縮放係數

使用以下程式碼設定縮放因子：

```csharp
worksheet.PageSetup.Zoom = 100;
```

這裡我們將縮放因子設定為 100，這表示電子表格在列印時將以正常尺寸的 100% 顯示。

## 步驟 7：儲存 Excel 工作簿

若要使用定義的縮放係數儲存 Excel 工作簿，請使用`Save`Workbook物件的方法：

```csharp
workbook.Save(dataDir + "ScalingFactor_out.xls");
```

這會將 Excel 工作簿儲存在指定目錄中，檔案名稱為「ScalingFactor_out.xls」。

### 使用 Aspose.Cells for .NET 設定 Excel 縮放因子的範例原始程式碼 
```csharp
//文檔目錄的路徑。
string dataDir = "YOUR DOCUMENT DIRECTORY";
//實例化 Workbook 物件
Workbook workbook = new Workbook();
//存取 Excel 文件中的第一個工作表
Worksheet worksheet = workbook.Worksheets[0];
//將縮放因子設定為 100
worksheet.PageSetup.Zoom = 100;
//儲存工作簿。
workbook.Save(dataDir + "ScalingFactor_out.xls");
```

## 結論

恭喜！您已經學習如何使用 Aspose.Cells for .NET 在 Excel 電子表格中設定縮放因子。縮放係數可讓您在列印時調整電子表格的大小以獲得最佳顯示。

### 常見問題解答

#### 1. 如何使用 Aspose.Cells for .NET 在 Excel 試算表中設定縮放因子？

使用`Zoom`的財產`PageSetup`物件設定縮放因子。例如，`worksheet.PageSetup.Zoom = 100;`將縮放因子設定為 100%。

#### 2. 我可以根據需要自訂縮放比例嗎？

是的，您可以透過變更分配給`Zoom`財產。例如，`worksheet.PageSetup.Zoom = 75;`將縮放因子設定為 75%。

#### 3. 是否可以使用定義的縮放比例來保存Excel工作簿？

是的，您可以使用`Save`的方法`Workbook`物件以定義的縮放因子儲存 Excel 工作簿。