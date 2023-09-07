---
title: 设置 Excel 打印选项
linktitle: 设置 Excel 打印选项
second_title: Aspose.Cells for .NET API 参考
description: 学习使用 Aspose.Cells for .NET 轻松操作 Excel 文件并自定义打印选项。
type: docs
weight: 150
url: /zh/net/excel-page-setup/set-excel-print-options/
---
在本指南中，我们将引导您了解如何使用 Aspose.Cells for .NET 设置 Excel 工作簿的打印选项。我们将引导您逐步完成所提供的 C# 源代码来完成此任务。

## 第一步：搭建环境

在开始之前，请确保您已设置开发环境并安装了 Aspose.Cells for .NET。您可以从Aspose官方网站下载最新版本的库。

## 第2步：导入所需的命名空间

在您的 C# 项目中，导入必要的命名空间以使用 Aspose.Cells：

```csharp
using Aspose.Cells;
```

## 第三步：设置文档目录路径

声明一个`dataDir`变量来指定要保存生成的 Excel 文件的目录的路径：

```csharp
string dataDir = "YOUR_DIRECTORY_OF_DOCUMENTS";
```

一定要更换`"YOUR_DOCUMENT_DIRECTORY"`与系统上的正确路径。

## 第 4 步：创建工作簿对象

实例化一个代表要创建的 Excel 工作簿的 Workbook 对象：

```csharp
Workbook workbook = new Workbook();
```

## 步骤5：获取工作表的PageSetup引用

要设置打印选项，我们首先需要从工作表中获取 PageSetup 引用。使用以下代码获取参考：

```csharp
PageSetup pageSetup = workbook.Worksheets[0].PageSetup;
```

## 第 6 步：启用打印网格线

要打印网格线，请使用以下代码：

```csharp
pageSetup. PrintGridlines = true;
```

## 步骤 7：启用行/列标题打印

要启用行标题和列标题的打印，请使用以下代码：

```csharp
pageSetup.PrintHeadings = true;
```

## 步骤 8：启用黑白打印模式

要启用黑白模式打印工作表，请使用以下代码：

```csharp
pageSetup.BlackAndWhite = true;
```

## 第9步：启用反馈打印

要允许打印出现在电子表格上的注释，请使用以下代码：

```csharp
pageSetup.PrintComments = PrintCommentsType.PrintInPlace;
```

## 步骤 10：启用草稿模式打印

要在草稿模式下打印电子表格，请使用以下代码：

```csharp
pageSetup.PrintDraft = true;
```

## 步骤 11：启用打印单元格错误为 N/A

允许将单元格错误打印为

  如果不适用，请使用以下代码：

```csharp
pageSetup.PrintErrors = PrintErrorsType.PrintErrorsNA;
```

## 第 12 步：保存 Excel 工作簿

要保存设置了打印选项的 Excel 工作簿，请使用`Save`Workbook对象的方法：

```csharp
workbook.Save(dataDir + "OtherPrintOptions_out.xls");
```

这会将 Excel 工作簿保存在指定目录中，文件名为“OtherPrintOptions_out.xls”。

### 使用 Aspose.Cells for .NET 设置 Excel 打印选项的示例源代码 
```csharp
//文档目录的路径。
string dataDir = "YOUR DOCUMENT DIRECTORY";
//实例化 Workbook 对象
Workbook workbook = new Workbook();
//获取工作表PageSetup的引用
PageSetup pageSetup = workbook.Worksheets[0].PageSetup;
//允许打印网格线
pageSetup.PrintGridlines = true;
//允许打印行/列标题
pageSetup.PrintHeadings = true;
//允许以黑白模式打印工作表
pageSetup.BlackAndWhite = true;
//允许打印工作表上显示的注释
pageSetup.PrintComments = PrintCommentsType.PrintInPlace;
//允许以草稿质量打印工作表
pageSetup.PrintDraft = true;
//允许将单元格错误打印为 N/A
pageSetup.PrintErrors = PrintErrorsType.PrintErrorsNA;
//保存工作簿。
workbook.Save(dataDir + "OtherPrintOptions_out.xls");
```
## 结论

您现在已经了解了如何使用 Aspose.Cells for .NET 设置 Excel 工作簿的打印选项。这个功能强大且用户友好的库允许您以简单有效的方式自定义 Excel 工作簿的打印设置。

### 常见问题解答


#### 1. 我可以进一步自定义打印选项，例如边距或页面方向吗？

是的，Aspose.Cells for .NET 提供了广泛的可自定义打印选项，例如边距、页面方向、比例等。

#### 2. Aspose.Cells for .NET支持其他Excel文件格式吗？

是的，Aspose.Cells for .NET 支持多种 Excel 文件格式，例如 XLSX、XLS、CSV、HTML、PDF 等。

#### 3. Aspose.Cells for .NET 是否与所有版本的.NET Framework 兼容？

Aspose.Cells for .NET 与 .NET Framework 2.0 或更高版本兼容，包括版本 3.5、4.0、4.5、4.6 等。