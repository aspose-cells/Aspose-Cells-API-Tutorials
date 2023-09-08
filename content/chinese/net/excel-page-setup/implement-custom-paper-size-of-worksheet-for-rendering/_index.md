---
title: 实现工作表的自定义纸张尺寸以进行渲染
linktitle: 实现工作表的自定义纸张尺寸以进行渲染
second_title: Aspose.Cells for .NET API 参考
description: 使用 Aspose.Cells for .NET 实现自定义工作表大小的分步指南。设置尺寸、添加消息并另存为 PDF。
type: docs
weight: 50
url: /zh/net/excel-page-setup/implement-custom-paper-size-of-worksheet-for-rendering/
---
当您想要创建具有特定尺寸的 PDF 文档时，为工作表实现自定义尺寸非常有用。在本教程中，我们将学习如何使用 Aspose.Cells for .NET 设置工作表的自定义大小，然后将文档另存为 PDF。

## 第 1 步：创建输出文件夹

开始之前，您需要创建一个输出文件夹，用于保存生成的 PDF 文件。您可以为输出文件夹使用任何您想要的路径。

```csharp
//输出目录
string outputDir = "YOUR_OUTPUT_FOLDER";
```

确保指定输出文件夹的正确路径。

## 第 2 步：创建 Workbook 对象

首先，您需要使用 Aspose.Cells 创建一个 Workbook 对象。该对象代表您的电子表格。

```csharp
//创建工作簿对象
Workbook wb = new Workbook();
```

## 第 3 步：访问第一个工作表

创建 Workbook 对象后，您可以访问其中的第一个工作表。

```csharp
//访问第一个工作表
Worksheet ws = wb.Worksheets[0];
```

## 步骤 4：设置自定义工作表大小

现在您可以使用设置自定义工作表大小`CustomPaperSize(width, height)`PageSetup 类的方法。

```csharp
//设置自定义工作表尺寸（以英寸为单位）
ws.PageSetup.CustomPaperSize(6, 4);
```

在此示例中，我们将工作表尺寸设置为 6 英寸宽和 4 英寸高。

## 第 5 步：访问 B4 单元

之后，我们可以访问工作表中的特定单元格。在本例中，我们将访问单元格 B4。

```csharp
//访问 B4 单元格
Cell b4 = ws.Cells["B4"];
```

## 步骤 6：在单元格 B4 中添加消息

我们现在可以使用以下命令将消息添加到单元格 B4`PutValue(value)`方法。

```csharp
//在单元格 B4 中添加消息
b4.PutValue("PDF page size: 6.00 x 4.00 inches");
```

在此示例中，我们在单元格 B4 中添加了消息“PDF 页面大小：6.00”x 4.00”。

## 步骤 7：将工作表保存为 PDF 格式

最后，我们可以使用以下命令将工作表保存为 PDF 格式：`Save(filePath)` Workbook 对象的方法。

```csharp
//将工作表保存为 PDF 格式
wb.Save(outputDir + "outputCustomPaperSize.pdf");
```

使用之前创建的输出文件夹指定生成的 PDF 文件的所需路径。

### 使用 Aspose.Cells for .NET 实现工作表的自定义纸张尺寸进行渲染的示例源代码 
```csharp
//输出目录
string outputDir = "YOUR_OUTPUT_DIRECTORY";
//创建工作簿对象
Workbook wb = new Workbook();
//访问第一个工作表
Worksheet ws = wb.Worksheets[0];
//以英寸为单位设置自定义纸张尺寸
ws.PageSetup.CustomPaperSize(6, 4);
//访问 B4 单元
Cell b4 = ws.Cells["B4"];
//在单元格 B4 中添加消息
b4.PutValue("Pdf Page Dimensions: 6.00 x 4.00 in");
//将工作簿保存为 pdf 格式
wb.Save(outputDir + "outputCustomPaperSize.pdf");
```

## 结论

在本教程中，您学习了如何使用 Aspose.Cells for .NET 实现工作表的自定义大小。您可以使用这些步骤设置工作表的特定尺寸，然后将文档保存为 PDF 格式。我们希望本指南有助于理解实现自定义电子表格大小的过程。

### 常见问题 (FAQ)

#### 问题1：我可以进一步自定义电子表格布局吗？

是的，Aspose.Cells 提供了许多选项来自定义您的工作表布局。您可以设置自定义尺寸、页面方向、边距、页眉和页脚等等。

#### 问题2：Aspose.Cells还支持哪些其他输出格式？

Aspose.Cells 支持许多不同的输出格式，包括 PDF、XLSX、XLS、CSV、HTML、TXT 等。您可以根据需要选择所需的输出格式。