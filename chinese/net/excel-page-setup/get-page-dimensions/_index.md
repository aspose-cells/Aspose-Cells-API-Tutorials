---
title: 获取页面尺寸
linktitle: 获取页面尺寸
second_title: Aspose.Cells for .NET API 参考
description: 了解如何使用 Aspose.Cells for .NET 在 Excel 中检索页面尺寸。使用 C# 编写源代码的分步指南。
type: docs
weight: 40
url: /zh/net/excel-page-setup/get-page-dimensions/
---
Aspose.Cells for .NET 是一个功能强大的库，允许开发人员以编程方式处理 Microsoft Excel 文件。它为处理 Excel 文档提供了广泛的功能，包括获取页面尺寸的能力。在本教程中，我们将引导您完成使用 Aspose.Cells for .NET 检索页面尺寸的步骤。

## 第 1 步：创建 Workbook 类的实例

首先，我们需要创建 Workbook 类的一个实例，它表示 Excel 工作簿。这可以使用以下代码实现：

```csharp
Workbook book = new Workbook();
```

## 第 2 步：访问电子表格

接下来，我们需要导航到工作簿中要设置页面尺寸的工作表。在此示例中，假设我们要使用第一个工作表。我们可以使用以下代码访问它：

```csharp
Worksheet sheet = book.Worksheets[0];
```

## 第 3 步：将纸张大小设置为 A2，并以英寸为单位打印宽度和高度

现在我们将纸张大小设置为 A2，并以英寸为单位打印页面宽度和高度。这可以使用以下代码实现：

```csharp
sheet.PageSetup.PaperSize = PaperSizeType.PaperA2;
Console.WriteLine("A2: " + sheet.PageSetup.PaperWidth + "x" + sheet.PageSetup.PaperHeight);
```

## 第 4 步：将纸张尺寸设置为 A3，并以英寸为单位打印宽度和高度

接下来，我们将纸张大小设置为 A3，并以英寸为单位打印页面宽度和高度。下面是相应的代码：

```csharp
sheet.PageSetup.PaperSize = PaperSizeType.PaperA3;
Console.WriteLine("A3: " + sheet.PageSetup.PaperWidth + "x" + sheet.PageSetup.PaperHeight);
```

## 第 5 步：将纸张尺寸设置为 A4，并以英寸为单位打印宽度和高度

我们现在将纸张大小设置为 A4，并以英寸为单位打印页面宽度和高度。这是代码：

```csharp
sheet.PageSetup.PaperSize = PaperSizeType.PaperA4;
Console.WriteLine("A4: " + sheet.PageSetup.PaperWidth + "x" + sheet.PageSetup.PaperHeight);
```

## 第 6 步：将纸张大小设置为 Letter 并以英寸为单位打印宽度和高度

最后，我们将纸张大小设置为 Letter 并以英寸为单位打印页面宽度和高度。这是代码：

```csharp
sheet.PageSetup.PaperSize = PaperSizeType.PaperLetter;
Console.WriteLine("Letter: " + sheet.PageSetup.PaperWidth + "x" + sheet.PageSetup.PaperHeight);
```

### 使用 Aspose.Cells for .NET 获取页面尺寸的示例源代码 
```csharp
//创建工作簿类的实例
Workbook book = new Workbook();
//访问第一个工作表
Worksheet sheet = book.Worksheets[0];
//将纸张大小设置为 A2 并以英寸为单位打印纸张宽度和高度
sheet.PageSetup.PaperSize = PaperSizeType.PaperA2;
Console.WriteLine("PaperA2: " + sheet.PageSetup.PaperWidth + "x" + sheet.PageSetup.PaperHeight);
//将纸张尺寸设置为 A3 并以英寸为单位打印纸张宽度和高度
sheet.PageSetup.PaperSize = PaperSizeType.PaperA3;
Console.WriteLine("PaperA3: " + sheet.PageSetup.PaperWidth + "x" + sheet.PageSetup.PaperHeight);
//将纸张大小设置为 A4 并以英寸为单位打印纸张宽度和高度
sheet.PageSetup.PaperSize = PaperSizeType.PaperA4;
Console.WriteLine("PaperA4: " + sheet.PageSetup.PaperWidth + "x" + sheet.PageSetup.PaperHeight);
//将纸张大小设置为 Letter 并以英寸为单位打印纸张宽度和高度
sheet.PageSetup.PaperSize = PaperSizeType.PaperLetter;
Console.WriteLine("PaperLetter: " + sheet.PageSetup.PaperWidth + "x" + sheet.PageSetup.PaperHeight);
Console.WriteLine("GetPageDimensions executed successfully.\r\n");
```

## 结论

恭喜！您学习了如何使用 Aspose.Cells for .NET 检索页面尺寸。当您需要根据 Excel 文件中的页面尺寸执行特定操作时，此功能会很有用。

不要忘记进一步浏览 Aspose.Cells 的文档以发现它提供的所有强大功能。

### 常见问题解答

#### 1. Aspose.Cells for .NET 支持哪些其他纸张尺寸？

Aspose.Cells for .NET 支持多种纸张尺寸，包括 A1、A5、B4、B5、Executive、Legal、Letter 等等。您可以查看文档以获取支持的纸张尺寸的完整列表。

#### 2. 我可以使用 Aspose.Cells for .NET 设置自定义页面尺寸吗？

是的，您可以通过指定所需的宽度和高度来设置自定义页面尺寸。 Aspose.Cells 提供了充分的灵活性来根据您的需要自定义页面尺寸。

#### 3. 我能否获得以英寸以外的单位为单位的页面尺寸？

是的，Aspose.Cells for .NET 允许您获取不同单位的页面尺寸，包括英寸、厘米、毫米和磅。

#### 4. Aspose.Cells for .NET 是否支持其他页面设置编辑功能？

是的，Aspose.Cells 为编辑页面设置提供了全方位的功能，包括设置页边距、方向、页眉和页脚等。