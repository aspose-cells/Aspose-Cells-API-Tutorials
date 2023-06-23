---
title: 获取页面尺寸
linktitle: 获取页面尺寸
second_title: Aspose.Cells for .NET API 参考
description: 了解如何使用 Aspose.Cells for .NET 在 Excel 中检索页面尺寸。带有 C# 源代码的分步指南。
type: docs
weight: 40
url: /zh/net/excel-page-setup/get-page-dimensions/
---
Aspose.Cells for .NET 是一个功能强大的库，允许开发人员以编程方式处理 Microsoft Excel 文件。它提供了广泛的用于操作 Excel 文档的功能，包括获取页面尺寸的功能。在本教程中，我们将引导您完成使用 Aspose.Cells for .NET 检索页面尺寸的步骤。

## 步骤 1：创建 Workbook 类的实例

首先，我们需要创建 Workbook 类的一个实例，它代表 Excel 工作簿。这可以使用以下代码来实现：

```csharp
Workbook book = new Workbook();
```

## 第 2 步：访问电子表格

接下来，我们需要导航到工作簿中要设置页面尺寸的工作表。在此示例中，假设我们要使用第一个工作表。我们可以使用以下代码访问它：

```csharp
Worksheet sheet = book.Worksheets[0];
```

## 步骤 3：将纸张尺寸设置为 A2，并以英寸为单位打印宽度和高度

现在我们将纸张尺寸设置为A2，并以英寸为单位打印页面宽度和高度。这可以使用以下代码来实现：

```csharp
sheet.PageSetup.PaperSize = PaperSizeType.PaperA2;
Console.WriteLine("A2: " + sheet.PageSetup.PaperWidth + "x" + sheet.PageSetup.PaperHeight);
```

## 步骤 4：将纸张尺寸设置为 A3，并以英寸为单位打印宽度和高度

接下来，我们将纸张尺寸设置为 A3 并以英寸为单位打印页面宽度和高度。这是相应的代码：

```csharp
sheet.PageSetup.PaperSize = PaperSizeType.PaperA3;
Console.WriteLine("A3: " + sheet.PageSetup.PaperWidth + "x" + sheet.PageSetup.PaperHeight);
```

## 步骤 5：将纸张尺寸设置为 A4，并以英寸为单位打印宽度和高度

现在，我们将纸张尺寸设置为 A4，并以英寸为单位打印页面宽度和高度。这是代码：

```csharp
sheet.PageSetup.PaperSize = PaperSizeType.PaperA4;
Console.WriteLine("A4: " + sheet.PageSetup.PaperWidth + "x" + sheet.PageSetup.PaperHeight);
```

## 步骤 6：将纸张尺寸设置为 Letter 并以英寸为单位打印宽度和高度

最后，我们将纸张尺寸设置为 Letter 并以英寸为单位打印页面宽度和高度。这是代码：

```csharp
sheet.PageSetup.PaperSize = PaperSizeType.PaperLetter;
Console.WriteLine("Letter: " + sheet.PageSetup.PaperWidth + "x" + sheet.PageSetup.PaperHeight);
```

### 使用 Aspose.Cells for .NET 获取页面尺寸的示例源代码 
```csharp
//创建 Workbook 类的实例
Workbook book = new Workbook();
//访问第一个工作表
Worksheet sheet = book.Worksheets[0];
//将纸张尺寸设置为 A2 并以英寸为单位打印纸张宽度和高度
sheet.PageSetup.PaperSize = PaperSizeType.PaperA2;
Console.WriteLine("PaperA2: " + sheet.PageSetup.PaperWidth + "x" + sheet.PageSetup.PaperHeight);
//将纸张尺寸设置为 A3 并以英寸为单位打印纸张宽度和高度
sheet.PageSetup.PaperSize = PaperSizeType.PaperA3;
Console.WriteLine("PaperA3: " + sheet.PageSetup.PaperWidth + "x" + sheet.PageSetup.PaperHeight);
//将纸张尺寸设置为 A4 并以英寸为单位打印纸张宽度和高度
sheet.PageSetup.PaperSize = PaperSizeType.PaperA4;
Console.WriteLine("PaperA4: " + sheet.PageSetup.PaperWidth + "x" + sheet.PageSetup.PaperHeight);
//将纸张尺寸设置为 Letter 并打印纸张宽度和高度（以英寸为单位）
sheet.PageSetup.PaperSize = PaperSizeType.PaperLetter;
Console.WriteLine("PaperLetter: " + sheet.PageSetup.PaperWidth + "x" + sheet.PageSetup.PaperHeight);
Console.WriteLine("GetPageDimensions executed successfully.\r\n");
```

## 结论

恭喜！您学习了如何使用 Aspose.Cells for .NET 检索页面尺寸。当您需要根据 Excel 文件中的页面尺寸执行特定操作时，此功能非常有用。

不要忘记进一步探索 Aspose.Cells 的文档，以发现它提供的所有强大功能。

### 常见问题解答

#### 1. Aspose.Cells for .NET 支持哪些其他纸张尺寸？

Aspose.Cells for .NET 支持多种纸张尺寸，包括 A1、A5、B4、B5、Executive、Legal、Letter 等。您可以查看文档以获取支持的纸张尺寸的完整列表。

#### 2. 我可以使用 Aspose.Cells for .NET 设置自定义页面尺寸吗？

是的，您可以通过指定所需的宽度和高度来设置自定义页面尺寸。 Aspose.Cells 提供了完全的灵活性，可以根据您的需求自定义页面尺寸。

#### 3. 我可以获得英寸以外的页面尺寸吗？

是的，Aspose.Cells for .NET 允许您获取不同单位的页面尺寸，包括英寸、厘米、毫米和磅。

#### 4. Aspose.Cells for .NET支持其他页面设置编辑功能吗？

是的，Aspose.Cells 提供了编辑页面设置的全套功能，包括设置边距、方向、页眉和页脚等。