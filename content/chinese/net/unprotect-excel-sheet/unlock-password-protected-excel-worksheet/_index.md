---
title: 解锁受密码保护的 Excel 工作表
linktitle: 解锁受密码保护的 Excel 工作表
second_title: Aspose.Cells for .NET API 参考
description: 了解如何使用 Aspose.Cells for .NET 解锁受密码保护的 Excel 电子表格。 C# 分步教程。
type: docs
weight: 10
url: /zh/net/unprotect-excel-sheet/unlock-password-protected-excel-worksheet/
---
Excel 电子表格的密码保护通常用于保护敏感数据。在本教程中，我们将逐步指导您理解和实现所提供的 C# 源代码，以使用适用于 .NET 的 Aspose.Cells 库解锁受密码保护的 Excel 电子表格。

## 第一步：准备环境

开始之前，请确保您的计算机上安装了 Aspose.Cells for .NET。您可以从Aspose官方网站下载该库并按照提供的说明进行安装。

安装完成后，在您首选的集成开发环境 (IDE) 中创建一个新的 C# 项目，并导入适用于 .NET 的 Aspose.Cells 库。

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

现在我们将使用以下命令解锁工作表`Unprotect()`Worksheet 对象的方法。将密码字符串留空（`""`) 如果电子表格不受密码保护。

```csharp
//使用密码取消对工作表的保护
worksheet.Unprotect("");
```

## 步骤 6：保存解锁的 Excel 文件

电子表格解锁后，我们可以保存最终的 Excel 文件。使用`Save()`指定输出文件的完整路径的方法

.

```csharp
//保存工作簿
workbook.Save(dataDir + "output.out.xls");
```

### 使用 Aspose.Cells for .NET 解锁受密码保护的 Excel 工作表的示例源代码 
```csharp
try
{
    //文档目录的路径。
    string dataDir = "YOUR DOCUMENT DIRECTORY";
    //实例化 Workbook 对象
    Workbook workbook = new Workbook(dataDir + "book1.xls");
    //访问 Excel 文件中的第一个工作表
    Worksheet worksheet = workbook.Worksheets[0];
    //使用密码取消对工作表的保护
    worksheet.Unprotect("");
    //保存工作簿
    workbook.Save(dataDir + "output.out.xls");
}
catch (Exception ex)
{
    Console.WriteLine(ex.Message);
    Console.ReadLine();
}
```

## 结论

恭喜！您现在已经了解了如何使用 Aspose.Cells for .NET 使用 C# 源代码解锁受密码保护的 Excel 电子表格。通过遵循本教程中的步骤，您可以将此功能应用到您自己的项目中，并高效、安全地处理 Excel 文件。

请随意进一步探索 Aspose.Cells 提供的功能以实现更高级的操作。

### 常见问题解答

#### 问：如果电子表格受密码保护怎么办？

答：如果电子表格受密码保护，您必须在`Unprotect()`方法能够解锁它。

#### 问：解锁受保护的 Excel 电子表格时有什么限制或注意事项吗？

答：是的，请确保您拥有解锁电子表格所需的权限。此外，使用此功能时请务必遵循组织的安全策略。