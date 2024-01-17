---
title: 提取嵌入的 Mol 文件
linktitle: 提取嵌入的 Mol 文件
second_title: Aspose.Cells for .NET API 參考
description: 了解如何使用 Aspose.Cells for .NET 從 Excel 工作簿輕鬆提取嵌入的 MOL 檔案。
type: docs
weight: 90
url: /zh-hant/net/excel-workbook/extract-embedded-mol-file/
---
在本教學中，我們將逐步引導您了解如何使用 .NET 的 Aspose.Cells 庫從 Excel 工作簿中提取嵌入的 MOL 檔案。您將學習如何瀏覽工作簿工作表、提取相應的 OLE 物件以及保存提取的 MOL 檔案。請依照以下步驟成功完成此任務。

## 第 1 步：定義來源目錄和輸出目錄
首先，我們需要在程式碼中定義來源目錄和輸出目錄。這些目錄指示來源 Excel 工作簿所在的位置以及擷取的 MOL 檔案的儲存位置。這是對應的程式碼：

```csharp
//目錄
string SourceDir = RunExamples.Get_SourceDirectory();
string outputDir = RunExamples.Get_OutputDirectory();
```

請務必根據需要指定適當的路徑。

## 第 2 步：載入 Excel 工作簿
下一步是載入包含嵌入的 OLE 物件和 MOL 檔案的 Excel 工作簿。這是載入工作簿的程式碼：

```csharp
Workbook workbook = new Workbook(SourceDir + "EmbeddedMolSample.xlsx");
```

確保在程式碼中正確指定原始檔案名稱。

## 步驟 3：遍歷工作表並提取 MOL 文件
現在我們將循環遍歷工作簿中的每個工作表並提取相應的 OLE 對象，其中包含 MOL 檔案。這是對應的程式碼：

```csharp
var index = 1;
foreach(Worksheet sheet in workbook.Worksheets)
{
     OleObjectCollection oles = sheet.OleObjects;
     foreach(OleObject ole in oles)
     {
         string fileName = outputDir + "OleObject" + index + ".mol";
         FileStream fs = File.Create(fileName);
         fs.Write(ole.ObjectData, 0, ole.ObjectData.Length);
         fs. Close();
         index++;
     }
}
Console.WriteLine("ExtractEmbeddedMolFile executed successfully.");
```

此程式碼循環遍歷工作簿中的每個工作表，取得 OLE 對象，並將提取的 MOL 檔案儲存到輸出目錄。

### 使用 Aspose.Cells for .NET 提取嵌入式 Mol 檔案的範例原始程式碼 
```csharp
//目錄
string SourceDir = RunExamples.Get_SourceDirectory();
string outputDir = RunExamples.Get_OutputDirectory();
Workbook workbook = new Workbook(SourceDir + "EmbeddedMolSample.xlsx");
var index = 1;
foreach (Worksheet sheet in workbook.Worksheets)
{
	OleObjectCollection oles = sheet.OleObjects;
	foreach (OleObject ole in oles)
	{
		string fileName = outputDir + "OleObject" + index + ".mol ";
		FileStream fs = File.Create(fileName);
		fs.Write(ole.ObjectData, 0, ole.ObjectData.Length);
		fs.Close();
		index++;
	}
}
Console.WriteLine("ExtractEmbeddedMolFile executed successfully.");
```

## 結論
恭喜！您已了解如何使用 Aspose.Cells for .NET 從 Excel 工作簿中提取嵌入的 MOL 檔案。現在您可以應用這些知識從您自己的 Excel 工作簿中提取 MOL 檔案。請隨意進一步探索 Aspose.Cells 庫並了解其其他強大功能。

### 常見問題解答

#### Q：什麼是MOL檔案？
 
答：MOL 檔案是用來表示計算化學中的化學結構的檔案格式。它包含有關原子、鍵和其他分子特性的資訊。

#### Q：此方法適用於所有 Excel 檔案類型嗎？

答：是的，此方法適用於 Aspose.Cells 支援的所有 Excel 檔案類型。

#### Q：我可以一次提取多個 MOL 檔案嗎？

答：是的，您可以透過迭代工作簿中每個工作表上的 OLE 物件來一次提取多個 MOL 檔案。