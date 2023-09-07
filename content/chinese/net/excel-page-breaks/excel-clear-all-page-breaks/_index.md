---
title: Excel 清除所有分页符
linktitle: Excel 清除所有分页符
second_title: Aspose.Cells for .NET API 参考
description: 了解如何使用 Aspose.Cells for .NET 删除 Excel 中的所有分页符。清理 Excel 文件的分步教程。
type: docs
weight: 20
url: /zh/net/excel-page-breaks/excel-clear-all-page-breaks/
---

删除 Excel 文件中的分页符是处理报表或电子表格时的重要步骤。在本教程中，我们将引导您逐步理解和实现所提供的 C# 源代码，以使用适用于 .NET 的 Aspose.Cells 库删除 Excel 文件中的所有分页符。

## 第一步：准备环境

开始之前，请确保您的计算机上安装了 Aspose.Cells for .NET。您可以从以下位置下载该库[Aspose 发布](https://releases.aspose.com/cells/net)并按照提供的说明进行安装。

安装完成后，在您首选的集成开发环境 (IDE) 中创建一个新的 C# 项目，并导入适用于 .NET 的 Aspose.Cells 库。

## 第二步：配置文档目录路径

在提供的源代码中，您需要指定要保存生成的Excel文件的目录路径。修改`dataDir`变量，将“YOUR DOCUMENT DIRECTORY”替换为计算机上目录的绝对路径。

```csharp
//文档目录的路径。
string dataDir = "PATH TO YOUR DOCUMENTS DIRECTORY";
```

## 第 3 步：创建工作簿对象

首先，我们需要创建一个代表 Excel 文件的 Workbook 对象。这可以使用 Aspose.Cells 提供的 Workbook 类来实现。

```csharp
//实例化 Workbook 对象
Workbook workbook = new Workbook();
```

## 步骤 4：删除分页符

现在我们要删除 Excel 工作表中的所有分页符。在示例代码中，我们使用`Clear()`水平和垂直分页符的方法将其全部删除。

```csharp
workbook.Worksheets[0].HorizontalPageBreaks.Clear();
workbook.Worksheets[0].VerticalPageBreaks.Clear();
```

## 第 5 步：保存 Excel 文件

删除所有分页符后，我们可以保存最终的 Excel 文件。使用`Save()`方法来指定输出文件的完整路径。

```csharp
//保存 Excel 文件。
workbook.Save(dataDir + "ClearingPageBreaks_out.xls");
```

### 使用 Aspose.Cells for .NET 清除所有分页符的 Excel 示例源代码 

```csharp

//文档目录的路径。
string dataDir = "YOUR DOCUMENT DIRECTORY";
//实例化 Workbook 对象
Workbook workbook = new Workbook();
//清除所有分页符
workbook.Worksheets[0].HorizontalPageBreaks.Clear();
workbook.Worksheets[0].VerticalPageBreaks.Clear();
//保存 Excel 文件。
workbook.Save(dataDir + "ClearAllPageBreaks_out.xls");

```

## 结论

在本教程中，我们学习了如何使用 Aspose.Cells for .NET 删除 Excel 文件中的所有分页符。通过按照提供的步骤操作，您可以轻松管理和清理动态生成的 Excel 文件中不需要的分页符。请随意进一步探索 Aspose.Cells 提供的功能以实现更高级的操作。

### 常见问题解答

#### 问：Aspose.Cells for .NET 是免费库吗？

答：Aspose.Cells for .NET 是一个商业库，但它提供了免费试用版，您可以使用它来评估其功能。

#### 问：删除分页符是否会影响其他工作表元素？

答：不会，删除分页符只会更改分页符本身，不会影响工作表中的任何其他数据或格式。

#### 问：我可以有选择地删除 Excel 中的某些特定分页符吗？

答：是的，使用 Aspose.Cells，您可以单独访问每个分页符，并在需要时使用适当的方法将其删除。

#### 问：Aspose.Cells for .NET 支持哪些其他 Excel 文件格式？

答：Aspose.Cells for .NET 支持各种 Excel 文件格式，例如 XLSX、XLSM、CSV、HTML、PDF 等。

