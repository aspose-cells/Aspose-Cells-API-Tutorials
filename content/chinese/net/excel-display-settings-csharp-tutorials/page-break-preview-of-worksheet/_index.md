---
title: 工作表的分页预览
linktitle: 工作表的分页预览
second_title: Aspose.Cells for .NET API 参考
description: 使用 Aspose.Cells for .NET 显示工作表分页预览的分步指南。
type: docs
weight: 110
url: /zh/net/excel-display-settings-csharp-tutorials/page-break-preview-of-worksheet/
---
在本教程中，我们将解释如何使用 Aspose.Cells for .NET 显示工作表的分页符预览。请按照以下步骤操作以获得所需的结果：

## 第一步：搭建环境

确保您已安装 Aspose.Cells for .NET 并设置您的开发环境。另外，请确保您拥有要在其上显示分页符预览的 Excel 文件的副本。

## 第2步：导入必要的依赖项

添加必要的指令以使用 Aspose.Cells 中的类：

```csharp
using Aspose.Cells;
using System.IO;
```

## 第三步：代码初始化

首先初始化包含 Excel 文档的目录的路径：

```csharp
string dataDir = "YOUR DOCUMENTS DIRECTORY";
```

## 步骤 4：打开 Excel 文件

创建一个`FileStream`包含要打开的 Excel 文件的对象：

```csharp
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
```

实例化一个`Workbook`对象并使用文件流打开 Excel 文件：

```csharp
Workbook workbook = new Workbook(fstream);
```

## 第 5 步：访问电子表格

导航到 Excel 文件中的第一个工作表：

```csharp
Worksheet worksheet = workbook.Worksheets[0];
```

## 步骤 6：显示分页预览

启用电子表格的分页预览：

```csharp
worksheet. IsPageBreakPreview = true;
```

## 第 7 步：保存更改

保存对 Excel 文件所做的更改：

```csharp
workbook.Save(dataDir + "output.xls");
```

## 第8步：关闭文件流

关闭文件流以释放所有资源：

```csharp
fstream.Close();
```

### 使用 Aspose.Cells for .NET 进行工作表分页预览的示例源代码 
```csharp
//文档目录的路径。
string dataDir = "YOUR DOCUMENT DIRECTORY";
//创建包含要打开的 Excel 文件的文件流
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
//实例化 Workbook 对象
//通过文件流打开Excel文件
Workbook workbook = new Workbook(fstream);
//访问 Excel 文件中的第一个工作表
Worksheet worksheet = workbook.Worksheets[0];
//在分页预览中显示工作表
worksheet.IsPageBreakPreview = true;
//保存修改后的Excel文件
workbook.Save(dataDir + "output.xls");
//关闭文件流以释放所有资源
fstream.Close();
```

## 结论

在本教程中，您学习了如何使用 Aspose.Cells for .NET 显示工作表的分页符预览。通过执行所述步骤，您可以轻松控制 Excel 文件的外观和布局。

### 常见问题 (FAQ)

#### 什么是 Aspose.Cells for .NET？

Aspose.Cells for .NET 是一个流行的软件库，用于在 .NET 应用程序中操作 Excel 文件。

#### 我可以显示特定工作表而不是整个工作表的逐页预览吗？

是的，使用 Aspose.Cells，您可以通过访问相应的 Worksheet 对象来启用特定工作表的分页预览。

#### Aspose.Cells 是否支持其他 Excel 文件编辑功能？

是的，Aspose.Cells 提供了广泛的编辑和操作 Excel 文件的功能，例如添加数据、格式化、创建图表等。

#### Aspose.Cells 只能处理 .xls 格式的 Excel 文件吗？

不，Aspose.Cells 支持各种 Excel 文件格式，包括 .xls 和 .xlsx。
	