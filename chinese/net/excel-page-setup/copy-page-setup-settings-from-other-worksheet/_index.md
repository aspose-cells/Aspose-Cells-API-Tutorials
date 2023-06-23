---
title: 从其他工作表复制页面设置设置
linktitle: 从其他工作表复制页面设置设置
second_title: Aspose.Cells for .NET API 参考
description: 了解如何使用 Aspose.Cells for .NET 将页面配置设置从一个电子表格复制到另一个电子表格。优化该库的使用的分步指南。
type: docs
weight: 10
url: /zh/net/excel-page-setup/copy-page-setup-settings-from-other-worksheet/
---
在本文中，我们将带您逐步解释以下 C# 源代码：使用 Aspose.Cells for .NET 从另一个电子表格复制页面配置设置。我们将使用 .NET 的 Aspose.Cells 库来执行此操作。如果要将页面设置设置从一个工作表复制到另一个工作表，请按照以下步骤操作。

## 第 1 步：创建工作簿
第一步是创建工作簿。在我们的例子中，我们将使用 Aspose.Cells 库提供的 Workbook 类。以下是创建工作簿的代码：

```csharp
Workbook wb = new Workbook();
```

## 第 2 步：添加测试工作表
创建工作簿后，我们需要添加测试工作表。在此示例中，我们将添加两个工作表。以下是添加两个工作表的代码：

```csharp
wb.Worksheets.Add("TestSheet1");
wb.Worksheets.Add("TestSheet2");
```

## 第 3 步：访问工作表
现在我们已经添加了工作表，我们需要访问它们才能更改其设置。我们将使用“TestSheet1”和“TestSheet2”工作表的名称来访问它们。这是访问它的代码：

```csharp
Worksheet TestSheet1 = wb. Worksheets["TestSheet1"];
Worksheet TestSheet2 = wb. Worksheets["TestSheet2"];
```

## 步骤 4：设置纸张尺寸
在此步骤中，我们将设置“TestSheet1”工作表的纸张大小。我们将使用`PageSetup.PaperSize`属性来设置纸张尺寸。例如，我们将纸张尺寸设置为“PaperA3ExtraTransverse”。这是代码：

```csharp
TestSheet1.PageSetup.PaperSize = PaperSizeType.PaperA3ExtraTransverse;
```

## 步骤 5：复制页面设置
现在我们将页面配置设置从“TestSheet1”工作表复制到“TestSheet2”。我们将使用`PageSetup.Copy`方法来执行此操作。这是代码：

```csharp
TestSheet2.PageSetup.Copy(TestSheet1.PageSetup, new CopyOptions());
```

## 步骤 6：打印纸张尺寸
复制页面设置设置后，我们将打印两个工作表的纸张尺寸。我们将使用`Console.WriteLine`显示纸张尺寸。这是代码：

```csharp
Console.WriteLine("Before Paper Size: " + TestSheet1.PageSetup.PaperSize);
Console.WriteLine("Before Paper Size: " + TestSheet2.PageSetup.PaperSize);
```

### 使用 Aspose.Cells for .NET 从其他工作表复制页面设置设置的示例源代码 
```csharp
//创建工作簿
Workbook wb = new Workbook();
//添加两个测试工作表
wb.Worksheets.Add("TestSheet1");
wb.Worksheets.Add("TestSheet2");
//访问两个工作表作为 TestSheet1 和 TestSheet2
Worksheet TestSheet1 = wb.Worksheets["TestSheet1"];
Worksheet TestSheet2 = wb.Worksheets["TestSheet2"];
//将 TestSheet1 的纸张尺寸设置为 PaperA3ExtraTransverse
TestSheet1.PageSetup.PaperSize = PaperSizeType.PaperA3ExtraTransverse;
//打印两个工作表的纸张尺寸
Console.WriteLine("Before Paper Size: " + TestSheet1.PageSetup.PaperSize);
Console.WriteLine("Before Paper Size: " + TestSheet2.PageSetup.PaperSize);
Console.WriteLine();
//将 PageSetup 从 TestSheet1 复制到 TestSheet2
TestSheet2.PageSetup.Copy(TestSheet1.PageSetup, new CopyOptions());
//打印两个工作表的纸张尺寸
Console.WriteLine("After Paper Size: " + TestSheet1.PageSetup.PaperSize);
Console.WriteLine("After Paper Size: " + TestSheet2.PageSetup.PaperSize);
Console.WriteLine();
Console.WriteLine("CopyPageSetupSettingsFromSourceWorksheetToDestinationWorksheet executed successfully.\r\n");
```

## 结论
在本文中，我们学习了如何使用 Aspose.Cells for .NET 将页面配置设置从一个工作表复制到另一个工作表。我们完成了以下步骤：创建工作簿、添加测试工作表、访问工作表、设置纸张尺寸、复制页面设置设置和打印纸张尺寸。现在您可以使用这些知识将页面配置设置复制到您自己的项目中。

### 常见问题解答

#### 问：我可以在不同的工作簿实例之间复制页面配置设置吗？

答：是的，您可以使用以下命令在不同工作簿实例之间复制页面设置设置`PageSetup.Copy`Aspose.Cells 库的方法。

#### 问：我可以复制其他页面设置，例如方向或边距吗？

答：是的，您可以使用复制其他页面设置设置`PageSetup.Copy`方法与适当的选项。例如，您可以使用复制方向`CopyOptions.Orientation`和边距使用`CopyOptions.Margins`.

#### 问：我如何知道纸张尺寸有哪些可用选项？

答：您可以查看 Aspose.Cells 库 API 参考以获取可用的纸张尺寸选项。有一个枚举叫做`PaperSizeType`其中列出了支持的不同纸张尺寸。

#### 问：如何下载 .NET 的 Aspose.Cells 库？

答：您可以从以下位置下载 .NET 的 Aspose.Cells 库：[Aspose 发布](https://releases.aspose.com/cells/net)。有免费试用版以及商业用途的付费许可证。

#### 问：Aspose.Cells 库支持其他编程语言吗？

答：是的，Aspose.Cells 库支持多种编程语言，包括 C#、Java、Python 等。