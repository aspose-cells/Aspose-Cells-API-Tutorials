---
title: 冻结工作表的窗格
linktitle: 冻结工作表的窗格
second_title: Aspose.Cells for .NET API 参考
description: 使用 Aspose.Cells for .NET 轻松操作 Excel 工作表的冻结窗格。
type: docs
weight: 70
url: /zh/net/excel-display-settings-csharp-tutorials/freeze-panes-of-worksheet/
---
在本教程中，我们将向您展示如何使用 C# 源代码和 Aspose.Cells for .NET 锁定 Excel 工作表中的窗格。请按照以下步骤操作以获得所需的结果。

## 第1步：导入必要的库

确保您已安装适用于 .NET 的 Aspose.Cells 库并将必要的库导入到您的 C# 项目中。

```csharp
using Aspose.Cells;
```

## 步骤2：设置目录路径并打开Excel文件

设置包含 Excel 文件的目录的路径，然后通过实例化打开该文件`Workbook`目的。

```csharp
string dataDir = "YOUR DOCUMENTS DIRECTORY";
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
Workbook workbook = new Workbook(fstream);
```

## 步骤 3：转到电子表格并应用窗格锁定设置

使用以下命令导航到 Excel 文件中的第一个工作表`Worksheet`目的。然后使用`FreezePanes`应用窗格锁定设置的方法。

```csharp
Worksheet worksheet = workbook.Worksheets[0];
worksheet. FreezePanes(3, 2, 3, 2);
```

在上面的示例中，窗格被锁定到第 3 行第 2 列中的单元格。

## 第 4 步：保存更改

进行必要的更改后，使用以下命令保存修改后的 Excel 文件：`Save`的方法`Workbook`目的。

```csharp
workbook.Save(dataDir + "output.xls");
```

### 使用 Aspose.Cells for .NET 冻结工作表窗格的示例源代码 

```csharp
//文档目录的路径。
string dataDir = "YOUR DOCUMENT DIRECTORY";
//创建包含要打开的 Excel 文件的文件流
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
//实例化 Workbook 对象
//通过文件流打开Excel文件
Workbook workbook = new Workbook(fstream);
//访问 Excel 文件中的第一个工作表
Worksheet worksheet = workbook.Worksheets[0];
//应用冻结窗格设置
worksheet.FreezePanes(3, 2, 3, 2);
//保存修改后的Excel文件
workbook.Save(dataDir + "output.xls");
//关闭文件流以释放所有资源
fstream.Close();
```

## 结论

本分步指南向您展示了如何使用 Aspose.Cells for .NET 锁定 Excel 电子表格中的窗格。使用提供的 C# 源代码，您可以轻松自定义窗格锁定设置，以更好地组织和可视化 Excel 文件中的数据。

### 常见问题 (FAQ)

#### 什么是 Aspose.Cells for .NET？

Aspose.Cells for .NET 是一个功能强大的库，用于在 .NET 应用程序中操作 Excel 文件。

#### 如何安装 Aspose.Cells for .NET？

要安装Aspose.Cells for .NET，您需要从以下位置下载相关包[Aspose 发布](https://releases/aspose.com/cells/net/)并将其添加到您的 .NET 项目中。

#### 如何使用 Aspose.Cells for .NET 锁定 Excel 工作表中的窗格？

您可以使用`FreezePanes`的方法`Worksheet`对象锁定工作表的窗格。通过提供行索引和列索引来指定要锁定的单元格。

#### 我可以使用 Aspose.Cells for .NET 自定义窗格锁定设置吗？

是的，使用`FreezePanes`方法中，您可以根据需要指定要锁定的单元格，并提供适当的行索引和列索引。
