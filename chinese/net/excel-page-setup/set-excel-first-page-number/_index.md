---
title: 设置 Excel 首页页码
linktitle: 设置 Excel 首页页码
second_title: Aspose.Cells for .NET API 参考
description: 了解如何使用 Aspose.Cells for .NET 在 Excel 中设置首页页码。
type: docs
weight: 90
url: /zh/net/excel-page-setup/set-excel-first-page-number/
---
在本教程中，我们将带您了解如何使用 Aspose.Cells for .NET 在 Excel 中设置首页页码。我们将使用 C# 源代码来说明该过程。

## 第 1 步：设置环境

确保你的机器上安装了 Aspose.Cells for .NET。还要在您喜欢的开发环境中创建一个新项目。

## 第二步：导入必要的库

在您的代码文件中，导入使用 Aspose.Cells 所需的库。下面是相应的代码：

```csharp
using Aspose.Cells;
```

## 第三步：设置数据目录

设置要保存修改后的 Excel 文件的数据目录。使用以下代码：

```csharp
string dataDir = "YOUR DATA DIRECTORY";
```

请务必指定完整的目录路径。

## 第 4 步：创建工作簿和工作表

创建一个新的工作簿对象并使用以下代码导航到工作簿中的第一个工作表：

```csharp
Workbook workbook = new Workbook();
Worksheet worksheet = workbook.Worksheets[0];
```

这将创建一个带有工作表的空工作簿。

## 第五步：设置首页页码

使用以下代码设置工作表页数的第一页：

```csharp
worksheet.PageSetup.FirstPageNumber = 2;
```

这会将第一个页码设置为 2。

## 第 6 步：保存修改后的工作簿

使用以下代码保存修改后的工作簿：

```csharp
workbook.Save(dataDir + "OutputFileName.xls");
```

这会将修改后的工作簿保存到指定的数据目录。

### 使用 Aspose.Cells for .NET 设置 Excel 第一页码的示例源代码 
```csharp
//文档目录的路径。
string dataDir = "YOUR DOCUMENT DIRECTORY";
//实例化工作簿对象
Workbook workbook = new Workbook();
//访问 Excel 文件中的第一个工作表
Worksheet worksheet = workbook.Worksheets[0];
//设置工作表页面的第一页码
worksheet.PageSetup.FirstPageNumber = 2;
//保存工作簿。
workbook.Save(dataDir + "SetFirstPageNumber_out.xls");
```

## 结论

您现在已经学习了如何使用 Aspose.Cells for .NET 在 Excel 中设置首页页码。本教程带您完成了从设置环境到设置首页页码的每一步。您现在可以使用这些知识来自定义 Excel 文件中的页码。

### 常见问题解答

#### Q1：我可以为每个工作表设置不同的首页页码吗？

 A1：是的，您可以通过访问`FirstPageNumber`各自工作表的属性`PageSetup`目的。

#### Q2：如何查看现有电子表格的首页页码？

 A2：您可以通过访问`FirstPageNumber`的财产`PageSetup`对应于该工作表的对象。

#### Q3：页码是否默认总是从1开始？

A3：是的，在 Excel 中页码默认从 1 开始。但是，您可以使用本教程中显示的代码来设置不同的首页编号。

#### Q4：编辑后的 Excel 文件中首页页码的更改是永久性的吗？

A4: 是的，对首页页码所做的更改将永久保存在修改后的 Excel 文件中。

#### Q5：此方法是否适用于所有 Excel 文件格式，例如 .xls 和 .xlsx？

A5：是的，此方法适用于 Aspose.Cells 支持的所有 Excel 文件格式，包括 .xls 和 .xlsx。