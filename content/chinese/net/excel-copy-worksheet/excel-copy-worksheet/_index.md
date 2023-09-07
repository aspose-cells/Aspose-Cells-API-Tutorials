---
title: Excel 复制工作表
linktitle: Excel 复制工作表
second_title: Aspose.Cells for .NET API 参考
description: 使用 Aspose.Cells for .NET 将一个 Excel 工作表复制到另一个。
type: docs
weight: 20
url: /zh/net/excel-copy-worksheet/excel-copy-worksheet/
---

在本指南中，我们将解释如何使用 .NET 的 Aspose.Cells 库复制 Excel 工作表。我们将为您提供 C# 源代码，并引导您完成完成此任务所需的步骤。最后，我们将向您展示预期的结果。请按照以下说明开始操作。

## 第 1 步：准备

在开始之前，请确保您已安装 Aspose.Cells for .NET 并在您首选的集成开发环境 (IDE) 中创建了一个 C# 项目。另请确保您拥有要操作的 Excel 文件的副本。

## 第2步：导入所需的库

在 C# 源文件中，使用以下命令从 Aspose.Cells 导入必要的库`using`指示：

```csharp
using Aspose.Cells;
```

## 第三步：设置文件路径

声明一个`dataDir`变量并使用包含 Excel 文件的目录对其进行初始化。例如 ：

```csharp
string dataDir = "PATH_TO_YOUR_DOCUMENT_DIRECTORY";
```

一定要更换`"PATH_TO_YOUR_DOCUMENT_DIRECTORY"`与目录的实际路径。

## 第 4 步：加载现有 Excel 文件

使用`Workbook`Aspose.Cells 中的类来打开现有的 Excel 文件。使用`InputPath`变量来指定文件路径：

```csharp
string InputPath = dataDir + "book1.xls";
Workbook wb = new Workbook(InputPath);
```

确保您已更换`"book1.xls"`与 Excel 文件的实际名称。

## 第 5 步：复制工作表

现在我们将现有工作表复制到新工作表。使用`Worksheets`的财产`Workbook`对象来访问工作表集合：

```csharp
WorksheetCollection sheets = wb.Worksheets;
```

然后使用`AddCopy`方法复制指定的工作表。例如，要复制“Sheet1”：

```csharp
sheets.AddCopy("Sheet1");
```

## 第 6 步：保存 Excel 文件

使用`Save`的方法`Workbook`对象将更改保存到新文件：

```csharp
wb.Save(dataDir + "CopyWithinWorkbook_out.xls");
```

请务必指定输出文件所需的路径和文件名。

### 使用 Aspose.Cells for .NET 的 Excel 复制工作表的示例源代码 

```csharp
//文档目录的路径。
string dataDir = "YOUR DOCUMENT DIRECTORY";
string InputPath = dataDir + "book1.xls";
//打开现有的 Excel 文件。
Workbook wb = new Workbook(InputPath);
//创建一个 Worksheets 对象，参考
//工作簿的工作表。
WorksheetCollection sheets = wb.Worksheets;
//将数据从现有工作表复制到新工作表
//工作簿中的工作表。
sheets.AddCopy("Sheet1");
//保存 Excel 文件。
wb.Save(dataDir + "CopyWithinWorkbook_out.xls");
```

## 结论

恭喜！您现在已经了解了如何使用 Aspose.Cells for .NET 复制 Excel 工作表。本分步指南展示了如何导入必要的库、加载现有 Excel 文件、复制工作表以及保存修改后的文件。请随意在您自己的项目中使用此方法来高效地操作 Excel 文件。

### 常见问题解答

#### 问：Aspose.Cells 与其他编程语言兼容吗？

A. 是的，Aspose.Cells 支持多种编程语言，包括 C#、Java、Python 等。

#### 问：我可以将工作表复制到另一个 Excel 工作簿吗？

A. 是的，您可以使用`AddCopy`方法将一个工作表复制到另一个 Excel 工作簿。

#### 问：复制工作表时，Aspose.Cells 是否保留公式和格式？

A. 是的，Aspose.Cells 在复制工作表时保留公式、格式和其他属性。

#### 问：Aspose.Cells 是否需要商业使用许可证？

A. 是的，Aspose.Cells 是一个商业产品，需要购买商业用途的许可证。您可以在 Aspose 的官方网站上找到更多许可信息。