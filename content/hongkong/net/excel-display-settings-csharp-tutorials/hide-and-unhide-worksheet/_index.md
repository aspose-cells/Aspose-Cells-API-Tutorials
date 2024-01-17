---
title: 隱藏和取消隱藏工作表
linktitle: 隱藏和取消隱藏工作表
second_title: Aspose.Cells for .NET API 參考
description: 用於處理 Excel 檔案的功能強大的程式庫，包括建立、修改和操作資料。
type: docs
weight: 90
url: /zh-hant/net/excel-display-settings-csharp-tutorials/hide-and-unhide-worksheet/
---
在本教程中，我們將逐步向您解釋以下 C# 原始程式碼，該程式碼用於使用 Aspose.Cells for .NET 隱藏和顯示工作表。請依照以下步驟操作：

## 第一步：準備環境

在開始之前，請確保您的系統上安裝了 Aspose.Cells for .NET。如果您還沒有安裝，可以從 Aspose 官方網站下載。安裝後，您可以在您首選的整合開發環境 (IDE) 中建立新專案。

## 步驟2：導入所需的命名空間

在您的 C# 原始檔中，新增必要的命名空間以使用 Aspose.Cells 的功能。將以下行新增至文件的開頭：

```csharp
using Aspose.Cells;
using System.IO;
```

## 步驟 3：載入 Excel 文件

在隱藏或取消隱藏工作表之前，必須將 Excel 檔案載入到應用程式中。確保您要使用的 Excel 檔案與您的專案位於同一目錄中。使用以下程式碼載入 Excel 檔案：

```csharp
string dataDir = "PATH TO YOUR DOCUMENTS DIRECTORY";
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
Workbook workbook = new Workbook(fstream);
```

請務必將「PATH TO YOUR DOCUMENTS DIRECTORY」替換為包含 Excel 檔案的目錄的實際路徑。

## 第 4 步：存取電子表格

載入 Excel 檔案後，您可以導覽至要隱藏或取消隱藏的工作表。使用以下程式碼存取文件中的第一個工作表：

```csharp
Worksheet worksheet = workbook.Worksheets[0];
```

## 第 5 步：隱藏工作表

現在您已經造訪了工作表，您可以使用`IsVisible`財產。使用以下程式碼隱藏檔案中的第一個工作表：

```csharp
worksheet. IsVisible = false;
```

## 第 6 步：重新顯示工作表

如果要重新顯示先前隱藏的工作表，可以使用相同的程式碼，透過更改`IsVisible`財產。使用以下程式碼重新顯示第一個工作表：

```csharp
worksheet. IsVisible = true;
```

## 第 7 步：儲存更改

一旦您

  根據需要隱藏或取消隱藏工作表後，您必須將變更儲存到 Excel 檔案。使用以下程式碼儲存變更：

```csharp
workbook.Save(dataDir + "output.out.xls");
fstream.Close();
```

確保指定正確的輸出路徑來儲存修改後的 Excel 檔案。

### 使用 Aspose.Cells for .NET 隱藏和取消隱藏工作表的範例原始程式碼 

```csharp
//文檔目錄的路徑。
string dataDir = "YOUR DOCUMENT DIRECTORY";
//建立包含要開啟的 Excel 檔案的檔案流
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
//透過檔案流開啟 Excel 檔案來實例化 Workbook 對象
Workbook workbook = new Workbook(fstream);
//存取 Excel 文件中的第一個工作表
Worksheet worksheet = workbook.Worksheets[0];
//隱藏 Excel 檔案的第一個工作表
worksheet.IsVisible = false;
//顯示 Excel 檔案的第一張工作表
//工作表.IsVisible = true;
//以預設（即 Excel 2003）格式儲存修改後的 Excel 文件
workbook.Save(dataDir + "output.out.xls");
//關閉文件流以釋放所有資源
fstream.Close();
```

## 結論

恭喜！您已經學習如何使用 Aspose.Cells for .NET 隱藏和顯示電子表格。現在您可以使用此功能來控制 Excel 檔案中電子表格的可見性。

### 常見問題 (FAQ)

#### 如何安裝 Aspose.Cells for .NET？

您可以透過下載相關的 NuGet 套件來安裝 Aspose.Cells for .NET[Aspose 發布](https://releases/aspose.com/cells/net/)並將其新增至您的 Visual Studio 專案。

#### 使用 Aspose.Cells for .NET 所需的最低 .NET Framework 版本是多少？

Aspose.Cells for .NET 支援.NET Framework 2.0 及更高版本。

#### 我可以使用 Aspose.Cells for .NET 開啟和編輯現有的 Excel 檔案嗎？

是的，您可以使用 Aspose.Cells for .NET 開啟和編輯現有的 Excel 檔案。您可以存取 Excel 檔案的工作表、儲存格、公式和其他元素。

#### Aspose.Cells for .NET 支援報表和匯出為其他檔案格式嗎？

是的，Aspose.Cells for .NET 支援報告產生和匯出為 PDF、HTML、CSV、TXT 等格式。

#### Excel檔案的修改是永久性的嗎？

是的，儲存後，Excel 文件的編輯將是永久性的。在對原始文件進行任何更改之前，請務必儲存備份副本。