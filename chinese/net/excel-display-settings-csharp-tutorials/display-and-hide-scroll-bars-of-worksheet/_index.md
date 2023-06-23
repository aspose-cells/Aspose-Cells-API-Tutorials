---
title: 显示和隐藏工作表滚动条
linktitle: 显示和隐藏工作表滚动条
second_title: Aspose.Cells for .NET API 参考
description: 使用 Aspose.Cells for .NET 在 Excel 工作表中显示或隐藏滚动条。
type: docs
weight: 50
url: /zh/net/excel-display-settings-csharp-tutorials/display-and-hide-scroll-bars-of-worksheet/
---
在本教程中，我们将向您展示如何使用 C# 源代码和 Aspose.Cells for .NET 在 Excel 工作表中显示或隐藏垂直和水平滚动条。请按照以下步骤操作以获得所需的结果。

## 第1步：导入必要的库

确保您已安装适用于 .NET 的 Aspose.Cells 库并将必要的库导入到您的 C# 项目中。

```csharp
using Aspose.Cells;
using System.IO;
```

## 步骤2：设置目录路径并打开Excel文件

设置包含 Excel 文件的目录的路径，然后通过创建文件流并实例化一个文件来打开该文件`Workbook`目的。

```csharp
string dataDir = "YOUR DOCUMENTS DIRECTORY";
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
Workbook workbook = new Workbook(fstream);
```

## 第 3 步：隐藏滚动条

使用`IsVScrollBarVisible`和`IsHScrollBarVisible`的属性`Workbook.Settings`对象隐藏工作表的垂直和水平滚动条。

```csharp
workbook.Settings.IsVScrollBarVisible = false;
workbook.Settings.IsHScrollBarVisible = false;
```

## 第 4 步：保存更改

进行必要的更改后，使用以下命令保存修改后的 Excel 文件：`Save`的方法`Workbook`目的。

```csharp
workbook.Save(dataDir + "output.xls");
```

### 使用 Aspose.Cells for .NET 显示和隐藏工作表滚动条的示例源代码 

```csharp
//文档目录的路径。
string dataDir = "YOUR DOCUMENT DIRECTORY";
//创建包含要打开的 Excel 文件的文件流
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
//实例化 Workbook 对象
//通过文件流打开Excel文件
Workbook workbook = new Workbook(fstream);
//隐藏Excel文件的垂直滚动条
workbook.Settings.IsVScrollBarVisible = false;
//隐藏Excel文件的水平滚动条
workbook.Settings.IsHScrollBarVisible = false;
//保存修改后的Excel文件
workbook.Save(dataDir + "output.xls");
//关闭文件流以释放所有资源
fstream.Close();
```

### 结论

本分步指南向您展示了如何使用 Aspose.Cells for .NET 在 Excel 电子表格中显示或隐藏垂直和水平滚动条。使用提供的 C# 源代码，您可以轻松自定义 Excel 文件中滚动条的显示。

### 常见问题 (FAQ)

#### 什么是 Aspose.Cells for .NET？

Aspose.Cells for .NET 是一个功能强大的库，用于在 .NET 应用程序中操作 Excel 文件。

#### 如何安装 Aspose.Cells for .NET？

要安装Aspose.Cells for .NET，您需要从以下位置下载相关包[Aspose 发布](https://releases/aspose.com/cells/net/)并将其添加到您的 .NET 项目中。

#### 如何使用 Aspose.Cells for .NET 在 Excel 电子表格中显示或隐藏滚动条？

您可以使用`IsVScrollBarVisible`和`IsHScrollBarVisible`的属性`Workbook.Settings`对象分别在 Excel 工作表中显示或隐藏垂直和水平滚动条。

#### Aspose.Cells for .NET 支持哪些其他 Excel 文件格式？

Aspose.Cells for .NET支持多种Excel文件格式，例如XLS、XLSX、CSV、HTML、PDF等。