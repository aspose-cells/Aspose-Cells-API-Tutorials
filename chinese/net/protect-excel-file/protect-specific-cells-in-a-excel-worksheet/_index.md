---
title: 保护 Excel 工作表中的特定单元格
linktitle: 保护 Excel 工作表中的特定单元格
second_title: Aspose.Cells for .NET API 参考
description: 了解如何使用 Aspose.Cells for .NET 保护 Excel 中的特定单元格。 C# 中的分步教程。
type: docs
weight: 70
url: /zh/net/protect-excel-file/protect-specific-cells-in-a-excel-worksheet/
---
在本教程中，我们将查看使用 Aspose.Cells 库保护 Excel 电子表格中特定单元格的 C# 源代码。我们将遍历代码的每个步骤并解释它是如何工作的。仔细按照说明进行操作以获得所需的结果。

## 第 1 步：先决条件

在开始之前，请确保您已经安装了用于 .NET 的 Aspose.Cells 库。您可以从 Aspose 官网获取。还要确保您拥有最新版本的 Visual Studio 或任何其他 C# 开发环境。

## 第 2 步：导入所需的命名空间

要使用 Aspose.Cells 库，我们需要将必要的命名空间导入到我们的代码中。将以下行添加到 C# 源文件的顶部：

```csharp
using Aspose.Cells;
```

## 第 3 步：创建 Excel 工作簿

在此步骤中，我们将创建一个新的 Excel 工作簿。使用以下代码创建 Excel 工作簿：

```csharp
//文档目录的路径。
string dataDir = "YOUR_DIRECTORY_OF_DOCUMENTS";

//创建一个新的工作簿。
Workbook wb = new Workbook();
```

务必更换`"YOUR_DOCUMENTS_DIR"`使用文档目录的适当路径。

## 第 4 步：创建电子表格

现在我们已经创建了 Excel 工作簿，让我们创建一个工作表并获取第一个工作表。使用以下代码：

```csharp
//创建一个电子表格对象并获取第一个工作表。
Worksheet sheet = wb.Worksheets[0];
```

## 第 5 步：定义样式

在此步骤中，我们将定义应用于特定单元格的样式。使用以下代码：

```csharp
//样式对象的定义。
Styling styling;
```

## 第 6 步：循环解锁所有列

现在我们将遍历工作表中的所有列并解锁它们。使用以下代码：

```csharp
//遍历工作表中的所有列并解锁它们。
for (int i = 0; i <= 255; i++)
{
     style = sheet.Cells.Columns[(byte)i].Style;
     style. IsLocked = false;
     sheet.Cells.Columns[(byte)i].ApplyStyle(style);
}
```

## 第 7 步：锁定特定单元格

在这一步中，我们将锁定特定的单元格。使用以下代码：

```csharp
//锁定所有三个单元格...即 A1、B1、C1。
style = sheet.Cells["A1"].GetStyle();
style. IsLocked = true;
sheet.Cells["A1"].SetStyle(style);

style = sheet.Cells["B1"].GetStyle();
style. IsLocked = true;
sheet.Cells["B1"].SetStyle(style);

style = sheet.Cells["C1"].GetStyle();
style. IsLocked = true;
sheet.Cells["C1"].SetStyle(style);
```

## 步骤 8：保护工作表

最后，我们将保护工作表以防止特定单元格被修改。使用以下代码：

```csharp
//保护工作表。
sheet.Protect(ProtectionType.All);
```

## 第 9 步：保存 Excel 文件

我们现在将保存修改后的 Excel 文件。使用以下代码：

```csharp
//保存 Excel 文件。
wb.Save(dataDir + "output.out.xls", SaveFormat.Excel97To2003);
```

确保指定正确的路径以保存修改后的 Excel 文件。

### 使用 Aspose.Cells for .NET 保护 Excel 工作表中特定单元格的示例源代码 
```csharp
//文档目录的路径。
string dataDir = "YOUR DOCUMENT DIRECTORY";
//如果目录不存在，则创建目录。
bool IsExists = System.IO.Directory.Exists(dataDir);
if (!IsExists)
    System.IO.Directory.CreateDirectory(dataDir);
//创建一个新的工作簿。
Workbook wb = new Workbook();
//创建工作表对象并获取第一张工作表。
Worksheet sheet = wb.Worksheets[0];
//定义样式对象。
Style style;
//定义样式标志对象
StyleFlag styleflag;
//遍历工作表中的所有列并解锁它们。
for (int i = 0; i <= 255; i++)
{
    style = sheet.Cells.Columns[(byte)i].Style;
    style.IsLocked = false;
    styleflag = new StyleFlag();
    styleflag.Locked = true;
    sheet.Cells.Columns[(byte)i].ApplyStyle(style, styleflag);
}
//锁定三个单元格...即 A1、B1、C1。
style = sheet.Cells["A1"].GetStyle();
style.IsLocked = true;
sheet.Cells["A1"].SetStyle(style);
style = sheet.Cells["B1"].GetStyle();
style.IsLocked = true;
sheet.Cells["B1"].SetStyle(style);
style = sheet.Cells["C1"].GetStyle();
style.IsLocked = true;
sheet.Cells["C1"].SetStyle(style);
//最后，现在保护工作表。
sheet.Protect(ProtectionType.All);
//保存 excel 文件。
wb.Save(dataDir + "output.out.xls", SaveFormat.Excel97To2003);
```


## 结论

恭喜！您现在拥有 C# 源代码，允许您使用 .NET 的 Aspose.Cells 库保护 Excel 工作表中的特定单元格。随意自定义代码以满足您的特定需求。

### FAQ（常见问题）

#### 此代码是否适用于最新版本的 Excel？

是的，此代码适用于最新版本的 Excel，包括 Excel 2010 及更高版本格式的文件。

#### 我可以保护除 A1、B1 和 C1 之外的其他电池吗？

是的，您可以通过调整相应代码行中的单元格引用来修改代码以锁定其他特定单元格。

#### 我怎样才能再次解锁锁定的单元格？

您可以使用`SetStyle`方法与`IsLocked`设置`false`解锁细胞。

#### 我可以向工作簿中添加更多工作表吗？

是的，您可以使用`Worksheets.Add()`方法并为每个工作表重复细胞保护步骤。

#### 如何更改Excel文件的保存格式？

您可以使用更改保存格式`SaveFormat`具有所需格式的方法，例如`SaveFormat.Xlsx`适用于 Excel 2007 及更高版本。