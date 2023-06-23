---
title: 设置 Excel 首页页码
linktitle: 设置 Excel 首页页码
second_title: Aspose.Cells for .NET API 参考
description: 了解如何使用 Aspose.Cells for .NET 在 Excel 中设置首页页码。
type: docs
weight: 90
url: /zh/net/excel-page-setup/set-excel-first-page-number/
---
在本教程中，我们将引导您了解如何使用 Aspose.Cells for .NET 在 Excel 中设置首页页码。我们将使用 C# 源代码来说明该过程。

## 第一步：搭建环境

确保您的计算机上安装了 Aspose.Cells for .NET。还可以在您首选的开发环境中创建一个新项目。

## 第二步：导入必要的库

在您的代码文件中，导入使用 Aspose.Cells 所需的库。这是相应的代码：

```csharp
using Aspose.Cells;
```

## 第三步：设置数据目录

设置要保存修改后的 Excel 文件的数据目录。使用以下代码：

```csharp
string dataDir = "YOUR DATA DIRECTORY";
```

请务必指定完整的目录路径。

## 步骤 4：创建工作簿和工作表

创建一个新的 Workbook 对象并使用以下代码导航到工作簿中的第一个工作表：

```csharp
Workbook workbook = new Workbook();
Worksheet worksheet = workbook.Worksheets[0];
```

这将创建一个带有工作表的空工作簿。

## 第五步：设置首页页码

使用以下代码设置工作表第一页的页码：

```csharp
worksheet.PageSetup.FirstPageNumber = 2;
```

这会将首页页码设置为 2。

## 第6步：保存修改后的工作簿

使用以下代码保存修改后的工作簿：

```csharp
workbook.Save(dataDir + "OutputFileName.xls");
```

这会将修改后的工作簿保存到指定的数据目录。

### 使用 Aspose.Cells for .NET 设置 Excel 第一页码的示例源代码 
```csharp
//文档目录的路径。
string dataDir = "YOUR DOCUMENT DIRECTORY";
//实例化 Workbook 对象
Workbook workbook = new Workbook();
//访问 Excel 文件中的第一个工作表
Worksheet worksheet = workbook.Worksheets[0];
//设置工作表页面的首页页码
worksheet.PageSetup.FirstPageNumber = 2;
//保存工作簿。
workbook.Save(dataDir + "SetFirstPageNumber_out.xls");
```

## 结论

您现在已经了解了如何使用 Aspose.Cells for .NET 在 Excel 中设置首页页码。本教程将引导您完成该过程的每一步，从设置环境到设置首页页码。现在，您可以使用这些知识来自定义 Excel 文件中的页码。

### 常见问题解答

#### Q1：我可以为每个工作表设置不同的首页页码吗？

 A1：是的，您可以通过访问为每个工作表设置不同的首页页码`FirstPageNumber`各自工作表的属性`PageSetup`目的。

#### Q2：如何查看现有电子表格的首页页码？

 A2：您可以通过访问查看现有工作表的首页页码`FirstPageNumber`的财产`PageSetup`与该工作表对应的对象。

#### Q3：页码默认都是从1开始吗？

A3：是的，Excel 中页码默认从 1 开始。但是，您可以使用本教程中显示的代码来设置不同的首页页码。

#### 问题 4：对首页页码的更改会永久保留在编辑的 Excel 文件中吗？

A4：是的，对首页页码所做的更改将永久保存在修改后的 Excel 文件中。

#### Q5：此方法适用于所有 Excel 文件格式，例如 .xls 和 .xlsx 吗？

A5：是的，此方法适用于 Aspose.Cells 支持的所有 Excel 文件格式，包括 .xls 和 .xlsx。