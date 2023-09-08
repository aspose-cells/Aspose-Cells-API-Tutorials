---
title: 编辑 Excel 工作表中的范围
linktitle: 编辑 Excel 工作表中的范围
second_title: Aspose.Cells for .NET API 参考
description: 了解使用 Aspose.Cells for .NET 编辑 Excel 电子表格中的特定范围。 C# 分步教程。
type: docs
weight: 20
url: /zh/net/protect-excel-file/edit-ranges-in-excel-worksheet/
---
Microsoft Excel 是用于创建和管理电子表格的强大工具，提供许多控制和保护数据的功能。其中一项功能是允许用户编辑工作表中的特定范围，同时保护其他部分。在本教程中，我们将逐步指导您使用 Aspose.Cells for .NET（一个用于以编程方式处理 Excel 文件的流行库）来实现此功能。

使用 Aspose.Cells for .NET 将允许您轻松操作 Excel 电子表格中的范围，提供用户友好的界面和高级功能。按照以下步骤允许用户使用 Aspose.Cells for .NET 编辑 Excel 电子表格中的特定范围。
## 第一步：搭建环境

确保您的开发环境中安装了 Aspose.Cells for .NET。从Aspose官方网站下载库并查看文档以获取安装说明。

## 第2步：初始化工作簿和工作表

首先，我们需要创建一个新工作簿并获取对要允许更改范围的工作表的引用。使用以下代码来实现此目的：

```csharp
//文档目录的路径。
string dataDir = "YOUR DOCUMENTS DIRECTORY";
//如果该目录尚不存在，则创建该目录。
bool exists = System.IO.Directory.Exists(dataDir);
if (! exists)
     System.IO.Directory.CreateDirectory(dataDir);

//实例化新工作簿
Workbook workbook = new Workbook();

//获取第一个工作表（默认）
Worksheet sheet = workbook.Worksheets[0];
```

在此代码片段中，我们首先定义保存 Excel 文件的目录路径。接下来，我们创建一个新的实例`Workbook`类并使用以下命令获取对第一个工作表的引用`Worksheets`财产。

## 第 3 步：获取可编辑范围

现在我们需要检索我们想要允许修改的范围。使用以下代码：

```csharp
//获取可修改范围
ProtectedRangeCollection EditableRanges = Sheet.AllowEditRanges;
```

## 第四步：设置保护范围

在允许修改范围之前，我们需要定义一个受保护的范围。就是这样：

```csharp
//定义保护范围
ProtectedRange ProtectedRange;

//创建范围
int index = ModifiableRanges.Add("r2", 1, 1, 3, 3);
rangeProtected = rangesEditable[index];
```

在此代码中，我们创建了一个新实例`ProtectedRange`类并使用`Add`方法指定要保护的范围。

## 第 5 步：指定密码

为了增强安全性，您可以为保护范围指定密码。就是这样：

```csharp
//指定密码
protectedBeach.Password = "YOUR_PASSWORD";
```

## 步骤 6：保护工作表

既然我们已经设置了保护范围，我们就可以保护工作表以防止未经授权的修改。使用以下代码：

```csharp
//保护工作表
leaf.Protect(ProtectionType.All);
```

## 步骤 7：保存 Excel 文件

最后，我们保存所做更改的 Excel 文件。这是必要的代码：

```csharp
//保存 Excel 文件
workbook.Save(dataDir + "protectedrange.out.xls");
```

### 使用 Aspose.Cells for .NET 在 Excel 工作表中编辑范围的示例源代码 
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
proteced_range.Password = "YOUR_PASSWORD";

//保护板材
sheet.Protect(ProtectionType.All);

//保存 Excel 文件
book.Save(dataDir + "protectedrange.out.xls");
```

## 结论

恭喜！您学习了如何允许用户使用 Aspose.Cells for .NET 编辑 Excel 电子表格中的特定范围。您现在可以在自己的项目中应用此技术并提高 Excel 文件的安全性。


#### 常见问题解答

#### 问：为什么我应该使用 Aspose.Cells for .NET 来编辑 Excel 电子表格中的范围？

答：Aspose.Cells for .NET 提供了强大且易于使用的 API 来处理 Excel 文件。它提供了高级功能，例如范围操作、工作表保护等。

#### 问：我可以在工作表中设置多个可编辑范围吗？

答：是的，您可以使用`Add`的方法`ProtectedRangeCollection`收藏。每个范围都可以有自己的保护设置。

####  问：定义可编辑范围后是否可以将其删除？

答：是的，您可以使用`RemoveAt`的方法`ProtectedRangeCollection`集合通过指定其索引来删除特定的可编辑范围。

#### 问：保存后如何打开受保护的 Excel 文件？

答：您需要提供创建保护范围时指定的密码才能打开受保护的 Excel 文件。请务必将密码保存在安全的地方，以防止丢失数据访问权限。