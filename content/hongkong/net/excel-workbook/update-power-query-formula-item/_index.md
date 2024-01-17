---
title: 更新 Power Query 公式項
linktitle: 更新 Power Query 公式項
second_title: Aspose.Cells for .NET API 參考
description: 了解如何使用 Aspose.Cells for .NET 更新 Excel 檔案中的 Power Query 公式元素。
type: docs
weight: 160
url: /zh-hant/net/excel-workbook/update-power-query-formula-item/
---
更新 Power Query 公式項目是處理 Excel 檔案中的資料時的常見操作。使用 Aspose.Cells for .NET，您可以依照下列步驟輕鬆更新 Power Query 公式項目：

## 第 1 步：指定來源目錄和輸出目錄

首先，您需要指定包含要更新的 Power Query 公式的 Excel 檔案所在的來源目錄，以及要儲存修改後的檔案的輸出目錄。以下是使用 Aspose.Cells 執行此操作的方法：

```csharp
//來源目錄
string SourceDir = RunExamples.Get_SourceDirectory();

//輸出目錄
string outputDir = RunExamples.Get_OutputDirectory();
```

## 步驟 2：載入來源 Excel 工作簿

接下來，您需要載入要更新 Power Query 公式項目的來源 Excel 工作簿。操作方法如下：

```csharp
//載入來源 Excel 工作簿
Workbook workbook = new Workbook(SourceDir + "SamplePowerQueryFormula.xlsx");
```

## 步驟 3：瀏覽並更新 Power Query 公式項

載入工作簿後，您可以導覽至 Power Query 公式集合併瀏覽每個公式及其元素。在此範例中，我們正在尋找名稱為“Source”的公式項目並更新其值。以下是更新 Power Query 公式項目的範例程式碼：

```csharp
//造訪 Power Query 公式集合
DataMashup mashupData = workbook.DataMashup;

//循環存取 Power Query 公式及其元素
foreach(PowerQueryFormula formula in mashupData.PowerQueryFormulas)
{
     foreach(PowerQueryFormulaItem item in formula.PowerQueryFormulaItems)
     {
         if (item.Name == "Source")
         {
             item.Value = "Excel.Workbook(File.Contents(\"" + SourceDir + "SamplePowerQueryFormulaSource.xlsx\"), null, true)";
         }
     }
}
```

## 步驟 4：儲存輸出的 Excel 工作簿

更新 Power Query 公式項目後，您可以將修改後的 Excel 工作簿儲存到指定的輸出目錄。操作方法如下：

```csharp
//儲存輸出的 Excel 工作簿
workbook.Save(outputDir + "SamplePowerQueryFormula_out.xlsx");
Console.WriteLine("UpdatePowerQueryFormulaItem executed successfully.\r\n");
```

### 使用 Aspose.Cells for .NET 更新 Power Query 公式項目的範例原始程式碼 
```csharp
//工作目錄
string SourceDir = RunExamples.Get_SourceDirectory();
string outputDir = RunExamples.Get_OutputDirectory();
Workbook workbook = new Workbook(SourceDir + "SamplePowerQueryFormula.xlsx");
DataMashup mashupData = workbook.DataMashup;
foreach (PowerQueryFormula formula in mashupData.PowerQueryFormulas)
{
	foreach (PowerQueryFormulaItem item in formula.PowerQueryFormulaItems)
	{
		if (item.Name == "Source")
		{
			item.Value = "Excel.Workbook(File.Contents(\"" + SourceDir + "SamplePowerQueryFormulaSource.xlsx\"), null, true)";
		}
	}
}
//儲存輸出工作簿。
workbook.Save(outputDir + "SamplePowerQueryFormula_out.xlsx");
Console.WriteLine("UpdatePowerQueryFormulaItem executed successfully.");
```

## 結論

使用 Aspose.Cells 操作和處理 Excel 檔案中的資料時，更新 Power Query 公式元素是一項重要操作。按照上面給出的步驟，您可以輕鬆更新公式元素

### 常見問題解答

#### Q：Excel 中的 Power Query 是什麼？
     
答：Power Query 是 Excel 中的功能，可協助收集、轉換和載入來自不同來源的資料。它提供了強大的工具，可以在將資料匯入 Excel 之前清理、組合和重塑資料。

#### Q：如何知道 Power Query 公式項目是否已成功更新？
    A: After running the Power Query Formula Item Update, you can check if the operation was successful by viewing the output and ensuring that the output Excel file was created correctly.

#### Q：我可以一次更新多個 Power Query 公式項目嗎？
    
答：是的，您可以循環遍歷 Power Query 公式項目集合併在單一循環中更新多個項目，具體取決於您的特定需求。

#### Q：我可以使用 Aspose.Cells 對 Power Query 公式執行其他操作嗎？
    
答：是的，Aspose.Cells 提供了使用 Power Query 公式的全套功能，包括在 Excel 工作簿中建立、刪除、複製和搜尋公式。