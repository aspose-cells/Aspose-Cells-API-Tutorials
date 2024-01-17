---
title: 獲取 Odata 詳細信息
linktitle: 獲取 Odata 詳細信息
second_title: Aspose.Cells for .NET API 參考
description: 了解如何使用 Aspose.Cells for .NET 從 Excel 工作簿中擷取 OData 詳細資訊。
type: docs
weight: 110
url: /zh-hant/net/excel-workbook/get-odata-details/
---
從外部資料來源擷取結構化資料時，OData 的使用很常見。使用 Aspose.Cells for .NET，您可以輕鬆地從 Excel 工作簿中擷取 OData 詳細資訊。請按照以下步驟操作以獲得所需的結果：

## 第1步：指定來源目錄

首先，您需要指定包含 OData 詳細資訊的 Excel 檔案所在的來源目錄。以下是使用 Aspose.Cells 執行此操作的方法：

```csharp
//來源目錄
string SourceDir = RunExamples.Get_SourceDirectory();
```

## 第 2 步：載入工作簿

指定來源目錄後，您可以從檔案載入 Excel 工作簿。這是範例程式碼：

```csharp
//載入工作簿
Workbook workbook = new Workbook(SourceDir + "ODataSample.xlsx");
```

## 步驟 3：取得 OData 詳細信息

載入工作簿後，您可以使用 PowerQueryFormulas 集合存取 OData 詳細資訊。就是這樣：

```csharp
//檢索 Power Query 公式的集合
PowerQueryFormulaCollction PQFcoll = workbook.DataMashup.PowerQueryFormulas;

//瀏覽每個 Power Query 公式
foreach(PowerQueryFormula PQF in PQFcoll)
{
Console.WriteLine("Connection name: " + PQF.Name);

//檢索 Power Query 公式元素的集合
PowerQueryFormulaItemCollection PQFIcoll = PQF.PowerQueryFormulaItems;

//迭代每個 Power Query 公式元素
foreach (PowerQueryFormulaItem PQFI in PQFIcoll)
{
Console.WriteLine("Name: " + PQFI.Name);
Console.WriteLine("Value: " + PQFI.Value);
}
}

Console.WriteLine("GetOdataDetails executed successfully.");
```

### 使用 Aspose.Cells for .NET 取得 Odata 詳細資訊的範例原始程式碼 
```csharp
//來源目錄
string SourceDir = RunExamples.Get_SourceDirectory();
Workbook workbook = new Workbook(SourceDir + "ODataSample.xlsx");
PowerQueryFormulaCollction PQFcoll = workbook.DataMashup.PowerQueryFormulas;
foreach (PowerQueryFormula PQF in PQFcoll)
{
	Console.WriteLine("Connection Name: " + PQF.Name);
	PowerQueryFormulaItemCollection PQFIcoll = PQF.PowerQueryFormulaItems;
	foreach (PowerQueryFormulaItem PQFI in PQFIcoll)
	{
		Console.WriteLine("Name: " + PQFI.Name);
		Console.WriteLine("Value: " + PQFI.Value);
	}
}
Console.WriteLine("GetOdataDetails executed successfully.");
```

## 結論

現在，使用 Aspose.Cells for .NET 可以輕鬆從 Excel 工作簿中擷取 OData 詳細資訊。透過遵循本指南中概述的步驟，您將能夠有效地存取和處理 OData 資料。試驗您自己的包含 OData 詳細資訊的 Excel 文件，並充分利用這項強大的功能。

### 常見問題解答

#### Q：Aspose.Cells 是否支援 OData 以外的其他資料來源？
    
答：是的，Aspose.Cells 支援多種資料來源，例如 SQL 資料庫、CSV 檔案、Web 服務等。

#### Q：如何在我的應用程式中使用檢索到的 OData 詳細資訊？
    
答：使用 Aspose.Cells 檢索 OData 詳細資訊後，您可以將它們用於資料分析、報告產生或應用程式中的任何其他操作。

#### Q：使用 Aspose.Cells 檢索時可以過濾或排序 OData 資料嗎？
    
答：是的，Aspose.Cells 提供了過濾、排序和操作 OData 資料的進階功能，以滿足您的特定需求。

#### Q：我可以使用 Aspose.Cells 自動執行檢索 OData 詳細資訊的過程嗎？
    
答：是的，您可以透過將 Aspose.Cells 整合到您的工作流程中或使用程式腳本來自動化檢索 OData 詳細資訊的流程。