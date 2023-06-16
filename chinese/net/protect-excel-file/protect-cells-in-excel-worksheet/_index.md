---
title: 保护 Excel 工作表中的单元格
linktitle: 保护 Excel 工作表中的单元格
second_title: Aspose.Cells for .NET API 参考
description: 了解如何使用 Aspose.Cells for .NET 保护 Excel 中的特定单元格。 C# 中的分步教程。
type: docs
weight: 30
url: /zh/net/protect-excel-file/protect-cells-in-excel-worksheet/
---
Microsoft Excel 是一种广泛用于创建和管理电子表格的工具。 Excel 的核心功能之一是能够保护某些单元格以保持数据完整性。在本教程中，我们将逐步指导您使用 Aspose.Cells for .NET 保护 Excel 电子表格中的特定单元格。 Aspose.Cells for .NET 是一个功能强大的编程库，可以轻松操作 Excel 文件，具有极大的灵活性和高级功能。按照提供的步骤学习如何保护您的重要细胞并确保您的数据安全。

## 第 1 步：设置环境

确保您的开发环境中安装了 Aspose.Cells for .NET。从 Aspose 官方网站下载库并查看文档以获取安装说明。

## 第二步：初始化工作簿和工作表

首先，我们需要创建一个新工作簿并获取对我们要保护单元格的工作表的引用。使用以下代码：

```csharp
//文档目录的路径。
string dataDir = "YOUR DOCUMENTS DIRECTORY";
//如果目录尚不存在，请创建该目录。
bool exists = System.IO.Directory.Exists(dataDir);
if (! exists)
     System.IO.Directory.CreateDirectory(dataDir);

//创建新工作簿
Workbook workbook = new Workbook();

//获取第一个工作表
Worksheet sheet = workbook.Worksheets[0];
```

在此代码片段中，我们首先定义保存 Excel 文件的目录路径。接下来，我们创建一个新的实例`Workbook`类并使用获取对第一个工作表的引用`Worksheets`财产。

## 第 3 步：定义单元格样式

现在我们需要定义要保护的单元格的样式。使用以下代码：

```csharp
//定义样式对象
Styling styling;

//遍历工作表中的所有列并解锁它们
for (int i = 0; i <= 255; i++)
{
     style = sheet.Cells.Columns[(byte)i].Style;
     style. IsLocked = false;
     leaf.Cells.Columns[(byte)i].ApplyStyle(style, new StyleFlag { Locked = true });
}
```

在这段代码中，我们使用循环遍历工作表中的所有列，并通过设置样式来解锁它们的单元格`IsLocked`财产给`false`.然后我们使用`ApplyStyle`将样式应用到列的方法`StyleFlag`标记以锁定单元格。

## 第 4 步：保护特定细胞

现在我们要保护我们想要锁定的特定单元格。使用以下代码：

```csharp
//锁定三个单元格：A1、B1、C1
style = sheet.Cells["A1"].GetStyle();
style. IsLocked = true;
sheet.Cells["A1"].SetStyle(style);

style = sheet.Cells["B1"].GetStyle();
style. IsLocked = true;
sheet.Cells["B1"].SetStyle(style);

style = sheet.Cells["C1"].GetStyle();
style. IsLocked = true;
sheet.Cells["C1"].SetStyle(style);
```

在这段代码中，我们使用`GetStyle`方法，然后我们设置`IsLocked`样式的属性`true`锁定单元格。最后，我们使用更新后的样式应用到每个单元格`SetStyle`方法。

## 步骤 5：保护工作表

现在我们已经定义了要保护的单元格，我们可以保护工作表本身。使用以下代码：

```csharp
//保护工作表
leaf.Protect(ProtectionType.All);
```

此代码使用`Protect`使用指定保护类型保护工作表的方法，在这种情况下`ProtectionType.All`保护工作表中的所有项目。

## 第 6 步：保存 Excel 文件

最后，我们保存所做更改的 Excel 文件。使用以下代码：

```csharp
//保存 Excel 文件
workbook.Save(dataDir + "output.xls", SaveFormat.Excel97To2003);
```

在这段代码中，我们使用`Save`将工作簿保存到指定目录的方法`Excel97To2003`格式。

### 使用 Aspose.Cells for .NET 保护 Excel 工作表中的单元格的示例源代码 
```csharp
//文档目录的路径。
string dataDir = "YOUR DOCUMENT DIRECTORY";
//如果目录不存在，则创建目录。
bool IsExists = System.IO.Directory.Exists(dataDir);
if (!IsExists)
    System.IO.Directory.CreateDirectory(dataDir);
//创建一个新的工作簿。
Workbook wb = new Workbook();
//创建工作表对象并获取第一张工作表。
Worksheet sheet = wb.Worksheets[0];
//定义样式对象。
Style style;
//定义样式标志对象
StyleFlag styleflag;
//遍历工作表中的所有列并解锁它们。
for (int i = 0; i <= 255; i++)
{
    style = sheet.Cells.Columns[(byte)i].Style;
    style.IsLocked = false;
    styleflag = new StyleFlag();
    styleflag.Locked = true;
    sheet.Cells.Columns[(byte)i].ApplyStyle(style, styleflag);
}
//锁定三个单元格...即 A1、B1、C1。
style = sheet.Cells["A1"].GetStyle();
style.IsLocked = true;
sheet.Cells["A1"].SetStyle(style);
style = sheet.Cells["B1"].GetStyle();
style.IsLocked = true;
sheet.Cells["B1"].SetStyle(style);
style = sheet.Cells["C1"].GetStyle();
style.IsLocked = true;
sheet.Cells["C1"].SetStyle(style);
//最后，现在保护工作表。
sheet.Protect(ProtectionType.All);
//保存 excel 文件。
wb.Save(dataDir + "output.xls", SaveFormat.Excel97To2003);
```

## 结论

恭喜！您已经学习了如何使用 Aspose.Cells for .NET 保护 Excel 电子表格中的特定单元格。您现在可以在自己的项目中应用此技术并提高 Excel 文件的安全性。


### 常见问题

#### 问：为什么我应该使用 Aspose.Cells for .NET 来保护 Excel 电子表格中的单元格？
答：Aspose.Cells for .NET 是一个功能强大的库，可以轻松处理 Excel 文件。它提供高级功能来保护电池、解锁范围等。

#### 问：是否可以保护单元格范围而不是单个单元格？
答：是的，您可以定义特定的单元格范围以使用`ApplyStyle`用适当的方法`StyleFlag`.

#### 问：保存后如何打开被保护的Excel文件？
答：打开受保护的Excel文件时，需要提供保护工作表时指定的密码。

#### 问：我可以对 Excel 电子表格应用其他类型的保护吗？
A：是的，Aspose.Cells for .NET支持多种类型的保护，如结构保护、窗口保护等，您可以根据需要选择合适的保护类型。