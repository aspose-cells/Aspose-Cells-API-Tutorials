---
title: 取消保护简单的 Excel 工作表
linktitle: 取消保护简单的 Excel 工作表
second_title: Aspose.Cells for .NET API 参考
description: 了解如何使用 Aspose.Cells for .NET 取消对 Excel 电子表格的保护。 C# 分步教程。
type: docs
weight: 30
url: /zh/net/unprotect-excel-sheet/unprotect-simple-excel-sheet/
---
在本教程中，我们将指导您完成使用 .NET 的 Aspose.Cells 库解锁简单 Excel 电子表格所需的步骤。

## 第一步：准备环境

开始之前，请确保您的计算机上安装了 Aspose.Cells for .NET。从 Aspose 官方网站下载该库并按照提供的安装说明进行操作。

## 第二步：配置文档目录路径

在提供的源代码中，您需要指定要解锁的Excel文件所在的目录路径。修改`dataDir`变量，将“YOUR DOCUMENT DIRECTORY”替换为计算机上目录的绝对路径。

```csharp
//文档目录的路径。
string dataDir = "PATH TO YOUR DOCUMENTS DIRECTORY";
```

## 第 3 步：创建工作簿对象

首先，我们需要创建一个代表 Excel 文件的 Workbook 对象。使用 Workbook 类构造函数并指定要打开的 Excel 文件的完整路径。

```csharp
//实例化 Workbook 对象
Workbook workbook = new Workbook(dataDir + "book1.xls");
```

## 第 4 步：访问电子表格

接下来，我们需要导航到 Excel 文件中的第一个工作表。使用`Worksheets`Workbook 对象的属性来访问工作表集合，然后使用`[0]`用于访问第一张表的索引。

```csharp
//访问 Excel 文件中的第一个工作表
Worksheet worksheet = workbook.Worksheets[0];
```

## 第 5 步：解锁电子表格

现在我们将使用以下命令解锁工作表`Unprotect()` Worksheet 对象的方法。此方法不需要密码。

```csharp
//在没有密码的情况下取消对工作表的保护
worksheet.Unprotect();
```

## 步骤 6：保存解锁的 Excel 文件

电子表格解锁后，我们可以保存最终的 Excel 文件。使用`Save()`方法指定输出文件的完整路径和保存格式。

```csharp
//保存工作簿
workbook.Save(dataDir + "output.out.xls", SaveFormat.Excel97To2003);
```
### 使用 Aspose.Cells for .NET 取消保护简单 Excel 工作表的示例源代码 
```csharp
//文档目录的路径。
string dataDir = "YOUR DOCUMENT DIRECTORY";
//实例化 Workbook 对象
Workbook workbook = new Workbook(dataDir + "book1.xls");
//访问 Excel 文件中的第一个工作表
Worksheet worksheet = workbook.Worksheets[0];
//在没有密码的情况下取消对工作表的保护
worksheet.Unprotect();
//保存工作簿
workbook.Save(dataDir + "output.out.xls", SaveFormat.Excel97To2003);
```

## 结论

恭喜！您现在已经了解了如何使用 Aspose.Cells for .NET 解锁简单的 Excel 电子表格。通过遵循本教程中的步骤，您可以轻松地将此功能应用到您自己的项目中。

欢迎探索 Aspose.Cells 的更多功能
对 Excel 文件进行更高级的操作。

### 常见问题解答

#### 问：解锁 Excel 电子表格时应采取哪些预防措施？

答：解锁 Excel 电子表格时，请确保您拥有访问该文件所需的权限。另外，请务必使用正确的解锁方法并提供正确的密码（如果适用）。

#### 问：我如何知道电子表格是否受密码保护？

答：您可以使用 .NET 的 Aspose.Cells 库提供的属性或方法来检查工作表是否受密码保护。例如，您可以使用`IsProtected()`Worksheet 对象的方法来检查工作表是否受到保护。

#### 问：我在尝试解锁电子表格时遇到异常。我应该怎么办 ？

答：如果您在解锁电子表格时遇到异常，请确保您已正确指定 Excel 文件的路径，并检查您是否具有访问该文件所需的权限。如果问题仍然存在，请随时联系 Aspose.Cells 支持以获得进一步帮助。