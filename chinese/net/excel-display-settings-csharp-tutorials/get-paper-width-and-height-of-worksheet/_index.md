---
title: 获取工作表的纸张宽度和高度
linktitle: 获取工作表的纸张宽度和高度
second_title: Aspose.Cells for .NET API 参考
description: 创建一个分步指南来解释以下 C# 源代码，以使用 Aspose.Cells for .NET 获取电子表格的纸张宽度和高度。
type: docs
weight: 80
url: /zh/net/excel-display-settings-csharp-tutorials/get-paper-width-and-height-of-worksheet/
---
在本教程中，我们将带您一步步讲解以下C#源代码，使用Aspose.Cells for .NET获取工作表的纸张宽度和高度。请按照以下步骤操作：

## 第 1 步：创建工作簿
首先使用创建一个新的工作簿`Workbook`班级：

```csharp
Workbook wb = new Workbook();
```

## 第 2 步：访问第一个工作表
接下来，使用导航到工作簿中的第一个工作表`Worksheet`班级：

```csharp
Worksheet ws = wb.Worksheets[0];
```

## 第 3 步：将纸张大小设置为 A2 并以英寸为单位显示纸张宽度和高度
使用`PaperSize`的财产`PageSetup`对象将纸张大小设置为 A2，然后使用`PaperWidth`和`PaperHeight`属性分别获取纸张的宽度和高度。使用显示这些值`Console.WriteLine`方法：

```csharp
ws.PageSetup.PaperSize = PaperSizeType.PaperA2;
Console.WriteLine("PaperA2: " + ws.PageSetup.PaperWidth + "x" + ws.PageSetup.PaperHeight);
```

## 第 4 步：对其他纸张尺寸重复步骤
重复前面的步骤，将纸张尺寸更改为 A3、A4 和 Letter，然后显示每种尺寸的纸张宽度和高度值：

```csharp
ws.PageSetup.PaperSize = PaperSizeType.PaperA3;
Console.WriteLine("PaperA3: " + ws.PageSetup.PaperWidth + "x" + ws.PageSetup.PaperHeight);

ws.PageSetup.PaperSize = PaperSizeType.PaperA4;
Console.WriteLine("PaperA4: " + ws.PageSetup.PaperWidth + "x" + ws.PageSetup.PaperHeight);

ws.PageSetup.PaperSize = PaperSizeType.PaperLetter;
Console.WriteLine("PaperLetter: " + ws.PageSetup.PaperWidth + "x" + ws.PageSetup.PaperHeight);
```

### 使用 Aspose.Cells for .NET 获取工作表的纸张宽度和高度的示例源代码 

```csharp
//创建工作簿
Workbook wb = new Workbook();
//访问第一个工作表
Worksheet ws = wb.Worksheets[0];
//将纸张大小设置为 A2 并以英寸为单位打印纸张宽度和高度
ws.PageSetup.PaperSize = PaperSizeType.PaperA2;
Console.WriteLine("PaperA2: " + ws.PageSetup.PaperWidth + "x" + ws.PageSetup.PaperHeight);
//将纸张尺寸设置为 A3 并以英寸为单位打印纸张宽度和高度
ws.PageSetup.PaperSize = PaperSizeType.PaperA3;
Console.WriteLine("PaperA3: " + ws.PageSetup.PaperWidth + "x" + ws.PageSetup.PaperHeight);
//将纸张大小设置为 A4 并以英寸为单位打印纸张宽度和高度
ws.PageSetup.PaperSize = PaperSizeType.PaperA4;
Console.WriteLine("PaperA4: " + ws.PageSetup.PaperWidth + "x" + ws.PageSetup.PaperHeight);
//将纸张大小设置为 Letter 并以英寸为单位打印纸张宽度和高度
ws.PageSetup.PaperSize = PaperSizeType.PaperLetter;
Console.WriteLine("PaperLetter: " + ws.PageSetup.PaperWidth + "x" + ws.PageSetup.PaperHeight);
```


## 结论

您学习了如何使用 Aspose.Cells for .NET 获取电子表格的纸张宽度和高度。此功能对于 Excel 文档的配置和精确布局很有用。

### 常见问题 (FAQ)

#### 什么是 Aspose.Cells for .NET？

Aspose.Cells for .NET 是一个强大的库，用于在 .NET 应用程序中操作和处理 Excel 文件。它提供了许多用于创建、修改、转换和分析 Excel 文件的功能。

#### 如何使用 Aspose.Cells for .NET 获取电子表格的纸张大小？

您可以使用`PageSetup`类的`Worksheet`对象访问纸张大小。使用`PaperSize`属性来设置纸张大小和`PaperWidth`和`PaperHeight`属性分别获取纸张的宽度和高度。

#### Aspose.Cells for .NET 支持哪些纸张尺寸？

Aspose.Cells for .NET 支持广泛的常用纸张尺寸，例如 A2、A3、A4 和 Letter，以及许多其他自定义尺寸。

#### 我可以使用 Aspose.Cells for .NET 自定义电子表格的纸张大小吗？

是的，您可以通过使用指定确切的宽度和高度尺寸来设置自定义纸张尺寸`PaperWidth`和`PaperHeight`的属性`PageSetup`班级。