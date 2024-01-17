---
title: 調整壓縮等級
linktitle: 調整壓縮等級
second_title: Aspose.Cells for .NET API 參考
description: 透過使用 Aspose.Cells for .NET 調整壓縮等級來減少 Excel 工作簿的大小。
type: docs
weight: 50
url: /zh-hant/net/excel-workbook/adjust-compression-level/
---
在本逐步教程中，我們將解釋提供的 C# 原始程式碼，它允許您使用 Aspose.Cells for .NET 調整壓縮等級。請依照下列步驟調整 Excel 工作簿中的壓縮等級。

## 第 1 步：設定來源目錄和輸出目錄

```csharp
//來源目錄
string sourceDir = RunExamples.Get_SourceDirectory();
//輸出目錄
string outDir = RunExamples.Get_OutputDirectory();
```

在第一步中，我們定義 Excel 檔案的來源目錄和輸出目錄。

## 第 2 步：載入 Excel 工作簿

```csharp
//載入 Excel 工作簿
Workbook workbook = new Workbook(sourceDir + "LargeSampleFile.xlsx");
```

我們使用以下命令從指定檔案載入 Excel 工作簿`Workbook`來自 Aspose.Cells 的類別。

## 第 3 步：設定備份選項

```csharp
//定義備份選項
XlsbSaveOptions options = new XlsbSaveOptions();
```

我們建立一個實例`XlsbSaveOptions`類別設定保存選項。

## 步驟 4：調整壓縮等級（等級 1）

```csharp
//調整壓縮等級（等級 1）
options.CompressionType = OoxmlCompressionType.Level1;
var watch = System.Diagnostics.Stopwatch.StartNew();
workbook.Save(outDir + "LargeSampleFile_level_1_out.xlsb", options);
watch.Stop();
let elapsedMs = watch.ElapsedMilliseconds;
Console.WriteLine("Elapsed time (Level 1): " + elapsedMs);
```

我們透過設定來調整壓縮級別`CompressionType`到`Level1`。然後，我們儲存指定此壓縮選項的 Excel 工作簿。

## 步驟 5：調整壓縮等級（等級 6）

```csharp
//調整壓縮等級（等級 6）
options.CompressionType = OoxmlCompressionType.Level6;
watch = System.Diagnostics.Stopwatch.StartNew();
workbook.Save(outDir + "LargeSampleFile_level_6_out.xlsb", options);
watch.Stop();
elapsedMs = watch. ElapsedMilliseconds;
Console.WriteLine("Elapsed time (Level 6): " + elapsedMs);
```

我們重複該過程以將壓縮等級調整為`Level6`並使用此選項儲存 Excel 工作簿。

## 第 6 步：調整壓縮等級（等級 9）

```csharp
//調整壓縮等級（9級）
options.CompressionType = OoxmlCompressionType.Level9;
watch = System.Diagnostics.Stopwatch.StartNew();
workbook.Save(outDir + "LargeSampleFile_level_9_out.xlsb", options);
watch.Stop();
elapsedMs = watch. ElapsedMilliseconds;
Console.WriteLine("Elapsed time (Level 9): " + elapsedMs);
```

我們最後一次重複這個過程，將壓縮等級調整為`Level9`並使用此選項儲存 Excel 工作簿。

### 使用 Aspose.Cells for .NET 調整壓縮等級的範例原始碼 
```csharp
//原始碼目錄
string sourceDir = RunExamples.Get_SourceDirectory();
string outDir = RunExamples.Get_OutputDirectory();
Workbook workbook = new Workbook(sourceDir + "LargeSampleFile.xlsx");
XlsbSaveOptions options = new XlsbSaveOptions();
options.CompressionType = OoxmlCompressionType.Level1;
var watch = System.Diagnostics.Stopwatch.StartNew();
workbook.Save(outDir + "LargeSampleFile_level_1_out.xlsb", options);
watch.Stop();
var elapsedMs = watch.ElapsedMilliseconds;
Console.WriteLine("Level 1 Elapsed Time: " + elapsedMs);
watch = System.Diagnostics.Stopwatch.StartNew();
options.CompressionType = OoxmlCompressionType.Level6;
workbook.Save(outDir + "LargeSampleFile_level_6_out.xlsb", options);
watch.Stop();
elapsedMs = watch.ElapsedMilliseconds;
Console.WriteLine("Level 6 Elapsed Time: " + elapsedMs);
watch = System.Diagnostics.Stopwatch.StartNew();
options.CompressionType = OoxmlCompressionType.Level9;
workbook.Save(outDir + "LargeSampleFile_level_9_out.xlsb", options);
watch.Stop();
elapsedMs = watch.ElapsedMilliseconds;
Console.WriteLine("Level 9 Elapsed Time: " + elapsedMs);
Console.WriteLine("AdjustCompressionLevel executed successfully.");
```

## 結論

恭喜！您學習如何使用 Aspose.Cells for .NET 調整 Excel 工作簿中的壓縮等級。嘗試不同的壓縮級別，找到最適合您需求的壓縮級別。

### 常見問題解答

#### Q：Excel 工作簿中的壓縮是什麼？

答：Excel 工作簿中的壓縮是使用壓縮演算法來減少檔案大小的過程。這減少了載入和操作檔案時所需的儲存空間並提高了效能。

#### Q：Aspose.Cells 提供什麼等級的壓縮？

答：使用Aspose.Cells，您可以將壓縮等級從1調整到9。壓縮等級越高，檔案大小越小，但也會增加處理時間。

#### Q：如何為 Excel 工作簿選擇正確的壓縮等級？

答：壓縮等級的選擇取決於您的特定需求。如果您想要最大壓縮並且處理時間不是問題，則可以選擇等級 9。如果您希望在檔案大小和處理時間之間進行折衷，則可以選擇中間層級。

#### Q：壓縮會影響 Excel 工作簿中的資料品質嗎？

答：不會，壓縮不會影響 Excel 工作簿中的資料品質。它只是使用壓縮技術來減小檔案大小，而不改變資料本身。

#### Q：儲存 Excel 檔案後可以調整壓縮等級嗎？

答：不可以，一旦您以特定的壓縮等級儲存 Excel 文件，您以後就無法調整壓縮等級。如果您想修改文件，則需要使用新的壓縮等級再次儲存該文件。