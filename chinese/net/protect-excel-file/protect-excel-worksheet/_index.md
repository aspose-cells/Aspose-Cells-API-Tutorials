---
title: 保护 Excel 工作表
linktitle: 保护 Excel 工作表
second_title: Aspose.Cells for .NET API 参考
description: 在本教程中了解如何使用 Aspose.Cells for .NET 保护 Excel 电子表格。 C# 中的分步指南。
type: docs
weight: 50
url: /zh/net/protect-excel-file/protect-excel-worksheet/
---
在本教程中，我们将查看一些使用 Aspose.Cells 库保护 Excel 电子表格的 C# 源代码。我们将遍历代码的每个步骤并解释它是如何工作的。请务必仔细按照说明进行操作以获得所需的结果。

## 第 1 步：先决条件

在开始之前，请确保您已经安装了用于 .NET 的 Aspose.Cells 库。您可以从 Aspose 官网获取。还要确保您拥有最新版本的 Visual Studio 或任何其他 C# 开发环境。

## 第 2 步：导入所需的命名空间

要使用 Aspose.Cells 库，我们需要将必要的命名空间导入到我们的代码中。将以下行添加到 C# 源文件的顶部：

```csharp
using Aspose.Cells;
using System.IO;
```

## 第 3 步：加载 Excel 文件

在此步骤中，我们将加载要保护的 Excel 文件。请务必指定包含 Excel 文件的目录的正确路径。使用以下代码上传文件：

```csharp
//文档目录的路径。
string dataDir = "YOUR_DIRECTORY_OF_DOCUMENTS";

//创建包含要打开的 Excel 文件的文件流。
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);

//实例化工作簿对象。
//通过文件流打开 Excel 文件。
Workbook excel = new Workbook(fstream);
```

务必更换`"YOUR_DOCUMENTS_DIR"`使用文档目录的适当路径。

## 第 4 步：访问电子表格

现在我们已经加载了 Excel 文件，我们可以访问第一个工作表。使用以下代码访问第一个工作表：

```csharp
//访问 Excel 文件中的第一个工作表。
Worksheet worksheet = excel.Worksheets[0];
```

## 步骤 5：保护工作表

在此步骤中，我们将使用密码保护电子表格。使用以下代码保护电子表格：

```csharp
//使用密码保护工作表。
worksheet.Protect(ProtectionType.All, "YOUR_PASSWORD", null);
```

代替`"YOUR_PASSWORD"`使用您要用来保护电子表格的密码。

## 第 6 步：保存修改后的 Excel 文件 现在我们已经保护了

在电子表格中，我们将以默认格式保存修改后的 Excel 文件。使用以下代码保存 Excel 文件：

```csharp
//以默认格式保存修改后的 Excel 文件。
excel.Save(dataDir + "output.out.xls", SaveFormat.Excel97To2003);
```

确保指定正确的路径以保存修改后的 Excel 文件。

## 步骤 7：关闭文件流

要释放所有资源，我们需要关闭用于加载 Excel 文件的文件流。使用以下代码关闭文件流：

```csharp
//关闭文件流以释放所有资源。
fstream.Close();
```

请务必在代码末尾包含此步骤。


### 使用 Aspose.Cells for .NET 保护 Excel 工作表的示例源代码 
```csharp
//文档目录的路径。
string dataDir = "YOUR DOCUMENT DIRECTORY";
//创建包含要打开的 Excel 文件的文件流
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
//实例化工作簿对象
//通过文件流打开Excel文件
Workbook excel = new Workbook(fstream);
//访问 Excel 文件中的第一个工作表
Worksheet worksheet = excel.Worksheets[0];
//使用密码保护工作表
worksheet.Protect(ProtectionType.All, "aspose", null);
//以默认格式保存修改后的 Excel 文件
excel.Save(dataDir + "output.out.xls", SaveFormat.Excel97To2003);
//关闭文件流以释放所有资源
fstream.Close();
```

## 结论

恭喜！您现在拥有 C# 源代码，允许您使用 .NET 的 Aspose.Cells 库保护 Excel 电子表格。请务必仔细遵循这些步骤并根据您的特定需求自定义代码。

### FAQ（常见问题）

#### 是否可以在一个 Excel 文件中保护多个工作表？
答：是的，您可以通过对每个工作表重复步骤 4-6 来保护一个 Excel 文件中的多个工作表。

#### 如何为授权用户指定特定权限？
答：您可以使用`Protect`为授权用户指定特定权限的方法。有关详细信息，请参阅 Aspose.Cells 文档。

#### 我可以使用密码保护 Excel 文件本身吗？
答：是的，您可以使用 Aspose.Cells 库提供的其他方法对 Excel 文件本身进行密码保护。具体例子请参考文档。

#### Aspose.Cells 库是否支持其他 Excel 文件格式？
A：是的，Aspose.Cells 库支持广泛的 Excel 文件格式，包括 XLSX、XLSM、XLSB、CSV 等。