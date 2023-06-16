---
title: 适合 Excel 页面选项
linktitle: 适合 Excel 页面选项
second_title: Aspose.Cells for .NET API 参考
description: 了解如何使用 Aspose.Cells for .NET 自动调整 Excel 电子表格中的页面。
type: docs
weight: 30
url: /zh/net/excel-page-setup/fit-to-excel-pages-options/
---
在本文中，我们将带您一步一步地解释以下 C# 源代码：Fit to Excel Pages Options using Aspose.Cells for .NET。我们将使用 .NET 的 Aspose.Cells 库来执行此操作。按照以下步骤在 Excel 中配置适合页面。

## 第 1 步：创建工作簿
第一步是创建工作簿。我们将实例化一个 Workbook 对象。下面是创建工作簿的代码：

```csharp
//文档目录的路径
string dataDir = "YOUR_DIRECTORY_OF_DOCUMENTS";

//实例化工作簿对象
Workbook workbook = new Workbook();
```

## 第 2 步：访问工作表
现在我们已经创建了工作簿，我们需要导航到第一个工作表。我们将使用索引 0 访问第一个工作表。这是访问它的代码：

```csharp
//访问工作簿中的第一个工作表
Worksheet worksheet = workbook.Worksheets[0];
```

## 第 3 步：设置适合页面
在此步骤中，我们将配置对工作表页面的调整。我们将使用`FitToPagesTall`和`FitToPagesWide`的属性`PageSetup`对象来为工作表的高度和宽度指定所需的页数。下面是代码：

```csharp
//配置工作表高度的页数
worksheet.PageSetup.FitToPagesTall = 1;

//配置工作表宽度的页数
worksheet.PageSetup.FitToPagesWide = 1;
```

## 第 4 步：保存工作簿
现在我们已经配置适合页面，我们可以保存工作簿。我们将使用`Save`为此工作簿对象的方法。这是保存工作簿的代码：

```csharp
//保存工作簿
workbook.Save(dataDir + "FitToPagesOptions_out.xls");
```

### 使用 Aspose.Cells for .NET 的适合 Excel 页面选项的示例源代码 
```csharp
//文档目录的路径。
string dataDir = "YOUR DOCUMENT DIRECTORY";
//实例化工作簿对象
Workbook workbook = new Workbook();
//访问 Excel 文件中的第一个工作表
Worksheet worksheet = workbook.Worksheets[0];
//设置工作表长度将跨越的页数
worksheet.PageSetup.FitToPagesTall = 1;
//设置工作表宽度将跨越的页数
worksheet.PageSetup.FitToPagesWide = 1;
//保存工作簿。
workbook.Save(dataDir + "FitToPagesOptions_out.xls");
```

## 结论
在本文中，我们学习了如何使用 Aspose.Cells for .NET 在 Excel 中配置适合页面。我们经历了以下步骤：创建工作簿、访问工作表、配置适合页面以及保存工作簿。现在您可以使用这些知识将您的电子表格调整到所需的页面。

### 常见问题

问：如何安装 Aspose.Cells for .NET？

答：要安装 Aspose.Cells for .NET，您可以使用 Visual Studio 中的 NuGet 包管理器。找到“Aspose.Cells”包并将其安装到您的项目中。

问：我可以调整页面的高度和宽度吗？

答：是的，您可以使用`FitToPagesTall`和`FitToPagesWide`特性。您可以为每个维度指定所需的页数。

问：如何自定义适合页面选项？

答：除了指定页数外，您还可以自定义其他适合页面的选项，例如工作表比例、纸张方向、页边距等。使用中可用的属性`PageSetup`为此目的。

问：我可以使用 Aspose.Cells for .NET 来处理现有的工作簿吗？

A：是的，您可以使用 Aspose.Cells for .NET 打开和编辑现有的工作簿。您可以访问工作表、单元格、公式、样式和其他工作簿项目以执行各种操作。