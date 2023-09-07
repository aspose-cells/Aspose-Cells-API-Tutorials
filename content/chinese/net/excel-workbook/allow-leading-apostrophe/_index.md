---
title: 允许前导撇号
linktitle: 允许前导撇号
second_title: Aspose.Cells for .NET API 参考
description: 允许使用 Aspose.Cells for .NET 在 Excel 工作簿中使用前导撇号。
type: docs
weight: 60
url: /zh/net/excel-workbook/allow-leading-apostrophe/
---
在本分步教程中，我们将解释所提供的 C# 源代码，该源代码将允许您使用 Aspose.Cells for .NET 在 Excel 工作簿中使用前导撇号。请按照以下步骤执行此操作。

## 第 1 步：设置源目录和输出目录

```csharp
//源目录
string sourceDir = RunExamples.Get_SourceDirectory();
//输出目录
string outputDir = RunExamples.Get_OutputDirectory();
```

在第一步中，我们定义 Excel 文件的源目录和输出目录。

## 步骤 2：实例化 WorkbookDesigner 对象

```csharp
//实例化 WorkbookDesigner 对象
WorkbookDesigner designer = new WorkbookDesigner();
```

我们创建一个实例`WorkbookDesigner`来自 Aspose.Cells 的类。

## 第 3 步：加载 Excel 工作簿

```csharp
//加载 Excel 工作簿
Workbook workbook = new Workbook(sourceDir + "AllowLeadingApostropheSample.xlsx");
workbook.Settings.QuotePrefixToStyle = false;
designer.Workbook = workbook;
```

我们从指定文件加载 Excel 工作簿，并禁用首字母撇号自动转换为文本样式。

## 第四步：设置数据源

```csharp
//定义设计器工作簿的数据源
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

我们定义一个数据对象列表并使用`SetDataSource`方法来设置设计器工作簿的数据源。

## 第 5 步：处理智能标记

```csharp
//处理智能标记
designer. Process();
```

我们使用`Process`在设计器工作簿中处理智能标记的方法。

## 步骤6：保存修改后的Excel工作簿

```csharp
//保存修改后的Excel工作簿
designer.Workbook.Save(outputDir + "AllowLeadingApostropheSample_out.xlsx");
```

我们保存修改后的 Excel 工作簿以及所做的更改。

### 使用 Aspose.Cells for .NET 允许前导撇号的示例源代码 
```csharp
//源码目录
string sourceDir = RunExamples.Get_SourceDirectory();
string outputDir = RunExamples.Get_OutputDirectory();
//实例化 WorkbookDesigner 对象
WorkbookDesigner designer = new WorkbookDesigner();
Workbook workbook = new Workbook(sourceDir + "AllowLeadingApostropheSample.xlsx");
workbook.Settings.QuotePrefixToStyle = false;
//打开包含智能标记的设计器电子表格
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
//设置设计器电子表格的数据源
designer.SetDataSource("sampleData", list);
//处理智能标记
designer.Process();
designer.Workbook.Save(outputDir + "AllowLeadingApostropheSample_out.xlsx");
Console.WriteLine("AllowLeadingApostrophe executed successfully.");
```

## 结论

恭喜！您学习了如何使用 Aspose.Cells for .NET 在 Excel 工作簿中使用前导撇号。使用您自己的数据进行试验以进一步自定义您的 Excel 工作簿。

### 常见问题解答

#### 问：Excel 工作簿中的前导撇号权限是什么？

答：允许在 Excel 工作簿中使用首字母撇号可以正确显示以撇号开头的数据，而无需将其转换为文本样式。当您想要将撇号保留为数据的一部分时，这非常有用。

#### 问：为什么需要关闭首字母撇号的自动转换？

答：通过禁用前导引号的自动转换，您可以保留它们在数据中的使用方式。这可以避免在打开或操作 Excel 工作簿时对数据进行任何意外修改。

#### 问：设计师工作簿中如何设置数据源？

 A：要在设计器工作簿中设置数据源，可以使用`SetDataSource`方法指定数据源的名称和相应数据对象的列表。

#### 问：允许前导撇号是否会影响 Excel 工作簿中的其他数据？

答：不可以，允许前导撇号仅影响以撇号开头的数据。 Excel 工作簿中的其他数据保持不变。

#### 问：我可以将此功能用于其他 Excel 文件格式吗？

答：是的，您可以将此功能与 Aspose.Cells 支持的其他 Excel 文件格式一起使用，例如 .xls、.xlsm 等。