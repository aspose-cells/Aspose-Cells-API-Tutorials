---
title: 检测链接类型
linktitle: 检测链接类型
second_title: Aspose.Cells for .NET API 参考
description: 使用 Aspose.Cells for .NET 检测 Excel 工作簿中的链接类型。
type: docs
weight: 80
url: /zh/net/excel-workbook/detect-link-types/
---
在本教程中，我们将逐步引导您完成所提供的 C# 源代码，使您能够使用 Aspose.Cells for .NET 检测 Excel 工作簿中的链接类型。请按照以下步骤执行此操作。

## 第1步：设置源目录

```csharp
//源目录
string SourceDir = RunExamples.Get_SourceDirectory();
```

在第一步中，我们定义包含链接的 Excel 工作簿所在的源目录。

## 第 2 步：加载 Excel 工作簿

```csharp
//加载 Excel 工作簿
Workbook workbook = new Workbook(SourceDir + "LinkTypes.xlsx");
```

我们使用源文件路径加载 Excel 工作簿。

## 第 3 步：获取电子表格

```csharp
//获取第一个工作表（默认）
Worksheet worksheet = workbook.Worksheets[0];
```

我们得到工作簿的第一个工作表。您可以更改`[0]`如果需要，可以使用索引来访问特定的工作表。

## 步骤 4：创建单元格范围

```csharp
//创建单元格区域 A1:B3
Range range = worksheet.Cells.CreateRange("A1", "A7");
```

我们创建一系列单元格，在此示例中从单元格 A1 到单元格 A7。您可以根据需要调整单元格引用。

## 第五步：获取范围内的超链接

```csharp
//获取范围内的超链接
Hyperlink[] hyperlinks = range.Hyperlinks;
```

我们获得指定范围内存在的所有超链接。

## 步骤 6：浏览超链接并查看链接类型

```csharp
foreach (Hyperlink link in hyperlinks)
{
Console.WriteLine(link.TextToDisplay + ": " + link.LinkType);
}
```

我们循环遍历每个链接并显示显示文本和关联的链接类型。

### 使用 Aspose.Cells for .NET 检测链接类型的示例源代码 
```csharp
//源目录
string SourceDir = RunExamples.Get_SourceDirectory();
Workbook workbook = new Workbook(SourceDir + "LinkTypes.xlsx");
//获取第一个（默认）工作表
Worksheet worksheet = workbook.Worksheets[0];
//创建范围 A2:B3
Range range = worksheet.Cells.CreateRange("A1", "A7");
//获取范围内的超链接
Hyperlink[] hyperlinks = range.Hyperlinks;
foreach (Hyperlink link in hyperlinks)
{
	Console.WriteLine(link.TextToDisplay + ": " + link.LinkType);
}
Console.WriteLine("DetectLinkTypes executed successfully.");
```

## 结论

恭喜！您已了解如何使用 Aspose.Cells for .NET 检测 Excel 工作簿中的链接类型。此功能允许您使用 Excel 工作簿中的超链接。不断探索 Aspose.Cells 的功能来扩展您的 Excel 工作簿处理能力。

### 常见问题解答

#### 问：如何在我的项目中安装 Aspose.Cells for .NET？

答：您可以使用 NuGet 包管理器安装 Aspose.Cells for .NET。搜索[Aspose 发布](https://releases.aspose.com/cells/net)在 NuGet 包管理器控制台中并安装最新版本。

#### 问：我可以检测特定工作表而不是第一个工作表中的链接类型吗？

答：是的，您可以修改`workbook.Worksheets[0]`用于访问特定工作表的索引。例如，要访问第二张表，请使用`workbook.Worksheets[1]`.

#### 问：是否可以修改范围内检测到的链接类型？

答：是的，您可以浏览超链接并执行编辑操作，例如更新 URL 或删除不需要的链接。

#### 问：Aspose.Cells for .NET 中可以使用哪些类型的链接？

答：可能的链接类型包括超链接、其他工作表的链接、外部文件的链接、网站的链接等。

#### 问：Aspose.Cells for .NET 支持在电子表格中创建新链接吗？

答：是的，Aspose.Cells for .NET 支持使用以下命令创建新链接`Hyperlink`类及其相关属性。您可以添加超链接、URL 链接、其他电子表格的链接等。

#### 问：我可以在 Web 应用程序中使用 Aspose.Cells for .NET 吗？

答：是的，Aspose.Cells for .NET 可以在 Web 应用程序中使用。您可以将其嵌入到 ASP.NET、ASP.NET Core 和其他基于 .NET 的 Web 框架中。

#### 问：使用 Aspose.Cells for .NET 时有文件大小限制吗？

答：Aspose.Cells for .NET 可以处理大型 Excel 工作簿，没有特定限制。但是，实际文件大小可能受到可用系统资源的限制。