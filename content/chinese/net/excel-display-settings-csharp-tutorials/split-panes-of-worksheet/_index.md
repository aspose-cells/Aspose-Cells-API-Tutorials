---
title: 工作表的拆分窗格
linktitle: 工作表的拆分窗格
second_title: Aspose.Cells for .NET API 参考
description: 使用 Aspose.Cells for .NET 在 Excel 工作表中拆分窗格的分步指南。
type: docs
weight: 130
url: /zh/net/excel-display-settings-csharp-tutorials/split-panes-of-worksheet/
---
在本教程中，我们将解释如何使用 Aspose.Cells for .NET 在 Excel 工作表中拆分窗格。请按照以下步骤操作以获得所需的结果：

## 第一步：搭建环境

确保您已安装 Aspose.Cells for .NET 并设置您的开发环境。另外，请确保您拥有要分割窗格的 Excel 文件的副本。

## 第2步：导入必要的依赖项

添加必要的指令以使用 Aspose.Cells 中的类：

```csharp
using Aspose.Cells;
```

## 第三步：代码初始化

首先初始化包含 Excel 文档的目录的路径：

```csharp
string dataDir = "YOUR DOCUMENTS DIRECTORY";
```

## 步骤 4：打开 Excel 文件

实例化一个新的`Workbook`对象并使用打开 Excel 文件`Open`方法：

```csharp
Workbook book = new Workbook(dataDir + "Book1.xls");
```

## 步骤 5：定义活动单元格

使用以下命令设置工作表的活动单元格`ActiveCell`财产：

```csharp
book.Worksheets[0].ActiveCell = "A20";
```

## 第6步：分割皮瓣

使用以下命令分割工作表窗口`Split`方法：

```csharp
book.Worksheets[0].Split();
```

## 第 7 步：保存更改

保存对 Excel 文件所做的更改：

```csharp
book.Save(dataDir + "output.xls");
```

### 使用 Aspose.Cells for .NET 分割工作表窗格的示例源代码 

```csharp
//文档目录的路径。
string dataDir = "YOUR DOCUMENT DIRECTORY";
//实例化一个新工作簿并打开模板文件
Workbook book = new Workbook(dataDir + "Book1.xls");
//设置活动单元格
book.Worksheets[0].ActiveCell = "A20";
//拆分工作表窗口
book.Worksheets[0].Split();
//保存 Excel 文件
book.Save(dataDir + "output.xls");
```

## 结论

在本教程中，您学习了如何使用 Aspose.Cells for .NET 在 Excel 工作表中拆分窗格。通过执行所述步骤，您可以轻松自定义 Excel 文件的外观和行为。

### 常见问题 (FAQ)

#### 什么是 Aspose.Cells for .NET？

Aspose.Cells for .NET 是一个流行的软件库，用于在 .NET 应用程序中操作 Excel 文件。

#### 如何在 Aspose.Cells 中设置工作表的活动单元格？

您可以使用以下命令设置活动单元格`ActiveCell`Worksheet 对象的属性。

#### 我可以只拆分工作表窗口的水平或垂直窗格吗？

是的，使用 Aspose.Cells，您只能使用适当的方法分割水平或垂直窗格，例如`SplitColumn`或者`SplitRow`.

#### Aspose.Cells 只能处理 .xls 格式的 Excel 文件吗？

不，Aspose.Cells 支持各种 Excel 文件格式，包括 .xls 和 .xlsx。