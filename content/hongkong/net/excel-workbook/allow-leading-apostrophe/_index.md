---
title: 允許前導撇號
linktitle: 允許前導撇號
second_title: Aspose.Cells for .NET API 參考
description: 允許使用 Aspose.Cells for .NET 在 Excel 工作簿中使用前導撇號。
type: docs
weight: 60
url: /zh-hant/net/excel-workbook/allow-leading-apostrophe/
---
在本逐步教學中，我們將解釋所提供的 C# 原始程式碼，該程式碼將允許您使用 Aspose.Cells for .NET 在 Excel 工作簿中使用前導撇號。請按照以下步驟執行此操作。

## 第 1 步：設定來源目錄和輸出目錄

```csharp
//來源目錄
string sourceDir = RunExamples.Get_SourceDirectory();
//輸出目錄
string outputDir = RunExamples.Get_OutputDirectory();
```

在第一步中，我們定義 Excel 檔案的來源目錄和輸出目錄。

## 步驟 2：實例化 WorkbookDesigner 對象

```csharp
//實例化 WorkbookDesigner 對象
WorkbookDesigner designer = new WorkbookDesigner();
```

我們建立一個實例`WorkbookDesigner`來自 Aspose.Cells 的類別。

## 第 3 步：載入 Excel 工作簿

```csharp
//載入 Excel 工作簿
Workbook workbook = new Workbook(sourceDir + "AllowLeadingApostropheSample.xlsx");
workbook.Settings.QuotePrefixToStyle = false;
designer.Workbook = workbook;
```

我們從指定檔案載入 Excel 工作簿，並停用首字母撇號自動轉換為文字樣式。

## 第四步：設定資料來源

```csharp
//定義設計器工作簿的資料來源
List<DataObject> list = new List<DataObject>
{
new DataObject
{
Id=1,
Name = "demo"
},
new DataObject
{
ID=2,
Name = "'demo"
}
};
designer.SetDataSource("sampleData", list);
```

我們定義一個資料對象清單並使用`SetDataSource`方法來設定設計器工作簿的資料來源。

## 第 5 步：處理智慧標記

```csharp
//處理智慧標記
designer. Process();
```

我們使用`Process`在設計器工作簿中處理智慧標記的方法。

## 步驟6：儲存修改後的Excel工作簿

```csharp
//儲存修改後的Excel工作簿
designer.Workbook.Save(outputDir + "AllowLeadingApostropheSample_out.xlsx");
```

我們儲存修改後的 Excel 工作簿以及所做的變更。

### 使用 Aspose.Cells for .NET 允許前導撇號的範例原始程式碼 
```csharp
//原始碼目錄
string sourceDir = RunExamples.Get_SourceDirectory();
string outputDir = RunExamples.Get_OutputDirectory();
//實例化 WorkbookDesigner 對象
WorkbookDesigner designer = new WorkbookDesigner();
Workbook workbook = new Workbook(sourceDir + "AllowLeadingApostropheSample.xlsx");
workbook.Settings.QuotePrefixToStyle = false;
//開啟包含智慧標記的設計器電子表格
designer.Workbook = workbook;
List<DataObject> list = new List<DataObject>
{
	new DataObject
	{
		 Id =1,
		 Name = "demo"
	},
	new DataObject
	{
		Id=2,
		Name = "'demo"
	}
};
//設定設計器電子表格的資料來源
designer.SetDataSource("sampleData", list);
//處理智慧標記
designer.Process();
designer.Workbook.Save(outputDir + "AllowLeadingApostropheSample_out.xlsx");
Console.WriteLine("AllowLeadingApostrophe executed successfully.");
```

## 結論

恭喜！您學習如何使用 Aspose.Cells for .NET 在 Excel 工作簿中使用前導撇號。使用您自己的資料進行試驗以進一步自訂您的 Excel 工作簿。

### 常見問題解答

#### Q：Excel 工作簿中的前導撇號權限是什麼？

答：允許在 Excel 工作簿中使用首字母撇號可以正確顯示以撇號開頭的數據，而無需將其轉換為文字樣式。當您想要將撇號保留為資料的一部分時，這非常有用。

#### Q：為什麼需要關閉首字母撇號的自動轉換？

答：透過停用前導引號的自動轉換，您可以保留它們在資料中的使用方式。這可以避免在開啟或操作 Excel 工作簿時對資料進行任何意外修改。

#### Q：設計師工作簿中如何設定資料來源？

 A：要在設計器工作簿中設定資料來源，可以使用`SetDataSource`方法指定資料來源的名稱和對應資料物件的清單。

#### Q：允許前導撇號是否會影響 Excel 工作簿中的其他資料？

答：不可以，允許前導撇號僅影響以撇號開頭的資料。 Excel 工作簿中的其他資料保持不變。

#### Q：我可以將此功能用於其他 Excel 檔案格式嗎？

答：是的，您可以將此功能與 Aspose.Cells 支援的其他 Excel 檔案格式一起使用，例如 .xls、.xlsm 等。