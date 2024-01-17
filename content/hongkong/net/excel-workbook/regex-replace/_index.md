---
title: 正規表示式替換
linktitle: 正規表示式替換
second_title: Aspose.Cells for .NET API 參考
description: 了解如何使用 Aspose.Cells for .NET 在 Excel 檔案中執行正規表示式取代。
type: docs
weight: 140
url: /zh-hant/net/excel-workbook/regex-replace/
---
基於正規表示式 (Regex) 的文字替換是操作 Excel 檔案中的資料時的常見任務。使用 Aspose.Cells for .NET，您可以按照以下步驟輕鬆執行正規表示式取代：

## 步驟1：指定來源目錄和輸出目錄

首先，您必須指定包含要替換的資料的Excel檔案所在的來源目錄，以及要儲存修改後的檔案的輸出目錄。以下是使用 Aspose.Cells 執行此操作的方法：

```csharp
//來源目錄
string sourceDir = RunExamples.Get_SourceDirectory();

//輸出目錄
string outputDir = RunExamples.Get_OutputDirectory();
```

## 第 2 步：載入來源 Excel 文件

接下來，您需要載入要執行正規表示式替換的來源 Excel 檔案。操作方法如下：

```csharp
//載入來源 Excel 文件
Workbook workbook = new Workbook(sourceDir + "SampleRegexReplace.xlsx");
```

## 步驟 3：執行正規表示式替換

上傳檔案後，您可以設定替換選項，包括區分大小寫和精確的儲存格內容匹配。以下是執行正規表示式替換的範例程式碼：

```csharp
//設定替換選項
ReplaceOptions replace = new ReplaceOptions();
replace.CaseSensitive = false;
replace.MatchEntireCellContents = false;

//定義搜尋關鍵字為正規表示式
replace. RegexKey = true;

//執行正規表示式替換
workbook. Replace("\\bKIM\\b", "^^^TIM^^^", replace);
```

## 步驟 4：儲存輸出 Excel 文件

正規表示式替換完成後，您可以將修改後的Excel檔案儲存到指定的輸出目錄。操作方法如下：

```csharp
//儲存輸出的 Excel 文件
workbook.Save(outputDir + "RegexReplace_out.xlsx");
Console.WriteLine("RegexReplace executed successfully.\r\n");
```

### 使用 Aspose.Cells for .NET 進行 Regex Replace 的範例原始碼 
```csharp
//原始碼目錄
string sourceDir = RunExamples.Get_SourceDirectory();
//輸出目錄
string outputDir = RunExamples.Get_OutputDirectory();
Workbook workbook = new Workbook(sourceDir + "SampleRegexReplace.xlsx");
ReplaceOptions replace = new ReplaceOptions();
replace.CaseSensitive = false;
replace.MatchEntireCellContents = false;
//設定為 true 表示搜尋的鍵是正規表示式
replace.RegexKey = true;
workbook.Replace("\\bKIM\\b", "^^^TIM^^^", replace);
workbook.Save(outputDir + "RegexReplace_out.xlsx");
Console.WriteLine("RegexReplace executed successfully.");
```

## 結論

正規表示式替換是一種用於動態修改 Excel 檔案中資料的強大技術。使用 Aspose.Cells for .NET，您可以按照上述步驟輕鬆執行正規表示式取代。嘗試您自己的正規表示式並利用 Aspose.Cells 提供的靈活性。

### 常見問題解答

#### Q：什麼是正規表示式替換？
    
答：正規表示式替換是一種用於根據 Excel 檔案中的正規表示式取代文字模式的技術。這樣可以快速且準確地更改數據。

#### Q：正規表示式替換是否區分大小寫？
    
答：不，使用 Aspose.Cells，您可以指定正規表示式替換是否應區分大小寫。您可以完全控制此功能。

#### Q：替換正規表示式時如何指定儲存格內容的精確比對？
    
答：Aspose.Cells 可讓您定義正規表示式替換是否應與儲存格內容完全相符。您可以根據您的需求調整此選項。

#### Q：用 Aspose.Cells 取代 Regex 時可以使用進階正規表示式嗎？
    
答：是的，Aspose.Cells 支援進階正規表示式，讓您在 Excel 檔案中執行複雜的替換。

#### Q：如何檢查正規表示式替換是否成功？
    
答：執行正規表示式替換後，您可以透過檢查輸出並確保正確建立輸出 Excel 檔案來驗證操作是否成功。
	