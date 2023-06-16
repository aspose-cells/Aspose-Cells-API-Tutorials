---
title: 设置 Excel 页眉和页脚
linktitle: 设置 Excel 页眉和页脚
second_title: Aspose.Cells for .NET API 参考
description: 了解如何使用 Aspose.Cells for .NET 在 Excel 中设置页眉和页脚。
type: docs
weight: 100
url: /zh/net/excel-page-setup/set-excel-headers-and-footers/
---

在本教程中，我们将逐步向您展示如何使用 Aspose.Cells for .NET 在 Excel 中设置页眉和页脚。我们将使用 C# 源代码来说明该过程。

## 第 1 步：设置环境

确保你的机器上安装了 Aspose.Cells for .NET。还要在您喜欢的开发环境中创建一个新项目。

## 第二步：导入必要的库

在您的代码文件中，导入使用 Aspose.Cells 所需的库。下面是相应的代码：

```csharp
using Aspose.Cells;
```

## 第三步：设置数据目录

设置要保存修改后的 Excel 文件的数据目录。使用以下代码：

```csharp
string dataDir = "YOUR DATA DIRECTORY";
```

请务必指定完整的目录路径。

## 第 4 步：创建工作簿和工作表

创建一个新的工作簿对象并使用以下代码导航到工作簿中的第一个工作表：

```csharp
Workbook excel = new Workbook();
PageSetup pageSetup = excel.Worksheets[0].PageSetup;
```

这将创建一个带有工作表的空工作簿，并提供对该工作表的 PageSetup 对象的访问。

## 第 5 步：设置标题

使用设置电子表格标题`SetHeader`PageSetup 对象的方法。这是一个示例代码：

```csharp
pageSetup.SetHeader(0, "&A");
pageSetup.SetHeader(1, "&\"Times New Roman,Bold\"&D-&T");
pageSetup.SetHeader(2, "&\"Times New Roman,Bold\"&12&F");
```

这将分别在标题中设置工作表名称、当前日期和时间以及文件名。

## 第 6 步：定义页脚

使用设置电子表格页脚`SetFooter`PageSetup 对象的方法。这是一个示例代码：

```csharp
pageSetup.SetFooter(0, "Hello World! &\"Courier New\"&14 123");
pageSetup.SetFooter(1, "&P");
pageSetup.SetFooter(2, "&N");
```

这将在页脚中分别设置一个文本字符串、当前页码和总页数。

## 第 7 步：保存修改后的工作簿

使用以下代码保存修改后的工作簿：

```csharp
excel.Save(dataDir + "OutputFileName.xls");
```

这会将修改后的工作簿保存到指定的数据目录。

### 使用 Aspose.Cells for .NET 设置 Excel 页眉和页脚的示例源代码 
```csharp
//文档目录的路径。
string dataDir = "YOUR DOCUMENT DIRECTORY";
//实例化工作簿对象
Workbook excel = new Workbook();
//获取工作表PageSetup的引用
PageSetup pageSetup = excel.Worksheets[0].PageSetup;
//在标题的左侧部分设置工作表名称
pageSetup.SetHeader(0, "&A");
//在标题的中央部分设置当前日期和当前时间
//并更改标题的字体
pageSetup.SetHeader(1, "&\"Times New Roman,Bold\"&D-&T");
//在标题的右侧设置当前文件名并更改
//标题的字体
pageSetup.SetHeader(2, "&\"Times New Roman,Bold\"&12&F");
//在页脚的左侧设置一个字符串并更改字体
//此字符串的一部分（“123”）
pageSetup.SetFooter(0, "Hello World! &\"Courier New\"&14 123");
//在页脚的中央部分设置当前页码
pageSetup.SetFooter(1, "&P");
//在页脚右侧设置页数
pageSetup.SetFooter(2, "&N");
//保存工作簿。
excel.Save(dataDir + "SetHeadersAndFooters_out.xls");
```


## 结论

您现在已经学习了如何使用 Aspose.Cells for .NET 在 Excel 中设置页眉和页脚。本教程向您介绍了该过程的每一步，从设置环境到保存修改后的工作簿。随意进一步探索 Aspose.Cells 的功能，以在您的 Excel 文件中执行进一步的操作。

### 常见问题 (FAQ)

#### 1. 如何在我的系统上安装 Aspose.Cells for .NET？
要安装Aspose.Cells for .NET，您需要从Aspose官网下载安装包并按照文档中提供的说明进行操作。

#### 2. 此方法适用于所有版本的 Excel 吗？
是的，使用 Aspose.Cells for .NET 设置页眉和页脚的方法适用于所有支持的 Excel 版本。

#### 3. 我可以进一步自定义页眉和页脚吗？
是的，Aspose.Cells 提供了广泛的功能来自定义页眉和页脚，包括文本位置、颜色、字体、页码等等。

#### 4. 如何在页眉和页脚中添加动态信息？
您可以使用特殊变量和格式代码将当前日期、时间、文件名、页码等动态信息添加到页眉和页脚。

#### 5、页眉页脚设置好后可以去掉吗？
是的，您可以使用删除页眉和页脚`ClearHeaderFooter`的方法`PageSetup`目的。这将恢复默认的页眉和页脚。