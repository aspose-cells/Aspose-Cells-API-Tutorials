---
title: 设置 PDF 保存选项的默认字体
linktitle: 设置 PDF 保存选项的默认字体
second_title: Aspose.Cells .NET Excel 处理 API
description: 了解如何使用 Aspose.Cells for .NET 设置 PDF 保存选项的默认字体，确保您的文档每次都看起来完美无缺。
type: docs
weight: 11
url: /zh/net/working-with-fonts-in-spreadsheets/set-default-font-for-pdf-save-options/
---
## 介绍
在生成 PDF 格式的报告、发票或任何其他文档时，确保内容看起来正确无误是至关重要的。字体在保持文档的视觉吸引力和可读性方面起着至关重要的作用。但是，如果您在 Excel 文件中使用的字体在生成 PDF 的系统上不可用，会发生什么情况？这就是 Aspose.Cells for .NET 派上用场的地方。这个功能强大的库允许您为 PDF 保存选项设置默认字体，确保您的文档无论在哪里打开，看起来都专业且一致。
## 先决条件
在开始之前，请确保您已准备好以下内容：
1. Visual Studio：您需要一个像 Visual Studio 这样的开发环境来编写和执行您的代码。
2.  Aspose.Cells for .NET：你可以从以下网址下载最新版本[此链接](https://releases.aspose.com/cells/net/)。或者，您可以通过 Visual Studio 中的 NuGet 包管理器安装它。
3. C# 基础知识：了解 C# 的基础知识将帮助您理解代码示例。
4. 示例 Excel 文件：准备一个示例 Excel 文件以供测试。您可以创建一个包含各种字体和样式的文件，以查看 Aspose.Cells 如何处理缺失字体。
## 导入包
在项目中使用 Aspose.Cells 之前，您需要导入必要的软件包。操作方法如下：
1. 打开您的项目：启动 Visual Studio 并打开您现有的项目或创建一个新项目。
2. 添加引用：在解决方案资源管理器中右键单击您的项目并选择“管理 NuGet 包”。
3. 安装 Aspose.Cells：搜索“Aspose.Cells”然后单击“安装”按钮。
4. 添加使用指令：在 C# 文件的顶部，包含以下命名空间：
```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using Aspose.Cells.Rendering;
using System.Drawing.Imaging;
```
## 步骤 1：设置目录
在处理文件之前，定义源目录和输出目录非常重要。这将使您更容易找到输入的 Excel 文件并保存生成的输出文件。
```csharp
//源目录
string sourceDir = "Your Document Directory";
//输出目录
string outputDir = "Your Document Directory";
```
代替`"Your Document Directory"`使用您的目录的实际路径。
## 第 2 步：打开 Excel 文件
现在我们已经设置了目录，让我们打开要处理的 Excel 文件。`Workbook` Aspose.Cells 中的类用于加载Excel文档。
```csharp
//打开 Excel 文件
Workbook workbook = new Workbook(sourceDir + "sampleSetDefaultFontPropertyOfPdfSaveOptionsAndImageOrPrintOptions.xlsx");
```
确保将文件名替换为您的实际文件名。
## 步骤 3：设置图像渲染选项
接下来，我们需要配置渲染选项，以便将 Excel 工作表转换为图像格式。我们将创建一个实例`ImageOrPrintOptions`，指定图像类型和默认字体。
```csharp
//渲染为 PNG 文件格式
ImageOrPrintOptions imgOpt = new ImageOrPrintOptions();
imgOpt.ImageType = Drawing.ImageType.Png;
imgOpt.CheckWorkbookDefaultFont = false;
imgOpt.DefaultFont = "Times New Roman";
```
在此代码片段中，我们设置`CheckWorkbookDefaultFont`财产`false`，这意味着如果缺少任何字体，则将使用指定的默认字体（“Times New Roman”）。
## 步骤 4：将工作表渲染为图像
现在，让我们将工作簿的第一张表渲染为 PNG 图像。我们将使用`SheetRender`类来完成此操作。
```csharp
//将第一个工作表渲染为图像
SheetRender sr = new SheetRender(workbook.Worksheets[0], imgOpt);
sr.ToImage(0, outputDir + "out1_imagePNG.png");
```
## 步骤 5：更改图像类型并渲染为 TIFF
如果你想将同一张表渲染为不同的图像格式，比如 TIFF，你可以简单地更改`ImageType`属性并重复渲染过程。
```csharp
//设置为 TIFF 格式
imgOpt.ImageType = Drawing.ImageType.Tiff;
WorkbookRender wr = new WorkbookRender(workbook, imgOpt);
wr.ToImage(outputDir + "out1_imageTIFF.tiff");
```
## 步骤 6：配置 PDF 保存选项
接下来，让我们设置 PDF 保存选项。我们将创建一个实例`PdfSaveOptions`，设置默认字体，并指定我们要检查缺少的字体。
```csharp
//配置 PDF 保存选项
PdfSaveOptions saveOptions = new PdfSaveOptions();
saveOptions.DefaultFont = "Times New Roman";
saveOptions.CheckWorkbookDefaultFont = false;
```
## 步骤 7：将工作簿另存为 PDF
配置完保存选项后，就可以将我们的 Excel 工作簿保存为 PDF 文件了。 
```csharp
//将工作簿保存为 PDF
workbook.Save(outputDir + "out1_pdf.pdf", saveOptions);
```
## 步骤8：确认执行
最后，让用户知道该过程已成功完成是一种很好的做法。您可以使用简单的控制台消息来实现这一点。
```csharp
Console.WriteLine("SetDefaultFontPropertyOfPdfSaveOptionsAndImageOrPrintOptions executed successfully.\r\n");
```
## 结论
Aspose.Cells 提供了一种灵活而强大的方法来处理 Excel 文件操作，使开发人员能够更轻松地创建具有视觉吸引力且保留其格式的文档。无论您是在处理报告、财务文档还是任何其他形式的数据呈现，控制字体渲染都可以显著提高您的输出质量。
## 常见问题解答
### 什么是 Aspose.Cells？
Aspose.Cells 是一个功能强大的 .NET 库，允许开发人员操作 Excel 文件，而无需安装 Microsoft Excel。它支持各种文件格式，并提供丰富的电子表格处理功能。
### 如何为我的 Excel 文件设置默认字体？
您可以使用`PdfSaveOptions`类并指定所需的字体名称。这可确保即使缺少字体，您的文档也会使用您指定的默认字体。
### 我可以将 Excel 文件转换为 PDF 以外的格式吗？
当然！Aspose.Cells 允许您将 Excel 文件转换为各种格式，包括图像 (PNG、TIFF)、HTML、CSV 等。
### Aspose.Cells 可以免费使用吗？
Aspose.Cells 是一款商业产品，但您可以免费试用有限试用版。要使用完整功能，您需要购买许可证。
### 在哪里可以找到对 Aspose.Cells 的支持？
您可以通过访问以下网站获取对 Aspose.Cells 的支持[Aspose 论坛](https://forum.aspose.com/c/cells/9)，您可以在此提出问题并与其他用户和开发人员分享见解。