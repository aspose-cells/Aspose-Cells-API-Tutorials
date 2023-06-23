---
title: 提取嵌入的 Mol 文件
linktitle: 提取嵌入的 Mol 文件
second_title: Aspose.Cells for .NET API 参考
description: 了解如何使用 Aspose.Cells for .NET 从 Excel 工作簿轻松提取嵌入的 MOL 文件。
type: docs
weight: 90
url: /zh/net/excel-workbook/extract-embedded-mol-file/
---
在本教程中，我们将逐步引导您了解如何使用 .NET 的 Aspose.Cells 库从 Excel 工作簿中提取嵌入的 MOL 文件。您将学习如何浏览工作簿工作表、提取相应的 OLE 对象以及保存提取的 MOL 文件。请按照以下步骤成功完成此任务。

## 第 1 步：定义源目录和输出目录
首先，我们需要在代码中定义源目录和输出目录。这些目录指示源 Excel 工作簿所在的位置以及提取的 MOL 文件的保存位置。这是相应的代码：

```csharp
//目录
string SourceDir = RunExamples.Get_SourceDirectory();
string outputDir = RunExamples.Get_OutputDirectory();
```

请务必根据需要指定适当的路径。

## 第 2 步：加载 Excel 工作簿
下一步是加载包含嵌入的 OLE 对象和 MOL 文件的 Excel 工作簿。这是加载工作簿的代码：

```csharp
Workbook workbook = new Workbook(SourceDir + "EmbeddedMolSample.xlsx");
```

确保在代码中正确指定源文件名。

## 步骤 3：遍历工作表并提取 MOL 文件
现在我们将循环遍历工作簿中的每个工作表并提取相应的 OLE 对象，其中包含 MOL 文件。这是相应的代码：

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

此代码循环遍历工作簿中的每个工作表，获取 OLE 对象，并将提取的 MOL 文件保存到输出目录。

### 使用 Aspose.Cells for .NET 提取嵌入式 Mol 文件的示例源代码 
```csharp
//目录
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

## 结论
恭喜！您已了解如何使用 Aspose.Cells for .NET 从 Excel 工作簿中提取嵌入的 MOL 文件。您现在可以应用这些知识从您自己的 Excel 工作簿中提取 MOL 文件。请随意进一步探索 Aspose.Cells 库并了解其其他强大功能。

### 常见问题解答

#### 问：什么是MOL文件？
 
答：MOL 文件是一种用于表示计算化学中的化学结构的文件格式。它包含有关原子、键和其他分子特性的信息。

#### 问：此方法适用于所有 Excel 文件类型吗？

答：是的，此方法适用于 Aspose.Cells 支持的所有 Excel 文件类型。

#### 问：我可以一次提取多个 MOL 文件吗？

答：是的，您可以通过迭代工作簿中每个工作表上的 OLE 对象来一次提取多个 MOL 文件。