---
title: 在 Excel 中隨形狀旋轉文字
linktitle: 在 Excel 中隨形狀旋轉文字
second_title: Aspose.Cells .NET Excel 處理 API
description: 了解如何使用 Aspose.Cells for .NET 在 Excel 中旋轉具有形狀的文字。請按照此逐步指南進行完美的 Excel 演示。
type: docs
weight: 12
url: /zh-hant/net/excel-shape-text-modifications/rotate-text-shape-excel/
---
## 介紹
在 Excel 的世界中，視覺表示與資料本身同樣重要。無論您是製作報告還是設計動態儀表板，資訊的佈局方式都會極大地影響其可讀性和整體外觀。那麼，您是否曾經想過旋轉文字以使其與形狀時尚地對齊？你很幸運！在本教程中，我們將深入研究如何使用 Aspose.Cells for .NET 旋轉具有形狀的文本，確保您的電子表格不僅提供信息，而且給人留下深刻的印象。
## 先決條件
在開始之前，讓我們確保您已擁有所需的一切：
1. Visual Studio：確保您的電腦上安裝了 Visual Studio，因為我們將在其中編寫程式碼。
2.  Aspose.Cells for .NET：您需要 Aspose.Cells 函式庫。你可以[在這裡下載最新版本](https://releases.aspose.com/cells/net/)或免費試用[免費試用](https://releases.aspose.com/).
3. C# 基礎知識：熟悉 C# 和 .NET 環境將會有所幫助，儘管我們將引導您完成每一步。
4.  Excel 文件：一個範例 Excel 文件，我們稱之為`sampleRotateTextWithShapeInsideWorksheet.xlsx`，需要測試我們的程式碼。您應該將此文件放置在您可以輕鬆存取的目錄中。
一切都準備好了嗎？極好的！讓我們進入有趣的部分。
## 導入包
首先，我們需要將必要的套件匯入到我們的專案中。操作方法如下：
### 建立一個新項目
1. 打開視覺工作室。
2. 選擇“建立新項目”。
3. 選擇“控制台應用程式”並選擇 C# 作為您的首選程式語言。
### 安裝 Aspose.Cells
現在，讓我們將 Aspose.Cells 加入您的專案中。您可以使用 NuGet 套件管理器執行此操作：
1. 開啟頂部選單中的「工具」。
2. 選擇“NuGet 套件管理器”，然後選擇“管理解決方案的 NuGet 套件”。
3. 搜尋“Aspose.Cells”。
4. 點擊“安裝”將其添加到您的專案中。
### 新增使用指令
在主 C# 檔案的頂部，您需要新增以下指令：
```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using Aspose.Cells.Drawing;
```
現在我們已經準備好開始編碼了！
讓我們將這個過程分解為易於理解的步驟。以下是如何在 Excel 檔案中旋轉帶有形狀的文字：
## 第 1 步：設定目錄路徑
首先，您需要設定用於儲存 Excel 檔案的來源目錄和輸出目錄。方法如下：
```csharp
//原始碼目錄
string sourceDir = "Your Document Directory"; //設定您的文檔目錄
//輸出目錄
string outputDir = "Your Document Directory"; //設定你的輸出目錄
```
代替`"Your Document Directory"`與你的實際路徑`sampleRotateTextWithShapeInsideWorksheet.xlsx`文件位於。
## 第 2 步：載入範例 Excel 文件
現在，讓我們載入範例 Excel 檔案。這至關重要，因為我們想要操縱現有數據。
```csharp
//載入範例 Excel 檔案。
Workbook wb = new Workbook(sourceDir + "sampleRotateTextWithShapeInsideWorksheet.xlsx");
```
## 第 3 步：訪問工作表
載入檔案後，我們需要存取要修改的特定工作表。在我們的例子中，這是第一個工作表。
```csharp
//訪問第一個工作表。
Worksheet ws = wb.Worksheets[0];
```
## 第 4 步：修改儲存格
接下來，我們將修改特定單元格以顯示訊息。在我們的範例中，我們將使用儲存格 B4。
```csharp
//存取儲存格 B4 並在其中新增一則訊息。
Cell b4 = ws.Cells["B4"];
b4.PutValue("Text is not rotating with shape because RotateTextWithShape is false.");
```
這一步主要是為了溝通——確保打開此表的人都了解我們正在調整的內容。
## 第 5 步：存取第一個形狀
要旋轉文本，我們需要一個可以使用的形狀。在這裡，我們將存取工作表中的第一個形狀。
```csharp
//存取第一個形狀。
Shape sh = ws.Shapes[0];
```
## 第 6 步：調整形狀文字對齊方式
這就是奇蹟發生的地方。我們將調整形狀的文字對齊屬性。
```csharp
//存取形狀文字對齊方式。
Aspose.Cells.Drawing.Texts.ShapeTextAlignment shapeTextAlignment = sh.TextBody.TextAlignment;
//將 RotateTextWithShape 設定為 false，不要隨形狀旋轉文字。
shapeTextAlignment.RotateTextWithShape = false;
```
透過設定`RotateTextWithShape`當設定為 false 時，我們確保文字保持直立且不隨形狀旋轉，從而保持一切整潔有序。
## 第 7 步：儲存輸出 Excel 文件
最後，將變更儲存到新的 Excel 檔案。這可以確保我們不會丟失編輯內容並獲得整潔的輸出。
```csharp
//儲存輸出的 Excel 檔案。
wb.Save(outputDir + "outputRotateTextWithShapeInsideWorksheet.xlsx");
```
就是這樣！您的輸出檔案現已儲存，包括儲存格 B4 中的文字以及對形狀所做的調整。
## 第8步：執行程式碼
在你的`Main`方法，包裝上述所有程式碼片段，然後運行您的專案。查看輸出文件中反映的更改！
```csharp
Console.WriteLine("RotateTextWithShapeInsideWorksheet executed successfully.");
```
## 結論
使用 Aspose.Cells for .NET 在 Excel 中旋轉帶有形狀的文字乍一看似乎是一個複雜的過程，但一旦分解它就會非常簡單。透過執行這些簡單的步驟，您可以自訂電子表格，使其看起來更專業且更具視覺吸引力。現在，無論您是為客戶還是個人專案做這件事，每個人都會對您的工作品質讚不絕口！
## 常見問題解答
### 我可以免費使用 Aspose.Cells 嗎？
是的！您可以使用[免費試用](https://releases.aspose.com/)嘗試圖書館。
### Aspose.Cells 支援哪些版本的 Excel？
Aspose.Cells 支援多種 Excel 格式，包括 XLS、XLSX、CSV 等。
### 是否可以在舊版 Excel 中旋轉具有形狀的文字？
是的，該功能可以應用於 Aspose.Cells 支援的舊格式。
### 在哪裡可以找到有關 Aspose.Cells 的更多文件？
您可以探索全面的[文件](https://reference.aspose.com/cells/net/)以獲得更多見解。
### 我如何獲得 Aspose.Cells 的支援？
您可以透過訪問尋求支持[Aspose論壇](https://forum.aspose.com/c/cells/9).