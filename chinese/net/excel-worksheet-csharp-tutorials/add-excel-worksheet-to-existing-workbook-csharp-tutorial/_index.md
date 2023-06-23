---
title: 将 Excel 工作表添加到现有工作簿 C# 教程
linktitle: 将 Excel 工作表添加到现有工作簿
second_title: Aspose.Cells for .NET API 参考
description: 使用 Aspose.Cells for .NET 轻松将新工作表添加到现有 Excel 工作簿。带有代码示例的分步教程。
type: docs
weight: 10
url: /zh/net/excel-worksheet-csharp-tutorials/add-excel-worksheet-to-existing-workbook-csharp-tutorial/
---
在本教程中，我们将逐步向您解释下面的 C# 源代码，该代码有助于使用 Aspose.Cells for .NET 将新工作表添加到现有 Excel 工作簿。我们将为每个步骤提供示例代码，以帮助您详细了解该过程。

## 第 1 步：定义文档目录

首先，您需要设置 Excel 文件所在的目录路径。将代码中的“YOUR DOCUMENT DIRECTORY”替换为 Excel 文件的实际路径。

```csharp
//文档目录的路径。
string dataDir = "YOUR DOCUMENT DIRECTORY";
```

## 步骤 2：创建文件流并打开 Excel 文件

接下来，您需要创建一个文件流并使用以下命令打开 Excel 文件`FileStream`班级。

```csharp
//创建包含要打开的 Excel 文件的文件流
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
```

## 第 3 步：实例化工作簿对象

打开Excel文件后，需要实例化一个`Workbook`目的。该对象代表 Excel 工作簿并提供各种方法和属性来操作工作簿。

```csharp
//实例化 Workbook 对象
//通过文件流程打开Excel文件
Workbook workbook = new Workbook(fstream);
```

## 步骤 4：向工作簿添加新工作表

要将新工作表添加到工作簿中，您可以使用`Worksheets.Add()`的方法`Workbook`目的。该方法返回新添加的工作表的索引。

```csharp
//将新工作表添加到 Workbook 工作簿
int i = workbook. Worksheets. Add();
```

## 第5步：设置新工作表名称

您可以使用以下命令设置新添加的工作表的名称`Name`的财产`Worksheet`目的。

```csharp
//通过传递sheet索引获取新添加的sheet的引用
Worksheet worksheet = workbook.Worksheets[i];
//定义新工作表的名称
worksheet.Name = "My Worksheet";
```

## 第 6 步：保存 Excel 文件

添加新工作表并设置其名称后，您可以使用以下命令保存修改后的 Excel 文件：`Save()`的方法`Workbook`目的。

```csharp
//保存 Excel 文件
workbook.Save(dataDir + "output.out.xls");
```

## 步骤7：关闭文件流并释放资源

最后，关闭文件流以释放与其关联的所有资源非常重要。

```csharp
//关闭文件流以释放所有资源
fstream.Close();
```

### 使用 Aspose.Cells for .NET 将 Excel 工作表添加到现有工作簿 C# 教程的示例源代码 
```csharp
//文档目录的路径。
string dataDir = "YOUR DOCUMENT DIRECTORY";
//创建包含要打开的 Excel 文件的文件流
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
//实例化 Workbook 对象
//通过文件流打开Excel文件
Workbook workbook = new Workbook(fstream);
//将新工作表添加到 Workbook 对象
int i = workbook.Worksheets.Add();
//通过传递工作表索引来获取新添加的工作表的引用
Worksheet worksheet = workbook.Worksheets[i];
//设置新添加的工作表名称
worksheet.Name = "My Worksheet";
//保存 Excel 文件
workbook.Save(dataDir + "output.out.xls");
//关闭文件流以释放所有资源
fstream.Close();
```

## 结论

在本教程中，我们逐步介绍了使用 Aspose.Cells for .NET 将新的 Fire Connect 添加到现有 Excel 工作簿的过程。通过遵循提供的代码示例和说明，您现在应该很好地了解如何在 C# 应用程序中执行此任务。 Aspose.Cells for .NET 提供了一整套用于处理 Excel 文件的功能，使您能够高效地自动执行各种与 Excel 相关的任务。

### 常见问题 (FAQ)

#### 什么是 Aspose.Cells for .NET？

Aspose.Cells for .NET 是一个功能强大的 .NET 库，允许开发人员在其应用程序中创建、操作和转换 Excel 文件。它提供了广泛的功能来处理电子表格、单元格、公式、样式等。

#### 如何安装 Aspose.Cells for .NET？

要安装 Aspose.Cells for .NET，您可以从 Aspose Releases (https://releases.aspose.com/cells/net）并按照提供的安装说明进行操作。您还需要有效的许可证才能在应用程序中使用该库。

#### 我可以使用 Aspose.Cells for .NET 添加多个电子表格吗？

是的，您可以使用 Aspose.Cells for .NET 将多个工作表添加到一个 Excel 文件中。您可以使用`Worksheets.Add()`的方法`Workbook`对象在工作簿中的不同位置添加新工作表。

#### 如何设置 Excel 文件中单元格的格式？

Aspose.Cells for .NET 提供了不同的方法和属性来格式化 Excel 文件中的单元格。您可以设置单元格值，应用格式选项，例如字体样式、颜色、对齐方式、边框等。有关单元格格式设置的更多详细信息，请参阅 Aspose.Cells 提供的文档和示例代码。

#### Aspose.Cells for .NET 是否与不同版本的 Excel 兼容？

是的，Aspose.Cells for .NET 与不同版本的 Excel 兼容，包括 Excel 2003、Excel 2007、Excel 2010、Excel 2013、Excel 2016、Excel 2019 和 Excel for Office 365。它支持 .xls 格式和较新的 .xls 格式。 xlsx 格式。