---
title: 加载工作簿时过滤定义的名称
linktitle: 加载工作簿时过滤定义的名称
second_title: Aspose.Cells for .NET API 参考
description: 了解如何在使用 Aspose.Cells for .NET 加载 Excel 工作簿时过滤定义的名称。
type: docs
weight: 100
url: /zh/net/excel-workbook/filter-defined-names-while-loading-workbook/
---
在 .NET 应用程序中使用 Excel 工作簿时，通常需要在加载时过滤数据。 Aspose.Cells for .NET 是一个功能强大的库，可以轻松操作 Excel 工作簿。在本指南中，我们将向您展示如何过滤使用 Aspose.Cells for .NET 加载工作簿时定义的名称。按照以下简单步骤即可获得所需结果：

## 第 1 步：指定加载选项

首先，您需要指定加载选项来定义工作簿的加载行为。在我们的例子中，我们想要忽略加载时设置的名称。以下是使用 Aspose.Cells 执行此操作的方法：

```csharp
//指定加载选项
LoadOptions opts = new LoadOptions();

//不加载定义的名称
opts. LoadFilter = new LoadFilter(~LoadDataFilterOptions.DefinedNames);
```

## 第 2 步：加载工作簿

配置加载选项后，您可以从源文件加载 Excel 工作簿。请务必指定正确的文件路径。这是示例代码：

```csharp
//加载工作簿
Workbook wb = new Workbook(sourceDir + "sampleFilterDefinedNamesWhileLoadingWorkbook.xlsx", opts);
```

## 步骤 3：保存筛选后的工作簿

加载工作簿后，您可以根据需要执行其他操作或编辑。然后，您可以将筛选后的工作簿保存到输出文件中。就是这样：

```csharp
//保存筛选后的 Excel 工作簿
wb.Save(outputDir + "outputFilterDefinedNamesWhileLoadingWorkbook.xlsx");
```

### 使用 Aspose.Cells for .NET 加载工作簿时筛选定义名称的示例源代码 
```csharp
//指定加载选项
LoadOptions opts = new LoadOptions();
//我们不想加载定义的名称
opts.LoadFilter = new LoadFilter(~LoadDataFilterOptions.DefinedNames);
//加载工作簿
Workbook wb = new Workbook(sourceDir + "sampleFilterDefinedNamesWhileLoadingWorkbook.xlsx", opts);
//保存输出Excel文件，它会破坏C1中的公式
wb.Save(outputDir + "outputFilterDefinedNamesWhileLoadingWorkbook.xlsx");
Console.WriteLine("FilterDefinedNamesWhileLoadingWorkbook executed successfully.");
```

## 结论

加载 Excel 工作簿时过滤定义的名称对于许多应用程序来说至关重要。 Aspose.Cells for .NET 通过提供加载和过滤数据的灵活选项使这项任务变得更容易。通过遵循本指南中的步骤，您将能够有效地过滤掉定义的名称并在 Excel 工作簿中获得所需的结果。


### 常见问题解答

#### 问：Aspose.Cells 是否支持除 C# 之外的其他编程语言？
    
答：是的，Aspose.Cells是一个跨平台库，支持Java、Python、C等多种编程语言++， 还有很多。

#### 问：使用 Aspose.Cells 加载工作簿时可以过滤其他数据类型吗？
    
答：是的，Aspose.Cells 提供了一系列数据过滤选项，包括公式、样式、宏等。

#### 问：Aspose.Cells 是否保留原始工作簿的格式和属性？
    
答：是的，在处理 Excel 文件时，Aspose.Cells 会保留原始工作簿的格式、样式、公式和其他属性。