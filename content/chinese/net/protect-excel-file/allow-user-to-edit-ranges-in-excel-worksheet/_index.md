---
title: 允许用户编辑 Excel 工作表中的范围
linktitle: 允许用户编辑 Excel 工作表中的范围
second_title: Aspose.Cells for .NET API 参考
description: 允许用户使用 Aspose.Cells for .NET 编辑 Excel 电子表格中的特定范围。带有 C# 源代码的分步指南。
type: docs
weight: 10
url: /zh/net/protect-excel-file/allow-user-to-edit-ranges-in-excel-worksheet/
---
在本指南中，我们将引导您了解如何使用 Aspose.Cells for .NET 来允许用户编辑 Excel 电子表格中的特定范围。请按照以下步骤完成此任务。

## 第一步：搭建环境

确保您已设置开发环境并安装 Aspose.Cells for .NET。您可以从Aspose官方网站下载最新版本的库。

## 第2步：导入所需的命名空间

在您的 C# 项目中，导入必要的命名空间以使用 Aspose.Cells：

```csharp
using Aspose.Cells;
```

## 第三步：设置文档目录路径

声明一个`dataDir`变量来指定要保存生成的 Excel 文件的目录的路径：

```csharp
string dataDir = "YOUR_DIRECTORY_OF_DOCUMENTS";
```

一定要更换`"YOUR_DOCUMENT_DIRECTORY"`与系统上的正确路径。

## 第 4 步：创建工作簿对象

实例化一个新的 Workbook 对象，该对象代表要创建的 Excel 工作簿：

```csharp
Workbook book = new Workbook();
```

## 第 5 步：访问第一个工作表

使用以下代码导航到 Excel 工作簿中的第一个工作表：

```csharp
Worksheet sheet = book.Worksheets[0];
```

## 步骤 6：检索授权修改范围

使用以下命令获取允许编辑范围的集合`AllowEditRanges`财产：

```csharp
ProtectedRangeCollection allowRanges = sheet.AllowEditRanges;
```

## 步骤 7：定义保护范围

使用以下命令定义受保护范围`Add`的方法`AllowEditRanges`收藏：

```csharp
int idx = allowRanges.Add("r2", 1, 1, 3, 3);
protectedRange protectedRange = allowRanges[idx];
```

在这里，我们创建了一个从单元格 A1 到单元格 C3 的受保护范围“r2”。

## 步骤 8：指定密码

使用以下命令指定受保护范围的密码`Password`财产：

```csharp
protectedRange.Password = "YOUR_PASSWORD";
```

一定要更换`"YOUR_PASSWORD"`使用所需的密码。

## 步骤 9：保护工作表

使用以下命令保护工作表`Protect`的方法`Worksheet`目的：

```csharp
sheet.Protect(ProtectionType.All);
```

这将通过防止任何超出允许范围的修改来保护电子表格。

## 第 10 步：注册

  Excel文件

使用以下命令保存生成的 Excel 文件`Save`的方法`Workbook`目的：

```csharp
book.Save(dataDir + "protectedrange.out.xls");
```

请务必指定所需的文件名和正确的路径。

### 允许用户使用 Aspose.Cells for .NET 在 Excel 工作表中编辑范围的示例源代码 
```csharp
//文档目录的路径。
string dataDir = "YOUR DOCUMENT DIRECTORY";
//如果目录尚不存在，则创建该目录。
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
//保护板材
sheet.Protect(ProtectionType.All);
//保存 Excel 文件
book.Save(dataDir + "protectedrange.out.xls");
```

## 结论

您现在已经了解了如何使用 Aspose.Cells for .NET 来允许用户编辑 Excel 电子表格中的特定范围。请随意进一步探索 Aspose.Cells 提供的功能来满足您的特定需求。


### 常见问题解答

#### 1. 如何允许用户编辑Excel电子表格中的特定范围？

您可以使用`ProtectedRangeCollection`类来定义允许的修改范围。使用`Add`方法用所需的单元格创建新的受保护范围。

#### 2. 授权修改范围可以设置密码吗？

是的，您可以使用指定密码`Password`的财产`ProtectedRange`目的。这将限制仅具有密码的用户进行访问。

#### 3. 设置允许的范围后，如何保护电子表格？

使用`Protect`的方法`Worksheet`对象保护工作表。这将防止任何超出允许范围的更改，如果您指定了密码，可能会提示输入密码。