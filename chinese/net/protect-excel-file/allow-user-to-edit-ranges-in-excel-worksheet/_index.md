---
title: 允许用户在 Excel 工作表中编辑范围
linktitle: 允许用户在 Excel 工作表中编辑范围
second_title: Aspose.Cells for .NET API 参考
description: 允许用户使用 Aspose.Cells for .NET 编辑 Excel 电子表格中的特定范围。使用 C# 编写源代码的分步指南。
type: docs
weight: 10
url: /zh/net/protect-excel-file/allow-user-to-edit-ranges-in-excel-worksheet/
---
在本指南中，我们将带您了解如何使用 Aspose.Cells for .NET 允许用户编辑 Excel 电子表格中的特定范围。请按照以下步骤完成此任务。

## 第 1 步：设置环境

确保您已经设置了开发环境并安装了 Aspose.Cells for .NET。你可以从Aspose官网下载最新版本的库。

## 第 2 步：导入所需的命名空间

在您的 C# 项目中，导入必要的命名空间以使用 Aspose.Cells：

```csharp
using Aspose.Cells;
```

## 第三步：设置文档目录的路径

声明一个`dataDir`变量指定要保存生成的 Excel 文件的目录路径：

```csharp
string dataDir = "YOUR_DIRECTORY_OF_DOCUMENTS";
```

务必更换`"YOUR_DOCUMENT_DIRECTORY"`在您的系统上使用正确的路径。

## 第 4 步：创建工作簿对象

实例化一个新的 Workbook 对象，该对象代表您要创建的 Excel 工作簿：

```csharp
Workbook book = new Workbook();
```

## 第 5 步：访问第一个工作表

使用以下代码导航到 Excel 工作簿中的第一个工作表：

```csharp
Worksheet sheet = book.Worksheets[0];
```

## 第 6 步：检索授权修改范围

使用获取允许编辑范围的集合`AllowEditRanges`财产：

```csharp
ProtectedRangeCollection allowRanges = sheet.AllowEditRanges;
```

## 第 7 步：定义保护范围

使用`Add`的方法`AllowEditRanges`收藏：

```csharp
int idx = allowRanges.Add("r2", 1, 1, 3, 3);
protectedRange protectedRange = allowRanges[idx];
```

在这里，我们创建了一个从单元格 A1 到单元格 C3 的受保护范围“r2”。

## 步骤 8：指定密码

使用`Password`财产：

```csharp
protectedRange.Password = "YOUR_PASSWORD";
```

务必更换`"YOUR_PASSWORD"`使用所需的密码。

## 第 9 步：保护工作表

使用保护工作表`Protect`的方法`Worksheet`目的：

```csharp
sheet.Protect(ProtectionType.All);
```

这将通过防止超出允许范围的任何修改来保护电子表格。

## 第 10 步：注册

  Excel文件

保存生成的 Excel 文件，使用`Save`的方法`Workbook`目的：

```csharp
book.Save(dataDir + "protectedrange.out.xls");
```

请务必指定所需的文件名和正确的路径。

### 允许用户使用 Aspose.Cells for .NET 在 Excel 工作表中编辑范围的示例源代码 
```csharp
//文档目录的路径。
string dataDir = "YOUR DOCUMENT DIRECTORY";
//如果目录不存在，则创建目录。
bool IsExists = System.IO.Directory.Exists(dataDir);
if (!IsExists)
    System.IO.Directory.CreateDirectory(dataDir);
//实例化一个新的工作簿
Workbook book = new Workbook();
//获取第一个（默认）工作表
Worksheet sheet = book.Worksheets[0];
//获取允许编辑范围
ProtectedRangeCollection allowRanges = sheet.AllowEditRanges;
//定义保护范围
ProtectedRange proteced_range;
//创建范围
int idx = allowRanges.Add("r2", 1, 1, 3, 3);
proteced_range = allowRanges[idx];
//指定密码
proteced_range.Password = "123";
//保护工作表
sheet.Protect(ProtectionType.All);
//保存 Excel 文件
book.Save(dataDir + "protectedrange.out.xls");
```

## 结论

您现在已经学习了如何使用 Aspose.Cells for .NET 来允许用户编辑 Excel 电子表格中的特定范围。随意进一步探索 Aspose.Cells 提供的功能以满足您的特定需求。


### 常见问题

#### 1.如何允许用户编辑Excel电子表格中的特定范围？

您可以使用`ProtectedRangeCollection`定义允许修改范围的类。使用`Add`使用所需单元格创建新的受保护范围的方法。

#### 2.授权修改范围可以设置密码吗？

是的，您可以使用`Password`的财产`ProtectedRange`目的。这将限制只有拥有密码的用户才能访问。

#### 3.设置允许范围后如何保护电子表格？

使用`Protect`的方法`Worksheet`对象来保护工作表。这将防止任何超出允许范围的更改，如果您指定了密码，可能会提示输入密码。