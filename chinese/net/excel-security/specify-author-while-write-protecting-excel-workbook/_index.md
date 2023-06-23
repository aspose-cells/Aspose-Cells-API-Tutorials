---
title: 在写入保护 Excel 工作簿时指定作者
linktitle: 在写入保护 Excel 工作簿时指定作者
second_title: Aspose.Cells for .NET API 参考
description: 了解如何使用 Aspose.Cells for .NET 保护和自定义 Excel 工作簿。 C# 分步教程。
type: docs
weight: 30
url: /zh/net/excel-security/specify-author-while-write-protecting-excel-workbook/
---

在本教程中，我们将向您展示如何在使用 .NET 的 Aspose.Cells 库对 Excel 工作簿进行写保护时指定作者。

## 第一步：准备环境

开始之前，请确保您的计算机上安装了 Aspose.Cells for .NET。从 Aspose 官方网站下载该库并按照提供的安装说明进行操作。

## 第 2 步：配置源目录和输出目录

在提供的源代码中，您必须指定源目录和输出目录。修改`sourceDir`和`outputDir`通过将“YOUR SOURCE DIRECTORY”和“YOUR OUTPUT DIRECTORY”替换为计算机上相应的绝对路径来更改变量。

```csharp
//源码目录
string sourceDir = "PATH TO YOUR SOURCE DIRECTORY";

//输出目录
string outputDir = "YOUR OUTPUT DIRECTORY PATH";
```

## 步骤 3：创建一个空的 Excel 工作簿

首先，我们创建一个代表空 Excel 工作簿的 Workbook 对象。

```csharp
//创建空工作簿。
Workbook wb = new Workbook();
```

## 第四步：用密码写保护

接下来，我们使用以下命令指定一个密码来写保护 Excel 工作簿`WriteProtection.Password`Workbook 对象的属性。

```csharp
//使用密码写入保护工作簿。
wb.Settings.WriteProtection.Password = "YOUR_PASSWORD";
```

## 第 5 步：作者说明

现在我们使用以下命令指定 Excel 工作簿的作者`WriteProtection.Author`Workbook 对象的属性。

```csharp
//写入保护工作簿时指定作者。
wb.Settings.WriteProtection.Author = "YOUR_AUTHOR";
```

## 步骤 6：备份受保护的 Excel 工作簿

一旦指定了写保护和作者，我们就可以使用以下命令将 Excel 工作簿保存为 XLSX 格式：`Save()`方法。

```csharp
//将工作簿保存为 XLSX 格式。
wb.Save(outputDir + "outputSpecifyAuthorWhileWriteProtectingWorkbook.xlsx");
```

### 使用 Aspose.Cells for .NET 写入保护 Excel 工作簿时指定作者的示例源代码 
```csharp
//源码目录
string sourceDir = "YOUR SOURCE DIRECTORY";

//输出目录
string outputDir = "YOUR OUTPUT DIRECTORY";

//创建空工作簿。
Workbook wb = new Workbook();

//使用密码写入保护工作簿。
wb.Settings.WriteProtection.Password = "YOUR_PASSWORD";

//写入保护工作簿时指定作者。
wb.Settings.WriteProtection.Author = "YOUR_AUTHOR";

//将工作簿保存为 XLSX 格式。
wb.Save(outputDir + "outputSpecifyAuthorWhileWriteProtectingWorkbook.xlsx");

```

## 结论

恭喜！您现在已经了解了如何在使用 Aspose.Cells for .NET 对 Excel 工作簿进行写保护时指定作者。您可以将这些步骤应用到您自己的项目中，以保护和自定义您的 Excel 工作簿。

请随意进一步探索 Aspose.Cells for .NET 的功能，以对 Excel 文件进行更高级的操作。

## 常见问题解答

#### 问：我可以在不指定密码的情况下对 Excel 工作簿进行写保护吗？

答：是的，您可以使用 Workbook 对象的`WriteProtect()`方法无需指定密码即可对 Excel 工作簿进行写保护。这将限制对工作簿的更改，而无需密码。

#### 问：如何取消 Excel 工作簿的写保护？

答：要取消 Excel 工作簿的写保护，您可以使用`Unprotect()`Worksheet 对象的方法或`RemoveWriteProtection()`Workbook 对象的方法，具体取决于您的具体用例。 。

#### 问：我忘记了保护 Excel 工作簿的密码。我能做些什么 ？

答：如果您忘记了保护 Excel 工作簿的密码，则无法直接将其删除。但是，您可以尝试使用专门的第三方工具，为受保护的 Excel 文件提供密码恢复功能。

#### 问：对 Excel 工作簿进行写保护时是否可以指定多个作者？

答：不可以，Aspose.Cells for .NET 库允许在对 Excel 工作簿进行写保护时指定单个作者。如果要指定多个作者，则需要考虑通过直接操作 Excel 文件来自定义解决方案。