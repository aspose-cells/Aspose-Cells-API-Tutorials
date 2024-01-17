---
title: 控制工作表的縮放係數
linktitle: 控制工作表的縮放係數
second_title: Aspose.Cells for .NET API 參考
description: 使用 Aspose.Cells for .NET 控制 Excel 工作表的縮放係數。
type: docs
weight: 20
url: /zh-hant/net/excel-display-settings-csharp-tutorials/controll-zoom-factor-of-worksheet/
---
使用 .NET 的 Aspose.Cells 函式庫處理 Excel 檔案時，控制工作表的縮放係數是一項重要功能。在本指南中，我們將逐步向您展示如何使用 Aspose.Cells 使用 C# 原始碼控制工作表的縮放係數。

## 步驟1：導入所需的庫

在開始之前，請確保您已安裝適用於 .NET 的 Aspose.Cells 庫並將必要的庫匯入到您的 C# 專案中。

```csharp
using System;
using System.IO;
using Aspose.Cells;
```

## 步驟2：設定目錄路徑並開啟Excel文件

首先，設定包含 Excel 檔案的目錄的路徑，然後使用`FileStream`物件並實例化`Workbook`物件來表示 Excel 工作簿。

```csharp
string dataDir = "YOUR DOCUMENTS DIRECTORY";
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
Workbook workbook = new Workbook(fstream);
```

## 步驟 3：存取電子表格並更改縮放係數

在此步驟中，我們使用索引來存取 Excel 工作簿的第一個工作表`0`並將工作表縮放係數設為`75`.

```csharp
Worksheet worksheet = workbook.Worksheets[0];
worksheet. Zoom = 75;
```

## 步驟 4：儲存變更並關閉文件

更改工作表縮放係數後，我們使用以下命令將變更儲存到 Excel 檔案中：`Save`的方法`Workbook`目的。然後我們關閉文件流以釋放所有使用的資源。

```csharp
workbook.Save(dataDir + "output.xls");
fstream.Close();
```

### 使用 Aspose.Cells for .NET 控制工作表縮放係數的範例原始程式碼 

```csharp
//文檔目錄的路徑。
string dataDir = "YOUR DOCUMENT DIRECTORY";
//建立包含要開啟的 Excel 檔案的檔案流
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
//實例化 Workbook 物件
//透過檔案流程開啟Excel文件
Workbook workbook = new Workbook(fstream);
//存取 Excel 文件中的第一個工作表
Worksheet worksheet = workbook.Worksheets[0];
//將工作表的縮放係數設定為 75
worksheet.Zoom = 75;
//儲存修改後的Excel文件
workbook.Save(dataDir + "output.xls");
//關閉文件流以釋放所有資源
fstream.Close();
```

## 結論

本逐步指南向您展示如何使用 Aspose.Cells for .NET 控制工作表的縮放係數。使用提供的 C# 原始程式碼，您可以輕鬆調整 .NET 應用程式中工作表的縮放係數。

### 常見問題 (FAQ)

#### 什麼是 Aspose.Cells for .NET？

Aspose.Cells for .NET 是一個功能豐富的歸檔函式庫，用於在 .NET 應用程式中操作 Excel 檔案。

#### 如何安裝 Aspose.Cells for .NET？

要安裝Aspose.Cells for .NET，您需要從以下位置下載對應的NuGet包[Aspose 發布](https://releases/aspose.com/cells/net/)並將其新增至您的 .NET 專案。

#### Aspose.Cells for .NET 提供哪些功能？

Aspose.Cells for .NET 提供了 Excel 檔案的建立、編輯、轉換和進階操作等功能。

#### Aspose.Cells for .NET 支援哪些檔案格式？

Aspose.Cells for .NET 支援多種檔案格式，包括 XLSX、XLSM、CSV、HTML、PDF 等。
