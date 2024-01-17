---
title: 保护 Excel 工作表
linktitle: 保护 Excel 工作表
second_title: Aspose.Cells for .NET API 参考
description: 在本教程中了解如何使用 Aspose.Cells for .NET 保护 Excel 电子表格。 C# 的分步指南。
type: docs
weight: 50
url: /zh/net/protect-excel-file/protect-excel-worksheet/
---
在本教程中，我们将查看一些使用 Aspose.Cells 库来保护 Excel 电子表格的 C# 源代码。我们将逐步完成代码的每个步骤并解释其工作原理。请务必仔细按照说明进行操作，以获得所需的结果。

## 第 1 步：先决条件

在开始之前，请确保您已安装适用于 .NET 的 Aspose.Cells 库。您可以从Aspose官方网站获取它。另请确保您拥有最新版本的 Visual Studio 或任何其他 C# 开发环境。

## 第2步：导入所需的命名空间

要使用 Aspose.Cells 库，我们需要将必要的命名空间导入到我们的代码中。将以下行添加到 C# 源文件的顶部：

```csharp
using Aspose.Cells;
using System.IO;
```

## 步骤 3：加载 Excel 文件

在此步骤中，我们将加载要保护的 Excel 文件。请务必指定包含 Excel 文件的目录的正确路径。使用以下代码上传文件：

```csharp
//文档目录的路径。
string dataDir = "YOUR_DIRECTORY_OF_DOCUMENTS";

//创建包含要打开的 Excel 文件的文件流。
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);

//实例化一个 Workbook 对象。
//通过文件流打开 Excel 文件。
Workbook excel = new Workbook(fstream);
```

一定要更换`"YOUR_DOCUMENTS_DIR"`与您的文档目录的适当路径。

## 第 4 步：访问电子表格

现在我们已经加载了 Excel 文件，我们可以访问第一个工作表。使用以下代码访问第一个工作表：

```csharp
//访问 Excel 文件中的第一个工作表。
Worksheet worksheet = excel.Worksheets[0];
```

## 步骤 5：保护工作表

在此步骤中，我们将使用密码保护电子表格。使用以下代码来保护电子表格：

```csharp
//使用密码保护工作表。
worksheet.Protect(ProtectionType.All, "YOUR_PASSWORD", null);
```

代替`"YOUR_PASSWORD"`以及您想要用来保护电子表格的密码。

## 第6步：保存修改后的Excel文件现在我们已经保护了

é 电子表格，我们将以默认格式保存修改后的 Excel 文件。使用以下代码保存Excel文件：

```csharp
//以默认格式保存修改后的 Excel 文件。
excel.Save(dataDir + "output.out.xls", SaveFormat.Excel97To2003);
```

确保指定正确的路径来保存修改后的 Excel 文件。

## 步骤7：关闭文件流

要释放所有资源，我们需要关闭用于加载 Excel 文件的文件流。使用以下代码关闭文件流：

```csharp
//关闭文件流以释放所有资源。
fstream.Close();
```

请务必将此步骤包含在代码末尾。


### 使用 Aspose.Cells for .NET 保护 Excel 工作表的示例源代码 
```csharp
//文档目录的路径。
string dataDir = "YOUR DOCUMENT DIRECTORY";
//创建包含要打开的 Excel 文件的文件流
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
//实例化 Workbook 对象
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

恭喜！您现在拥有 C# 源代码，可让您使用 .NET 的 Aspose.Cells 库保护 Excel 电子表格。请务必仔细遵循这些步骤并根据您的特定需求自定义代码。

### 常见问题解答（常见问题）

#### 是否可以在一个 Excel 文件中保护多个工作表？

答：是的，您可以通过对每个工作表重复步骤 4-6 来保护一个 Excel 文件中的多个工作表。

#### 如何为授权用户指定特定权限？

答：您可以使用由`Protect`方法为授权用户指定特定权限。有关更多信息，请参阅 Aspose.Cells 文档。

#### 我可以使用密码保护 Excel 文件本身吗？

答：是的，您可以使用 Aspose.Cells 库提供的其他方法对 Excel 文件本身进行密码保护。具体示例请参考文档。

#### Aspose.Cells 库是否支持其他 Excel 文件格式？

答：是的，Aspose.Cells 库支持多种 Excel 文件格式，包括 XLSX、XLSM、XLSB、CSV 等。