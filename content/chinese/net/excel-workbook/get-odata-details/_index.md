---
title: 获取 Odata 详细信息
linktitle: 获取 Odata 详细信息
second_title: Aspose.Cells for .NET API 参考
description: 了解如何使用 Aspose.Cells for .NET 从 Excel 工作簿中检索 OData 详细信息。
type: docs
weight: 110
url: /zh/net/excel-workbook/get-odata-details/
---
从外部数据源检索结构化数据时，OData 的使用很常见。使用 Aspose.Cells for .NET，您可以轻松地从 Excel 工作簿中检索 OData 详细信息。请按照以下步骤操作以获得所需的结果：

## 第1步：指定源目录

首先，您需要指定包含 OData 详细信息的 Excel 文件所在的源目录。以下是使用 Aspose.Cells 执行此操作的方法：

```csharp
//源目录
string SourceDir = RunExamples.Get_SourceDirectory();
```

## 第 2 步：加载工作簿

指定源目录后，您可以从文件加载 Excel 工作簿。这是示例代码：

```csharp
//加载工作簿
Workbook workbook = new Workbook(SourceDir + "ODataSample.xlsx");
```

## 步骤 3：获取 OData 详细信息

加载工作簿后，您可以使用 PowerQueryFormulas 集合访问 OData 详细信息。就是这样：

```csharp
//检索 Power Query 公式的集合
PowerQueryFormulaCollction PQFcoll = workbook.DataMashup.PowerQueryFormulas;

//浏览每个 Power Query 公式
foreach(PowerQueryFormula PQF in PQFcoll)
{
Console.WriteLine("Connection name: " + PQF.Name);

//检索 Power Query 公式元素的集合
PowerQueryFormulaItemCollection PQFIcoll = PQF.PowerQueryFormulaItems;

//迭代每个 Power Query 公式元素
foreach (PowerQueryFormulaItem PQFI in PQFIcoll)
{
Console.WriteLine("Name: " + PQFI.Name);
Console.WriteLine("Value: " + PQFI.Value);
}
}

Console.WriteLine("GetOdataDetails executed successfully.");
```

### 使用 Aspose.Cells for .NET 获取 Odata 详细信息的示例源代码 
```csharp
//源目录
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

## 结论

现在，使用 Aspose.Cells for .NET 可以轻松从 Excel 工作簿中检索 OData 详细信息。通过遵循本指南中概述的步骤，您将能够有效地访问和处理 OData 数据。试验您自己的包含 OData 详细信息的 Excel 文件，并充分利用这一强大的功能。

### 常见问题解答

#### 问：Aspose.Cells 是否支持 OData 之外的其他数据源？
    
答：是的，Aspose.Cells 支持多种数据源，例如 SQL 数据库、CSV 文件、Web 服务等。

#### 问：如何在我的应用程序中使用检索到的 OData 详细信息？
    
答：使用 Aspose.Cells 检索 OData 详细信息后，您可以将它们用于数据分析、报告生成或应用程序中的任何其他操作。

#### 问：使用 Aspose.Cells 检索时可以过滤或排序 OData 数据吗？
    
答：是的，Aspose.Cells 提供了过滤、排序和操作 OData 数据的高级功能，以满足您的特定需求。

#### 问：我可以使用 Aspose.Cells 自动执行检索 OData 详细信息的过程吗？
    
答：是的，您可以通过将 Aspose.Cells 集成到您的工作流程中或使用编程脚本来自动化检索 OData 详细信息的过程。