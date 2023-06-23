---
title: 确定工作表的纸张尺寸是否自动
linktitle: 确定工作表的纸张尺寸是否自动
second_title: Aspose.Cells for .NET API 参考
description: 了解如何使用 Aspose.Cells for .NET 确定电子表格的纸张尺寸是否自动。
type: docs
weight: 20
url: /zh/net/excel-page-setup/determine-if-paper-size-of-worksheet-is-automatic/
---
在本文中，我们将带您逐步解释以下 C# 源代码： 使用 Aspose.Cells for .NET 确定工作表的纸张尺寸是否自动。我们将使用 .NET 的 Aspose.Cells 库来执行此操作。按照以下步骤确定工作表的纸张尺寸是否为自动。

## 第 1 步：加载工作簿
第一步是加载工作簿。我们将有两本工作簿：一本禁用自动纸张尺寸，另一本启用自动纸张尺寸。这是加载工作簿的代码：

```csharp
//源目录
string sourceDir = "YOUR_SOURCE_DIR";
//输出目录
string outputDir = "YOUR_OUTPUT_DIRECTORY";

//加载第一个工作簿并禁用自动纸张尺寸
Workbook wb1 = new Workbook(sourceDir + "samplePageSetupIsAutomaticPaperSize-False.xlsx");

//加载启用了自动纸张尺寸的第二个工作簿
Workbook wb2 = new Workbook(sourceDir + "samplePageSetupIsAutomaticPaperSize-True.xlsx");
```

## 第 2 步：访问电子表格
现在我们已经加载了工作簿，我们需要访问工作表，以便检查自动纸张尺寸。我们将转到两个工作簿中的第一个工作表。这是访问它的代码：

```csharp
//转到第一个工作簿的第一个工作表
Worksheet ws11 = wb1.Worksheets[0];

//转到第二个工作簿的第一个工作表
Worksheet ws12 = wb2.Worksheets[0];
```

## 步骤 3：检查自动纸张尺寸
在此步骤中，我们将检查工作表纸张尺寸是否是自动的。我们将使用`PageSetup.IsAutomaticPaperSize`属性来获取此信息。然后我们将显示结果。这是代码：

```csharp
//显示第一个工作簿中第一个工作表的 IsAutomaticPaperSize 属性
Console.WriteLine("First worksheet in first workbook - IsAutomaticPaperSize: " + ws11.PageSetup.IsAutomaticPaperSize);

//在第二个工作簿中显示第一个工作表的 IsAutomaticPaperSize 属性
Console.WriteLine("First worksheet of second workbook - IsAutomaticPaperSize: " + ws12.PageSetup.IsAutomaticPaperSize);

```

### 使用 Aspose.Cells for .NET 确定工作表的纸张尺寸是否自动的示例源代码 
```csharp
//源码目录
string sourceDir = "YOUR_SOURCE_DIRECTORY";
//输出目录
string outputDir = "YOUR_OUTPUT_DIRECTORY";
//加载第一个自动纸张尺寸为 false 的工作簿
Workbook wb1 = new Workbook(sourceDir + "samplePageSetupIsAutomaticPaperSize-False.xlsx");
//加载自动纸张尺寸为 true 的第二个工作簿
Workbook wb2 = new Workbook(sourceDir + "samplePageSetupIsAutomaticPaperSize-True.xlsx");
//访问两个工作簿的第一个工作表
Worksheet ws11 = wb1.Worksheets[0];
Worksheet ws12 = wb2.Worksheets[0];
//打印两个工作表的 PageSetup.IsAutomaticPaperSize 属性
Console.WriteLine("First Worksheet of First Workbook - IsAutomaticPaperSize: " + ws11.PageSetup.IsAutomaticPaperSize);
Console.WriteLine("First Worksheet of Second Workbook - IsAutomaticPaperSize: " + ws12.PageSetup.IsAutomaticPaperSize);
Console.WriteLine();
Console.WriteLine("DetermineIfPaperSizeOfWorksheetIsAutomatic executed successfully.\r\n");
```


## 结论
在本文中，我们学习了如何使用 Aspose.Cells for .NET 自动确定工作表的纸张尺寸。我们遵循以下步骤：加载工作簿，

访问电子表格和自动纸张尺寸检查。现在，您可以使用这些知识来确定电子表格的纸张尺寸是否是自动的。

### 常见问题解答

#### 问：如何使用 Aspose.Cells for .NET 加载工作簿？

答：您可以使用 Aspose.Cells 库中的 Workbook 类加载工作簿。使用 Workbook.Load 方法从文件加载工作簿。

#### 问：我可以检查其他电子表格的自动纸张尺寸吗？

答：是的，您可以通过访问相应 Worksheet 对象的 PageSetup.IsAutomaticPaperSize 属性来检查任何工作表的自动纸张尺寸。

#### 问：如何更改电子表格的自动纸张尺寸？

答：要更改工作表的自动纸张大小，您可以使用 PageSetup.IsAutomaticPaperSize 属性并将其设置为所需的值（true 或 false）。

#### 问：Aspose.Cells for .NET 还提供哪些其他功能？

答：Aspose.Cells for .NET 提供了许多用于处理电子表格的功能，例如创建、修改和转换工作簿，以及操作数据、公式和格式。