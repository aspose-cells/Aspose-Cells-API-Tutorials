---
title: 设置类别数据
linktitle: 设置类别数据
second_title: Aspose.Cells .NET Excel 处理 API
description: 了解如何使用 Aspose.Cells for .NET 在 Excel 图表中设置类别数据。按照我们的分步教程轻松实现。
type: docs
weight: 15
url: /zh/net/advanced-chart-operations/setting-category-data/
---
## 介绍

当谈到以编程方式管理和操作 Excel 文件时，拥有合适的工具可以带来很大的不同。Aspose.Cells for .NET 就是这样一种工具，它允许开发人员轻松创建、编辑和转换 Excel 文件。无论您是构建复杂的数据分析应用程序还是只需要自动生成报告，Aspose.Cells 都能满足您的需求。 

## 先决条件 

在深入讨论细节之前，让我们先确保您已获得所需的一切：

1. 开发环境：确保您已设置 .NET 开发环境。建议使用 Visual Studio。
2.  Aspose.Cells for .NET Library：从以下网址下载最新版本的库：[Aspose.Cells 下载页面](https://releases.aspose.com/cells/net/).
3. 对 C# 的基本了解：熟悉 C# 和 Excel 概念将帮助您更顺利地掌握内容。
4. 访问文档：可以访问[Aspose.Cells 文档](https://reference.aspose.com/cells/net/)如果你遇到困难时可以提供额外的见解。 

一切就绪后，让我们逐步揭开 Excel 操作的魔力。

## 导入包 

在开始编码之前，导入必要的软件包至关重要。这使我们能够访问 Aspose.Cells 提供的功能。

## 步骤 1：导入命名空间

首先，让我们将 Aspose.Cells 命名空间导入到您的 C# 文件中。

```csharp
using System;
using System.IO;
using Aspose.Cells;
```

通过在文件顶部包含此行，您可以访问 Aspose.Cells 库中的所有相关类和方法。

现在我们已经熟悉了先决条件并导入了必要的库，让我们探索如何在 Excel 图表中设置类别数据。

## 第 2 步：定义输出目录

首先，您需要指定 Excel 文件的保存位置。为输出目录创建一个变量。 

```csharp
string outputDir = "Your Output Directory";
```

代替`"Your Output Directory"`以及您想要保存输出 Excel 文件的实际路径。这可确保您确切知道在哪里可以找到成品！

## 步骤 3：实例化工作簿对象

接下来，您将创建 Workbook 对象的新实例。此对象用作 Excel 文件的容器。

```csharp
Workbook workbook = new Workbook();
```

## 步骤 4：访问第一个工作表

您需要使用工作簿中的第一个工作表。访问工作表非常简单：

```csharp
Worksheet worksheet = workbook.Worksheets[0];
```

指数`0`指向第一个工作表。在 Excel 中，可将其视为打开工作簿中的第一个选项卡。

## 步骤 5：向单元格添加示例值

让我们填写一些数据。您可以在前两列中添加数值。 

```csharp
worksheet.Cells["A1"].PutValue(10);
worksheet.Cells["A2"].PutValue(100);
worksheet.Cells["A3"].PutValue(170);
worksheet.Cells["A4"].PutValue(200);
worksheet.Cells["B1"].PutValue(120);
worksheet.Cells["B2"].PutValue(320);
worksheet.Cells["B3"].PutValue(50);
worksheet.Cells["B4"].PutValue(40);
```

在此代码片段中，我们用不同的数值填充 A1 至 A4 行，并填充 B1 至 B4 列。这些数据将作为我们图表的基础。

## 步骤6：添加类别数据

现在，让我们标记数据类别。这是在第三列（C 列）中完成的：

```csharp
worksheet.Cells["C1"].PutValue("Q1");
worksheet.Cells["C2"].PutValue("Q2");
worksheet.Cells["C3"].PutValue("Y1");
worksheet.Cells["C4"].PutValue("Y2");
```

在这里，我们用“Q1”和“Y1”等类别来表示每组数据，以便以后更容易解释我们的图表。

## 创建图表

有了数据后，我们就可以添加图表来直观地呈现这些数据了。

## 步骤 7：向工作表添加图表

现在，让我们在工作表上添加一个类型为“列”的图表。

```csharp
int chartIndex = worksheet.Charts.Add(Aspose.Cells.Charts.ChartType.Column, 5, 0, 15, 5);
```

此行从工作表的第 5 行和第 0 列开始创建一个新的柱形图。

## 步骤 8：访问图表实例

在我们用数据填充图表之前，我们需要访问新创建图表的实例：

```csharp
Aspose.Cells.Charts.Chart chart = worksheet.Charts[chartIndex];
```

通过这一步，我们现在可以将数据系列添加到图表中了。

## 步骤 9：向图表添加数据系列

接下来，您将添加系列集合，它定义图表将显示的数据。 

```csharp
chart.NSeries.Add("A1:B4", true);
```

此行指定图表应获取范围 A1 至 B4 中的数据，以便以直观的方式显示这些值。

## 步骤10：设置类别数据

接下来是关键部分——定义我们的类别数据。这就是在 x 轴上标记数据点的内容。

```csharp
chart.NSeries.CategoryData = "C1:C4";
```

通过指定此范围，我们可以告诉图表哪些单元格对应于数据系列中的类别。如果没有此步骤，您的图表就只是一组数字！

## 步骤11：保存Excel文件

所有设置完毕后，就该保存我们辛苦工作的成果了。 

```csharp
workbook.Save(outputDir + "outputSettingCategoryData.xlsx");
```

此命令将您的工作簿以“outputSettingCategoryData.xlsx”名称保存在指定的输出目录中。 

## 步骤12：确认信息

最后，我们可以添加一些反馈来确认一切顺利进行：

```csharp
Console.WriteLine("SettingCategoryData executed successfully.");
```

这会在控制台中打印一条消息，让您知道该过程已完成。很简单，对吧？

## 结论

就这样！您已成功使用 Aspose.Cells for .NET 为 Excel 工作簿中的图表设置类别数据。这种方法的优点在于它允许您自动执行 Excel 文件操作，而无需在计算机上安装 Excel。 

## 常见问题解答

### 什么是 Aspose.Cells？
Aspose.Cells 是一个无需 Microsoft Excel 即可管理 Excel 文件的 .NET 库。它允许以编程方式创建、编辑和转换 Excel 文档。

### 我可以免费使用 Aspose.Cells 吗？
是的，您可以免费试用 Aspose.Cells。他们提供免费试用版[这里](https://releases.aspose.com/).

### Aspose.Cells 适合大型数据集吗？
当然！Aspose.Cells 旨在高效处理大型数据集，是数据密集型应用程序的可靠选择。

### 如何使用 Aspose.Cells 添加图表？
您可以通过创建新的图表对象并将其链接到包含数据的单元格范围来添加图表，如本教程中所示。

### 在哪里可以找到更多使用 Aspose.Cells 的示例？
您可以在以下位置探索更多示例和详细文档[Aspose.Cells 文档页面](https://reference.aspose.com/cells/net/).