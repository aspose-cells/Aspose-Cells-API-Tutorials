---
title: 获取工作表打印的纸张宽度和高度
linktitle: 获取工作表打印的纸张宽度和高度
second_title: Aspose.Cells .NET Excel 处理 API
description: 通过本分步指南了解如何在 Aspose.Cells for .NET 中获取用于工作表打印的纸张宽度和高度。
type: docs
weight: 16
url: /zh/net/worksheet-display/get-paper-width-height/
---
## 介绍
准确打印文档需要了解纸张的尺寸。如果您是开发人员或正在开发处理 Excel 文件的应用程序，您可能需要知道如何在打印工作表时获取纸张的宽度和高度。幸运的是，Aspose.Cells for .NET 提供了一种强大的方法来以编程方式管理 Excel 文档。在本文中，我们将指导您完成确定纸张尺寸细节的过程，并使用简单示例来说明基本概念。 
## 先决条件
在深入讨论技术细节之前，让我们先做一些基础工作。要成功完成本教程，您需要：
### 1. C# 基础知识
您应该很好地掌握 C# 编程，因为我们将在 .NET 环境中工作。
### 2. Aspose.Cells 库
确保你的项目中安装了 Aspose.Cells 库。如果你还没有安装，你可以从[Aspose.Cells 下载页面](https://releases.aspose.com/cells/net/).
### 3.Visual Studio IDE
使用 Visual Studio 来运行和管理 C# 项目非常有益。任何支持 .NET 的版本都可以很好地运行。
### 4.有效的 Aspose 许可证
虽然 Aspose.Cells 可以试用，但如果您打算将其用于长期项目，请考虑购买许可证。您可以通过[此链接](https://purchase.aspose.com/buy)或探索[临时执照](https://purchase.aspose.com/temporary-license/)用于短暂的测试阶段。
一切准备就绪后，我们就开始编写代码吧！
## 导入包
我们旅程的第一步是导入必要的命名空间。这至关重要，因为它使我们能够访问用于操作 Excel 文件的类和方法。操作方法如下：
```csharp
using System;
using System.IO;
using Aspose.Cells;
```
确保将此行包含在 .cs 文件的顶部。现在我们已经准备好导入，让我们继续创建工作簿并访问工作表。
## 步骤 1：创建工作簿
我们首先创建一个`Workbook`类。这构成了我们操作 Excel 文件的基础。
```csharp
Workbook wb = new Workbook();
```
此行告诉程序初始化一个新的工作簿，让我们能够深入研究工作表。
## 第 2 步：访问第一个工作表
接下来，我们将访问新创建的工作簿中的第一个工作表。这非常简单：
```csharp
Worksheet ws = wb.Worksheets[0];
```
这里，我们访问工作簿中的第一个工作表（索引为 0）。我们将在这里设置纸张尺寸。
## 设置纸张大小并检索尺寸
现在我们进入操作的核心 — 设置纸张尺寸并检索其尺寸！让我们一步一步地分解。
## 步骤 3：将纸张尺寸设置为 A2
让我们首先将纸张尺寸设置为 A2 并打印出其尺寸。
```csharp
ws.PageSetup.PaperSize = PaperSizeType.PaperA2;
Console.WriteLine("PaperA2: " + ws.PageSetup.PaperWidth + "x" + ws.PageSetup.PaperHeight);
```
完成此设置后，我们使用`Console.WriteLine`显示尺寸。运行此命令后，您将看到 A2 纸张尺寸的宽度和高度（以英寸为单位）。
## 步骤 4：将纸张尺寸设置为 A3
现在到了 A3 的时间！我们只需重复该过程：
```csharp
ws.PageSetup.PaperSize = PaperSizeType.PaperA3;
Console.WriteLine("PaperA3: " + ws.PageSetup.PaperWidth + "x" + ws.PageSetup.PaperHeight);
```
瞧！声明将打印 A3 纸的具体高度和宽度。
## 步骤 5：将纸张尺寸设置为 A4
按照同样的模式，我们来看看 A4 的表现如何：
```csharp
ws.PageSetup.PaperSize = PaperSizeType.PaperA4;
Console.WriteLine("PaperA4: " + ws.PageSetup.PaperWidth + "x" + ws.PageSetup.PaperHeight);
```
这样我们就得到了 A4 的尺寸——最常用的纸张尺寸之一。
## 步骤 6：将纸张尺寸设置为 Letter
为了完善我们的纸张尺寸探索，我们将其设置为信纸尺寸：
```csharp
ws.PageSetup.PaperSize = PaperSizeType.PaperLetter;
Console.WriteLine("PaperLetter: " + ws.PageSetup.PaperWidth + "x" + ws.PageSetup.PaperHeight);
```
再次，我们将看到 Letter 尺寸的具体宽度和高度。
## 结论
就这样！您刚刚学会了如何在使用 Aspose.Cells for .NET 准备要打印的工作表时获取各种尺寸的纸张宽度和高度。此实用程序非常有用，尤其是当您计划打印布局或以编程方式管理打印设置时。通过了解英寸的确切尺寸，您可以避免常见的陷阱并确保您的文档按预期打印出来。
## 常见问题解答
### 什么是 Aspose.Cells？
Aspose.Cells 是一个.NET 库，它提供了一系列以编程方式处理 Excel 文件的功能。
### 如何开始使用 Aspose.Cells？
首先从[Aspose 网站](https://releases.aspose.com/cells/net/)并按照文档在您的项目中进行设置。
### 我可以免费使用 Aspose.Cells 吗？
Aspose.Cells 提供试用版，您可以试用以探索其功能。如需长期使用，则需要购买许可证。
### Aspose.Cells 支持哪些纸张尺寸？
Aspose.Cells 支持各种纸张尺寸，包括 A2、A3、A4、Letter 等。
### 在哪里可以找到有关 Aspose.Cells 的更多资源或支持？
您可以检查[Aspose 论坛](https://forum.aspose.com/c/cells/9)寻求社区帮助和[文档](https://reference.aspose.com/cells/net/)获取教程和参考资料。