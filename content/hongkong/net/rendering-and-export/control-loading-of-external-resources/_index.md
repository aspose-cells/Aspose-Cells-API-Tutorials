---
title: 在 Aspose.Cells 中控制 Excel 中的外部資源到 PDF
linktitle: 在 Aspose.Cells 中控制 Excel 中的外部資源到 PDF
second_title: Aspose.Cells .NET Excel 處理 API
description: 透過我們易於遵循的指南，了解如何使用 Aspose.Cells for .NET 控制 Excel 到 PDF 轉換中的外部資源。
type: docs
weight: 12
url: /zh-hant/net/rendering-and-export/control-loading-of-external-resources/
---
## 介紹
在當今的數位時代，將 Excel 電子表格轉換為 PDF 文件是一項常見任務。無論是準備報告、財務數據還是簡報資料，您都希望確保您的 PDF 完全符合您的預期。 Aspose.Cells for .NET 是一個強大的函式庫，可讓您控制此轉換過程直到最後的細節，特別是在處理外部資源（例如 Excel 檔案附帶的映像）時。在本指南中，我們將深入探討如何在使用 Aspose.Cells 將 Excel 轉換為 PDF 的過程中控制外部資源。所以，拿起你最喜歡的飲料，讓我們開始吧！
## 先決條件
在我們深入討論細節之前，讓我們確保您擁有開始滾動所需的一切。這是一個快速清單：
1. Visual Studio 或任何與 .NET 相容的 IDE：您需要一個環境來編寫和測試程式碼。
2.  Aspose.Cells for .NET：如果您還沒有安裝它，請前往[Aspose下載](https://releases.aspose.com/cells/net/)頁面並取得最新版本。
3. C# 基礎知識：熟悉 C# 程式語言將會有所幫助。如果您對任何概念不確定，請隨時查找。
4. Excel 檔案範例：使用您想要轉換的任何外部資源準備一個 Excel 檔案。您可以使用提供的範例檔案“samplePdfSaveOptions_StreamProvider.xlsx”。
5. 用於測試的圖像檔案：這將在轉換過程中用作外部資源。映像檔“newPdfSaveOptions_StreamProvider.png”是一個很好的佔位符。
## 導入包
首先，您需要從 Aspose.Cells 庫匯入必要的命名空間。這對於存取其功能至關重要。確保在文件頂部添加以下 using 指令：
```csharp
using System.IO;
using System.Drawing;
using System.Drawing.Imaging;
using Aspose.Cells;
using Aspose.Cells.Drawing;
using Aspose.Cells.Rendering;
using System;
```
這些套件將提供執行任務所需的所有基本類別和方法。
## 第 1 步：建立您的串流提供者類
第一個任務是建立一個流提供者類別來實現`IStreamProvider`介面.這個類別將允許您控制外部資源的載入方式。
```csharp
class MyStreamProvider : IStreamProvider
{
    public void CloseStream(StreamProviderOptions options)
    {
        Debug.WriteLine("-----Close Stream-----");
    }
    public void InitStream(StreamProviderOptions options)
    {
        string sourceDir = "Your Document Directory";
        Debug.WriteLine("-----Init Stream-----");
        //讀取記憶體流中的新映像並將其分配給 Stream 屬性
        byte[] bts = File.ReadAllBytes(sourceDir + "newPdfSaveOptions_StreamProvider.png");
        MemoryStream ms = new MemoryStream(bts);
        options.Stream = ms;
    }
}
```
在本課程中：
- CloseStream：關閉流時將呼叫此方法。目前，我們只是編寫一條用於追蹤的調試訊息。
-  InitStream：這就是魔法開始的地方。在這裡，您將讀取外部圖像作為位元組數組，將其轉換為記憶體流，並將其分配給`options.Stream`財產。
## 第 2 步：設定來源目錄和輸出目錄
現在您的串流提供者已準備就緒，是時候確定您的 Excel 檔案所在的位置以及您想要儲存 PDF 的位置了。
```csharp
//原始碼目錄
string sourceDir = "Your Document Directory";
//輸出目錄
string outputDir = "Your Document Directory";
```
只需更換`"Your Document Directory"`與您的電腦上文件所在的實際路徑。保持文件井井有條是關鍵！
## 第 3 步：載入 Excel 文件
接下來，您將載入要從中建立 PDF 的 Excel 檔案。
```csharp
//載入包含外部映像的來源 Excel 文件
Workbook wb = new Workbook(sourceDir + "samplePdfSaveOptions_StreamProvider.xlsx");
```
我們正在使用`Workbook`來自 Aspose.Cells 的類，它代表您的 Excel 檔案。該檔案可以包含各種外部資源，例如您想要在轉換過程中控制的映像。
## 步驟 4：設定 PDF 儲存選項
在將工作簿儲存為 PDF 之前，我們先指定儲存方式。您可以根據您的要求調整這些選項。
```csharp
//指定 Pdf 儲存選項 - Stream Provider
PdfSaveOptions opts = new PdfSaveOptions();
opts.OnePagePerSheet = true; //將每張紙保存在新頁面上
```
在這裡，我們建立一個新實例`PdfSaveOptions`，它允許您自訂 PDF 的格式。這`OnePagePerSheet`選項可以方便地確保每個 Excel 工作表在最終的 PDF 中都有自己的頁面。
## 第 5 步：分配您的串流媒體供應商
設定 PDF 選項後，您需要告訴 Aspose 使用自訂流程提供者取得外部資源。
```csharp
wb.Settings.StreamProvider = new MyStreamProvider();
```
這條線連接你的`Workbook`實例與`MyStreamProvider`您之前建立的類別。這意味著每當轉換過程中遇到外部資源時，您的提供者都會按指定處理它們。
## 步驟 6：將工作簿另存為 PDF
一切設定完畢後，終於可以將 Excel 工作簿另存為 PDF 了。
```csharp
//將工作簿儲存為 PDF
wb.Save(outputDir + "outputPdfSaveOptions_StreamProvider.pdf", opts);
```
透過致電`Save`工作簿物件上的方法並傳入輸出目錄以及 PDF 選項，您就可以將 Excel 檔案轉換為格式精美的 PDF。
## 第七步：確認執行成功
總而言之，確認您的流程已成功總是令人高興的！
```csharp
Console.WriteLine("ControlLoadingOfExternalResourcesInExcelToPDF executed successfully.\r\n");
```
將成功訊息列印到控制台有助於讓您了解操作的狀態。在程式碼中包含這些小確認是一個好習慣。
## 結論
給你了！透過遵循這些簡單的步驟，您可以熟練地控制在使用 Aspose.Cells 將 Excel 轉換為 PDF 期間如何處理外部資源。這意味著您的文件現在可以準確地包含圖像和其他外部元素，確保每次都能獲得精美的最終產品。
## 常見問題解答
### 什麼是 Aspose.Cells？  
Aspose.Cells 是一個針對 .NET 開發人員的強大程式庫，可讓您建立、操作、轉換和呈現各種格式的 Excel 檔案。
### 如何下載 Aspose.Cells？  
您可以從以下位置下載最新版本的 Aspose.Cells[下載連結](https://releases.aspose.com/cells/net/).
### 可以免費試用 Aspose.Cells 嗎？  
是的！您可以透過造訪獲得免費試用[免費試用頁面](https://releases.aspose.com/).
### 在哪裡可以找到對 Aspose.Cells 的支援？  
對於任何與支援相關的疑問，您可以訪問[Aspose 支援論壇](https://forum.aspose.com/c/cells/9).
### 我如何獲得 Aspose.Cells 的臨時許可證？  
您可以申請臨時許可證[這裡](https://purchase.aspose.com/temporary-license/).