---
title: 更新 Power Query 公式项
linktitle: 更新 Power Query 公式项
second_title: Aspose.Cells for .NET API 参考
description: 了解如何使用 Aspose.Cells for .NET 更新 Excel 文件中的 Power Query 公式元素。
type: docs
weight: 160
url: /zh/net/excel-workbook/update-power-query-formula-item/
---
更新 Power Query 公式项是处理 Excel 文件中的数据时的常见操作。使用 Aspose.Cells for .NET，您可以按照以下步骤轻松更新 Power Query 公式项：

## 第 1 步：指定源目录和输出目录

首先，您需要指定包含要更新的 Power Query 公式的 Excel 文件所在的源目录，以及要保存修改后的文件的输出目录。以下是使用 Aspose.Cells 执行此操作的方法：

```csharp
//源目录
string SourceDir = RunExamples.Get_SourceDirectory();

//输出目录
string outputDir = RunExamples.Get_OutputDirectory();
```

## 步骤 2：加载源 Excel 工作簿

接下来，您需要加载要更新 Power Query 公式项的源 Excel 工作簿。操作方法如下：

```csharp
//加载源 Excel 工作簿
Workbook workbook = new Workbook(SourceDir + "SamplePowerQueryFormula.xlsx");
```

## 步骤 3：浏览并更新 Power Query 公式项

加载工作簿后，您可以导航到 Power Query 公式集合并浏览每个公式及其元素。在此示例中，我们正在查找名称为“Source”的公式项并更新其值。以下是更新 Power Query 公式项的示例代码：

```csharp
//访问 Power Query 公式集合
DataMashup mashupData = workbook.DataMashup;

//循环访问 Power Query 公式及其元素
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

## 步骤 4：保存输出的 Excel 工作簿

更新 Power Query 公式项后，您可以将修改后的 Excel 工作簿保存到指定的输出目录。操作方法如下：

```csharp
//保存输出的 Excel 工作簿
workbook.Save(outputDir + "SamplePowerQueryFormula_out.xlsx");
Console.WriteLine("UpdatePowerQueryFormulaItem executed successfully.\r\n");
```

### 使用 Aspose.Cells for .NET 更新 Power Query 公式项的示例源代码 
```csharp
//工作目录
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
//保存输出工作簿。
workbook.Save(outputDir + "SamplePowerQueryFormula_out.xlsx");
Console.WriteLine("UpdatePowerQueryFormulaItem executed successfully.");
```

## 结论

使用 Aspose.Cells 操作和处理 Excel 文件中的数据时，更新 Power Query 公式元素是一项重要操作。按照上面给出的步骤，您可以轻松更新公式元素

### 常见问题解答

#### 问：Excel 中的 Power Query 是什么？
     
答：Power Query 是 Excel 中的一项功能，可帮助收集、转换和加载来自不同来源的数据。它提供了强大的工具，可以在将数据导入 Excel 之前清理、组合和重塑数据。

#### 问：如何知道 Power Query 公式项是否已成功更新？
    A: After running the Power Query Formula Item Update, you can check if the operation was successful by viewing the output and ensuring that the output Excel file was created correctly.

#### 问：我可以一次更新多个 Power Query 公式项吗？
    
答：是的，您可以循环遍历 Power Query 公式项目集合并在单个循环中更新多个项目，具体取决于您的具体需求。

#### 问：我可以使用 Aspose.Cells 对 Power Query 公式执行其他操作吗？
    
答：是的，Aspose.Cells 提供了使用 Power Query 公式的全套功能，包括在 Excel 工作簿中创建、删除、复制和搜索公式。