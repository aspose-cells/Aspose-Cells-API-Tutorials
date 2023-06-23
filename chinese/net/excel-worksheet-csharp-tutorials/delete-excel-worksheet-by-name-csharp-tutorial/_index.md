---
title: 按名称删除 Excel 工作表 C# 教程
linktitle: 按名称删除 Excel 工作表
second_title: Aspose.Cells for .NET API 参考
description: 使用 Aspose.Cells for .NET 按名称轻松删除特定的 Excel 工作表。带有代码示例的详细教程。
type: docs
weight: 40
url: /zh/net/excel-worksheet-csharp-tutorials/delete-excel-worksheet-by-name-csharp-tutorial/
---
在本教程中，我们将逐步指导您讲解下面的 C# 源代码，该源代码可以使用 Aspose.Cells for .NET 使用其名称来删除 Excel 工作表。我们将为每个步骤提供示例代码，以帮助您详细了解该过程。

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

## 步骤 4：按名称删除工作表

要从名称中删除工作表，您可以使用`RemoveAt()`的方法`Worksheets`的对象`Workbook`目的。您要删除的工作表的名称必须作为参数传递。

```csharp
//使用工作表名称删除工作表
workbook.Worksheets.RemoveAt("Sheet1");
```

## 第 5 步：保存工作簿

删除工作表后，您可以使用以下命令保存修改后的 Excel 工作簿`Save()`的方法`Workbook`目的。

```csharp
//保存 Excel 工作簿
workbook.Save(dataDir + "output.out.xls");
```


### 使用 Aspose.Cells for .NET 按名称删除 Excel 工作表的示例源代码 C# 教程 
```csharp
//文档目录的路径。
string dataDir = "YOUR DOCUMENT DIRECTORY";
//创建包含要打开的 Excel 文件的文件流
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
//实例化 Workbook 对象
//通过文件流打开Excel文件
Workbook workbook = new Workbook(fstream);
//使用工作表名称删除工作表
workbook.Worksheets.RemoveAt("Sheet1");
//保存工作簿
workbook.Save(dataDir + "output.out.xls");
```

## 结论

在本教程中，我们介绍了使用 Aspose.Cells for .NET 按名称删除 Excel 电子表格的分步过程。通过遵循提供的代码示例和说明，您现在应该很好地了解如何在 C# 应用程序中执行此任务。 Aspose.Cells for .NET 提供了一整套用于处理 Excel 文件的功能，使您可以轻松操作电子表格和相关数据。

### 常见问题 (FAQ)

#### 什么是 Aspose.Cells for .NET？

Aspose.Cells for .NET 是一个功能强大的库，允许开发人员在其 .NET 应用程序中创建、操作和转换 Excel 文件。它提供了广泛的功能来处理电子表格、单元格、公式、样式等。

#### 如何安装 Aspose.Cells for .NET？

要安装 Aspose.Cells for .NET，您可以从 Aspose Releases (https://releases.aspose.com/cells/net）并按照提供的说明进行操作。您需要有效的许可证才能在应用程序中使用该库。

#### 我可以一次删除多个工作表吗？

是的，您可以使用 Aspose.Cells for .NET 删除多个工作表。您只需对要删除的每个工作表重复删除步骤即可。

#### 在删除电子表格之前如何知道它是否存在？

在删除工作表之前，您可以使用以下命令检查它是否存在`Contains()`的方法`Worksheets`的对象`Workbook`目的。该方法将电子表格名称作为参数并返回`true`如果电子表格存在，否则返回`false`.

#### 是否可以恢复已删除的电子表格？

不幸的是，电子表格一旦被删除，就无法直接从 Excel 文件中恢复。建议在删除电子表格之前创建 Excel 文件的备份，以避免数据丢失。