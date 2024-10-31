---
title: 保存为 HTML 时禁用下级显示评论
linktitle: 保存为 HTML 时禁用下级显示评论
second_title: Aspose.Cells .NET Excel 处理 API
description: 通过详细的分步指南了解如何在使用 Aspose.Cells for .NET 将 Excel 工作簿保存为 HTML 时禁用下层显示的注释。
type: docs
weight: 11
url: /zh/net/loading-and-saving-excel-files-with-options/disabling-downlevel-revealed-comments/
---
## 介绍
您是否曾经需要将 Excel 工作簿转换为 HTML，并希望确保在此过程中不会显示任何不必要的注释或隐藏内容？这时，禁用下级显示注释就派上用场了。如果您使用的是 Aspose.Cells for .NET，则可以完全控制 Excel 工作簿如何呈现为 HTML 文件。在本教程中，我们将引导您完成一个简单的分步指南，帮助您在将工作簿保存为 HTML 时禁用下级显示注释。 
在本文结束时，您将清楚地了解如何使用此功能并确保您的 HTML 输出干净且无注释。
## 先决条件
在深入了解分步指南之前，让我们先介绍一下顺利进行操作所需准备的一些事项：
1.  Aspose.Cells for .NET：您需要安装 Aspose.Cells 库。如果您尚未安装，可以下载[这里](https://releases.aspose.com/cells/net/).
2. IDE：像 Visual Studio 这样的开发环境，用于编写和执行 C# 代码。
3. C# 基础知识：熟悉 C# 语法和面向对象编程将帮助您理解代码。
4. 临时或许可版本：您可以使用免费试用版，也可以从申请临时许可证[这里](https://purchase.aspose.com/temporary-license/).这确保了图书馆可以不受任何限制地工作。
现在您已经准备好了，让我们开始吧！
## 导入命名空间
在开始代码示例之前，必须包含 Aspose.Cells 所需的命名空间。如果没有这些，您的代码将无法访问操作 Excel 文件所需的方法和属性。
```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
```
确保将此行放在 C# 文件的顶部以导入 Aspose.Cells 命名空间。
## 步骤 1：设置目录路径
首先，我们需要设置源目录（存储 Excel 文件的位置）和输出目录（保存 HTML 文件的位置）。这很重要，因为 Aspose.Cells 需要准确的文件路径来访问和保存文件。
```csharp
// Excel 文件所在的源目录
string sourceDir = "Your Document Directory";
//保存生成的 HTML 文件的输出目录
string outputDir = "Your Document Directory";
```
在此步骤中，替换`"Your Document Directory"`使用系统上的实际文件路径。您还可以创建自定义目录以更好地组织输入和输出文件。
## 步骤 2：加载 Excel 工作簿
在此步骤中，我们将 Excel 工作簿加载到内存中，以便对其进行操作。为了演示目的，我们将使用名为`"sampleDisableDownlevelRevealedComments.xlsx"`您可以使用任何您喜欢的工作簿。
```csharp
//从源目录加载示例工作簿
Workbook wb = new Workbook(sourceDir + "sampleDisableDownlevelRevealedComments.xlsx");
```
这将创建一个 Workbook 对象，其中包含 Excel 文件的所有数据和结构。在这里，您可以修改它、应用设置，并最终以不同的格式保存它。
## 步骤 3：设置 HTML 保存选项
现在，我们需要配置 HtmlSaveOptions 对象以禁用向下显示的评论。此选项可确保任何评论或隐藏内容不会显示在生成的 HTML 文件中。
```csharp
//创建一个新的 HtmlSaveOptions 对象来配置保存选项
HtmlSaveOptions opts = new HtmlSaveOptions();
//禁用下级显示的评论
opts.DisableDownlevelRevealedComments = true;
```
通过设置`DisableDownlevelRevealedComments`到`true`，您确保在将工作簿保存为 HTML 文件时，任何下级注释都将被禁用。
## 步骤 4：将工作簿保存为 HTML
配置 HtmlSaveOptions 对象后，下一步是使用指定的选项将工作簿保存为 HTML。这是实际文件转换发生的地方。
```csharp
//使用指定的保存选项将工作簿保存为 HTML 文件
wb.Save(outputDir + "outputDisableDownlevelRevealedComments_true.html", opts);
```
在这行代码中，我们将工作簿保存到您之前指定的输出目录，并应用 DisableDownlevelRevealedComments 设置。结果将是一个干净的 HTML 文件，没有任何不需要的注释。
## 步骤 5：验证并执行
最后，为了确保一切都按预期工作，您可以向控制台输出成功消息。
```csharp
//向控制台输出成功消息
Console.WriteLine("DisableDownlevelRevealedCommentsWhileSavingToHTML executed successfully.");
```
这让您知道操作已完成且没有错误。
## 结论
就这样！您已成功学会了如何在使用 Aspose.Cells for .NET 将 Excel 工作簿保存为 HTML 时禁用下级显示注释。借助此功能，您现在可以控制工作簿如何呈现为 HTML 并避免显示任何不必要的内容。无论您是在开发 Web 应用程序还是只需要干净的 HTML 输出，此方法都可以确保您的工作簿转换准确且安全。
如果您发现本教程有用，请考虑探索 Aspose.Cells 的其他功能，以进一步增强您的 Excel 处理能力。
## 常见问题解答
### 什么是下级揭露的评论？
下级显示注释通常用于 Web 开发，以便为不支持某些 HTML 功能的旧版浏览器提供额外信息。在 Excel 到 HTML 的转换中，它们有时会显示隐藏的内容或注释，因此禁用它们会很有用。
### 如果我需要的话，可以启用下级评论吗？
是的，只需设置`DisableDownlevelRevealedComments`财产`false`如果您想在将工作簿保存为 HTML 时启用下级注释。
### 如何获取 Aspose.Cells 的临时许可证？
您可以通过访问以下网站轻松申请临时驾照：[Aspose 网站](https://purchase.aspose.com/temporary-license/).
### 禁用下级注释会影响 HTML 的外观吗？
不会，禁用下层显示的注释不会影响 HTML 输出的视觉效果。它只会阻止显示旧版浏览器所需的额外信息。
### 除了 HTML 之外，我还能将工作簿保存为其他格式吗？
是的，Aspose.Cells 支持多种输出格式，如 PDF、CSV 和 TXT。您可以在[文档](https://reference.aspose.com/cells/net/).