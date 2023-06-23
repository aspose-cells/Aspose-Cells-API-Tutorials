---
title: Excel 在工作簿之间复制工作表
linktitle: Excel 在工作簿之间复制工作表
second_title: Aspose.Cells for .NET API 参考
description: 使用 Aspose.Cells for .NET 在 Excel 工作簿之间轻松复制工作表。
type: docs
weight: 30
url: /zh/net/excel-copy-worksheet/excel-copy-worksheets-between-workbooks/
---
在本教程中，我们将指导您完成使用 .NET 的 Aspose.Cells 库在 Excel 工作簿之间复制工作表的步骤。请按照以下说明完成此任务。

## 第 1 步：准备

确保您已安装 Aspose.Cells for .NET 并在您首选的集成开发环境 (IDE) 中创建了 C# 项目。

## 第二步：设置文档目录路径

声明一个`dataDir`变量并使用文档目录的路径对其进行初始化。例如 ：

```csharp
string dataDir = "YOUR_DIRECTORY_OF_DOCUMENTS";
```

一定要更换`"YOUR_DOCUMENTS_DIRECTORY"`与目录的实际路径。

## 第三步：定义输入文件路径

声明一个`InputPath`变量并使用要从中复制电子表格的 Excel 文件的完整路径对其进行初始化。例如 ：

```csharp
string InputPath = dataDir + "book1.xls";
```

确保您有 Excel 文件`book1.xls`在您的文档目录中或指定正确的文件名和位置。

## 步骤 4：创建第一个 Excel 工作簿

使用`Workbook`Aspose.Cells 类创建第一个 Excel 工作簿并打开指定文件：

```csharp
Workbook excelWorkbook0 = new Workbook(InputPath);
```

## 步骤 5：创建第二个 Excel 工作簿

创建第二个 Excel 工作簿：

```csharp
Workbook excelWorkbook1 = new Workbook();
```

## 步骤 6：将工作表从第一个工作簿复制到第二个工作簿

使用`Copy`将第一个工作表从第一个工作簿复制到第二个工作簿的方法：

```csharp
excelWorkbook1.Worksheets[0].Copy(excelWorkbook0.Worksheets[0]);
```

## 第7步：保存Excel文件

保存包含复制的电子表格的 Excel 文件：

```csharp
excelWorkbook1.Save(dataDir + "Copy WorksheetsBetweenWorkbooks_out.xls");
```

请务必指定输出文件所需的路径和文件名。

### 使用 Aspose.Cells for .NET 在工作簿之间复制工作表的 Excel 示例源代码 
```csharp
//文档目录的路径。
string dataDir = "YOUR DOCUMENT DIRECTORY";
string InputPath = dataDir + "book1.xls";
//创建工作簿。
//打开第一本书中的文件。
Workbook excelWorkbook0 = new Workbook(InputPath);
//创建另一个工作簿。
Workbook excelWorkbook1 = new Workbook();
//将第一本书的第一页复制到第二本书中。
excelWorkbook1.Worksheets[0].Copy(excelWorkbook0.Worksheets[0]);
//保存文件。
excelWorkbook1.Save(dataDir + "CopyWorksheetsBetweenWorkbooks_out.xls");
```

## 结论

恭喜！您现在已经了解了如何使用 Aspose.Cells for .NET 在 Excel 工作簿之间复制工作表。请随意在您自己的项目中使用此方法来高效地操作 Excel 文件。

### 常见问题解答

#### 问：使用 Aspose.Cells for .NET 需要哪些库？

A. 要使用 Aspose.Cells for .NET，您必须在项目中包含 Aspose.Cells 库。确保您在集成开发环境 (IDE) 中正确引用了该库。

#### 问：Aspose.Cells 是否支持其他 Excel 文件格式，例如 XLSX？

A. 是的，Aspose.Cells 支持各种 Excel 文件格式，包括 XLSX、XLS、CSV、HTML 等。您可以使用 Aspose.Cells for .NET 的功能来操作这些文件格式。

#### 问：复制电子表格时我可以自定义布局选项吗？

A. 是的，您可以在使用电子表格的属性复制电子表格时自定义页面设置选项。`PageSetup`目的。您可以指定页眉、页脚、边距、方向等。