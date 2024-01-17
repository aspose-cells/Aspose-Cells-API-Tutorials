---
title: 刪除工作表的現有印表機設置
linktitle: 刪除工作表的現有印表機設置
second_title: Aspose.Cells for .NET API 參考
description: 了解如何使用 Aspose.Cells for .NET 從 Excel 電子表格中刪除現有印表機設定。
type: docs
weight: 80
url: /zh-hant/net/excel-page-setup/remove-existing-printer-settings-of-worksheets/
---
在本教學中，我們將逐步引導您了解如何使用 Aspose.Cells for .NET 從 Excel 工作表中移除現有印表機設定。我們將使用 C# 原始程式碼來說明該過程。

## 第一步：建構環境

請確定您的電腦上安裝了 Aspose.Cells for .NET。也可以在您首選的開發環境中建立一個新專案。

## 第二步：導入必要的函式庫

在您的程式碼檔案中，匯入使用 Aspose.Cells 所需的程式庫。這是對應的程式碼：

```csharp
using Aspose.Cells;
```

## 步驟 3：設定來源目錄和輸出目錄

分別設定原始 Excel 檔案所在的來源目錄和輸出目錄以及要儲存修改後的檔案的位置。使用以下程式碼：

```csharp
string sourceDir = "SOURCE DIRECTORY PATH";
string outputDir = "OUTPUT DIRECTORY PATH";
```

請務必指定完整目錄路徑。

## 第 4 步：載入來源 Excel 文件

使用以下程式碼載入來源 Excel 檔案：

```csharp
Workbook wb = new Workbook(sourceDir + "fileName.xlsx");
```

這會將指定的 Excel 檔案載入到 Workbook 物件中。

## 第 5 步：瀏覽工作表

使用循環遍歷工作簿中的所有工作表。使用以下程式碼：

```csharp
int sheetCount = wb. Worksheets. Count;

for (int i = 0; i < sheetCount; i++)
{
     Worksheet ws = wb.Worksheets[i];
     //其餘程式碼將在下一步中新增。
}
```

## 步驟 6：刪除現有印表機設置

檢查每個工作表是否有印表機設置，並在必要時將其刪除。使用以下程式碼：

```csharp
PageSetup ps = ws.PageSetup;

if (ps.PrinterSettings != null)
{
     Console.WriteLine("Printer settings for this spreadsheet exist.");
     Console.WriteLine("Sheet name: " + ws.Name);
     Console.WriteLine("Paper size: " + ps.PaperSize);

     ps.PrinterSettings = null;

     Console.WriteLine("Printer settings for this spreadsheet have been removed by setting them to null.");
     Console.WriteLine("");
}
```

## 步驟7：儲存修改後的工作簿

使用以下程式碼儲存修改後的工作簿：

```csharp
wb.Save(outputDir + "modifiedFilename.xlsx");
```

這會將修改後的工作簿儲存到指定的輸出目錄。

### 使用 Aspose.Cells for .NET 刪除工作表的現有印表機設定的範例原始碼 
```csharp
//原始碼目錄
string sourceDir = RunExamples.Get_SourceDirectory();
//輸出目錄
string outputDir = RunExamples.Get_OutputDirectory();
//載入來源 Excel 文件
Workbook wb = new Workbook(sourceDir + "sampleRemoveExistingPrinterSettingsOfWorksheets.xlsx");
//取得工作簿的頁數
int sheetCount = wb.Worksheets.Count;
//迭代所有工作表
for (int i = 0; i < sheetCount; i++)
{
    //造訪第 i 個工作表
    Worksheet ws = wb.Worksheets[i];
    //造訪工作表頁面設定
    PageSetup ps = ws.PageSetup;
    //檢查此工作表的印表機設定是否存在
    if (ps.PrinterSettings != null)
    {
        //列印以下訊息
        Console.WriteLine("PrinterSettings of this worksheet exist.");
        //列印紙張名稱及其紙張尺寸
        Console.WriteLine("Sheet Name: " + ws.Name);
        Console.WriteLine("Paper Size: " + ps.PaperSize);
        //透過將印表機設定設為空白來刪除它們
        ps.PrinterSettings = null;
        Console.WriteLine("Printer settings of this worksheet are now removed by setting it null.");
        Console.WriteLine("");
    }//如果
}//為了
//儲存工作簿
wb.Save(outputDir + "outputRemoveExistingPrinterSettingsOfWorksheets.xlsx");
```

## 結論

現在您已經了解如何使用 Aspose.Cells for .NET 從 Excel 中的工作表中刪除現有印表機設定。本教學將引導您完成流程的每一步，從設定環境到瀏覽電子表格和清除印表機設定。現在您可以使用這些知識來管理 Excel 檔案中的印表機設定。

### 常見問題解答

#### 問題 1：我如何知道電子表格是否有現有的印表機設定？

 A1：您可以透過存取工作表來檢查工作表是否有印表機設定`PrinterSettings`的財產`PageSetup`目的。如果該值非空，則表示存在現有的印表機設定。

#### 問題 2：我可以只刪除特定電子表格的印表機設定嗎？

 A2：是的，您可以使用相同的方法透過存取特定工作表的印表機設定來刪除該工作表的印表機設定。`PageSetup`目的。

#### Q3：此方法是否也會刪除其他佈局設定？

A3：不，此方法僅刪除印表機設定。其他佈局設置，例如邊距、紙張方向等保持不變。

#### 問題 4：此方法是否適用於所有 Excel 檔案格式，例如 .xls 和 .xlsx？

A4：是的，此方法適用於 Aspose.Cells 支援的所有 Excel 檔案格式，包括 .xls 和 .xlsx。

#### 問題 5：對印表機設定所做的變更會永久保留在編輯的 Excel 檔案中嗎？

A5：是的，印表機設定的變更會永久儲存在編輯的 Excel 檔案中。