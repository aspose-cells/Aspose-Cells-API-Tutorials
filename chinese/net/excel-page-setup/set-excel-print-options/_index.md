---
title: 设置 Excel 打印选项
linktitle: 设置 Excel 打印选项
second_title: Aspose.Cells for .NET API 参考
description: 使用 Aspose.Cells for .NET 轻松学习操作 Excel 文件和自定义打印选项。
type: docs
weight: 150
url: /zh/net/excel-page-setup/set-excel-print-options/
---
在本指南中，我们将带您了解如何使用 Aspose.Cells for .NET 为 Excel 工作簿设置打印选项。我们将带您逐步完成提供的 C# 源代码以完成此任务。

## 第 1 步：设置环境

在开始之前，请确保您已经设置了开发环境并安装了 Aspose.Cells for .NET。你可以从Aspose官网下载最新版本的库。

## 第 2 步：导入所需的命名空间

在您的 C# 项目中，导入必要的命名空间以使用 Aspose.Cells：

```csharp
using Aspose.Cells;
```

## 第三步：设置文档目录的路径

声明一个`dataDir`变量指定要保存生成的 Excel 文件的目录路径：

```csharp
string dataDir = "YOUR_DIRECTORY_OF_DOCUMENTS";
```

务必更换`"YOUR_DOCUMENT_DIRECTORY"`在您的系统上使用正确的路径。

## 第 4 步：创建工作簿对象

实例化一个代表您要创建的 Excel 工作簿的 Workbook 对象：

```csharp
Workbook workbook = new Workbook();
```

## 第五步：获取工作表的PageSetup引用

要设置打印选项，我们首先需要从工作表中获取 PageSetup 引用。使用以下代码获取参考：

```csharp
PageSetup pageSetup = workbook.Worksheets[0].PageSetup;
```

## 第 6 步：启用打印网格线

要启用要打印的网格线，请使用以下代码：

```csharp
pageSetup. PrintGridlines = true;
```

## 步骤 7：启用行/列标题打印

要启用行和列标题的打印，请使用以下代码：

```csharp
pageSetup.PrintHeadings = true;
```

## 步骤 8：启用黑白打印模式

要以黑白模式打印工作表，请使用以下代码：

```csharp
pageSetup.BlackAndWhite = true;
```

## 步骤 9：启用反馈打印

要允许在电子表格中显示评论，请使用以下代码：

```csharp
pageSetup.PrintComments = PrintCommentsType.PrintInPlace;
```

## 步骤 10：启用草稿模式打印

要启用以草稿模式打印电子表格，请使用以下代码：

```csharp
pageSetup.PrintDraft = true;
```

## 第 11 步：启用打印单元格错误作为 N/A

允许将单元格错误打印为

  比 N/A，使用以下代码：

```csharp
pageSetup.PrintErrors = PrintErrorsType.PrintErrorsNA;
```

## 第 12 步：保存 Excel 工作簿

要保存设置了打印选项的 Excel 工作簿，请使用`Save`工作簿对象的方法：

```csharp
workbook.Save(dataDir + "OtherPrintOptions_out.xls");
```

这将在指定目录中保存文件名为“OtherPrintOptions_out.xls”的 Excel 工作簿。

### 使用 Aspose.Cells for .NET 设置 Excel 打印选项的示例源代码 
```csharp
//文档目录的路径。
string dataDir = "YOUR DOCUMENT DIRECTORY";
//实例化工作簿对象
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

您现在已经学习了如何使用 Aspose.Cells for .NET 为 Excel 工作簿设置打印选项。这个功能强大且用户友好的库允许您以简单高效的方式自定义 Excel 工作簿的打印设置。

### 常见问题


#### 1. 我能否进一步自定义打印选项，例如页边距或页面方向？

是的，Aspose.Cells for .NET 提供了广泛的可定制打印选项，例如页边距、页面方向、比例等。

#### 2. Aspose.Cells for .NET 是否支持其他Excel文件格式？

是的，Aspose.Cells for .NET 支持多种 Excel 文件格式，例如 XLSX、XLS、CSV、HTML、PDF 等。

#### 3. Aspose.Cells for .NET 是否兼容所有版本的.NET Framework？

Aspose.Cells for .NET兼容.NET Framework 2.0或更新版本，包括3.5、4.0、4.5、4.6等版本。