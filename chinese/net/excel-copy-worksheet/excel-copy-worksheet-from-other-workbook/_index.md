---
title: Excel 从其他工作簿复制工作表
linktitle: Excel 从其他工作簿复制工作表
second_title: Aspose.Cells for .NET API 参考
description: 使用 Aspose.Cells for .NET 轻松将 Excel 工作表从一个工作簿复制到另一个工作簿。
type: docs
weight: 10
url: /zh/net/excel-copy-worksheet/excel-copy-worksheet-from-other-workbook/
---
在本教程中，我们将引导您完成使用 .NET 的 Aspose.Cells 库从另一个工作簿复制 Excel 工作表的步骤。请按照以下说明完成此任务。

## 第 1 步：准备

在开始之前，请确保您已安装 Aspose.Cells for .NET 并在您首选的集成开发环境 (IDE) 中创建了一个 C# 项目。

## 第二步：设置文档目录路径

声明一个`dataDir`变量并使用文档目录的路径对其进行初始化。例如 ：

```csharp
string dataDir = "YOUR_DIRECTORY_OF_DOCUMENTS";
```

一定要更换`"YOUR_DOCUMENTS_DIRECTORY"`与目录的实际路径。

## 步骤 3：创建新的 Excel 工作簿

使用`Workbook`来自 Aspose.Cells 的类来创建新的 Excel 工作簿：

```csharp
Workbook excelWorkbook0 = new Workbook();
```

## 步骤 4：获取工作簿中的第一个工作表

使用索引 0 导航到工作簿中的第一个工作表：

```csharp
Worksheet ws0 = excelWorkbook0.Worksheets[0];
```

## 步骤 5：将数据添加到标题行 (A1:A4)

用一个`for`循环将数据添加到标题行 (A1:A4)：

```csharp
for (int i = 0; i < 5; i++)
{
     ws0.Cells[i, 0].PutValue(string.Format("Header row {0}", i));
}
```

## 步骤 6：添加详细数据 (A5:A999)

使用另一个`for`循环添加详细数据（A5：A999）：

```csharp
for (int i = 5; i < 1000; i++)
{
     ws0.Cells[i, 0].PutValue(string.Format("Detail row {0}", i));
}
```

## 第 7 步：设置布局选项

使用以下命令设置工作表的页面设置选项`PageSetup`目的：

```csharp
PageSetup pagesetup = ws0.PageSetup;
pagesetup.PrintTitleRows = "$1:$5";
```

## 步骤 8：创建另一个 Excel 工作簿

创建另一个 Excel 工作簿：

```csharp
Workbook excelWorkbook1 = new Workbook();
```

## 步骤 9：从第二个工作簿中获取第一个工作表

导航到第二个工作簿中的第一个工作表：

```csharp
Worksheet ws1 = excelWorkbook1.Worksheets[0];
```

## 第 10 步：为工作表命名

为火命名

计算岛：

```csharp
ws1.Name = "MySheet";
```

## 步骤 11：将数据从第一个工作簿的第一个工作表复制到第二个工作簿的第一个工作表

将数据从第一个工作簿的第一个工作表复制到第二个工作簿的第一个工作表：

```csharp
ws1.Copy(ws0);
```

## 第12步：保存Excel文件

保存 Excel 文件：

```csharp
excelWorkbook1.Save(dataDir + "CopyWorkbookSheetToOther_out.xls");
```

请务必指定输出文件所需的路径和文件名。

### 使用 Aspose.Cells for .NET 从其他工作簿复制工作表的 Excel 示例源代码 
```csharp
//文档目录的路径。
string dataDir = "YOUR DOCUMENT DIRECTORY";
//创建一个新的工作簿。
Workbook excelWorkbook0 = new Workbook();
//获取本书中的第一个工作表。
Worksheet ws0 = excelWorkbook0.Worksheets[0];
//将一些数据放入标题行 (A1:A4)
for (int i = 0; i < 5; i++)
{
	ws0.Cells[i, 0].PutValue(string.Format("Header Row {0}", i));
}
//放一些详细数据（A5：A999）
for (int i = 5; i < 1000; i++)
{
	ws0.Cells[i, 0].PutValue(string.Format("Detail Row {0}", i));
}
//根据第一个工作表定义 pagesetup 对象。
PageSetup pagesetup = ws0.PageSetup;
//前五行在每页中重复...
//可以在打印预览中看到。
pagesetup.PrintTitleRows = "$1:$5";
//创建另一个工作簿。
Workbook excelWorkbook1 = new Workbook();
//获取本书中的第一个工作表。
Worksheet ws1 = excelWorkbook1.Worksheets[0];
//为工作表命名。
ws1.Name = "MySheet";
//将第一个工作簿的第一个工作表中的数据复制到
//第二个工作簿的第一个工作表。
ws1.Copy(ws0);
//保存 Excel 文件。
excelWorkbook1.Save(dataDir + "CopyWorksheetFromWorkbookToOther_out.xls");
```

## 结论

恭喜！您现在已经了解了如何使用 Aspose.Cells for .NET 从另一个工作簿复制 Excel 工作表。请随意在您自己的项目中使用此方法来高效地操作 Excel 文件。

### 常见问题解答

#### 问：使用 Aspose.Cells for .NET 需要哪些库？

A. 要使用 Aspose.Cells for .NET，您必须在项目中包含 Aspose.Cells 库。确保您在集成开发环境 (IDE) 中正确引用了该库。

#### 问：Aspose.Cells 是否支持其他 Excel 文件格式，例如 XLSX？

A. 是的，Aspose.Cells 支持各种 Excel 文件格式，包括 XLSX、XLS、CSV、HTML 等。您可以使用 Aspose.Cells for .NET 的功能来操作这些文件格式。

#### 问：复制工作表时我可以自定义布局选项吗？

A. 是的，您可以在复制工作表时使用工作表的属性自定义页面设置选项。`PageSetup`目的。您可以指定页眉、页脚、边距、方向等。