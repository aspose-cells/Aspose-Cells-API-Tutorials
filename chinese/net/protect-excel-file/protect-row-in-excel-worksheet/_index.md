---
title: 保护 Excel 工作表中的行
linktitle: 保护 Excel 工作表中的行
second_title: Aspose.Cells for .NET API 参考
description: 在本教程中了解如何使用 Aspose.Cells for .NET 保护 Excel 电子表格的行。 C# 中的分步教程。
type: docs
weight: 60
url: /zh/net/protect-excel-file/protect-row-in-excel-worksheet/
---
在本教程中，我们将查看一些使用 Aspose.Cells 库保护 Excel 电子表格中的行的 C# 源代码。我们将遍历代码的每个步骤并解释它是如何工作的。仔细按照说明进行操作以获得所需的结果。

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

在此步骤中，我们将定义应用于电子表格行的样式。使用以下代码：

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

## 第七步：锁定第一行

在此步骤中，我们将锁定工作表的第一行。使用以下代码：

```csharp
//获取第一行的样式。
style = sheet.Cells.Rows[0].Style;
//锁定样式。
style. IsLocked = true;
//将样式应用于第一行。
sheet.Cells.ApplyRowStyle(0, style);
```

## 步骤 8：保护工作表

现在我们已经设置了样式并锁定了行，让我们保护电子表格。使用以下代码：

```csharp
//保护工作表。
sheet.Protect(ProtectionType.All);
```

## 第 9 步：保存 Excel 文件

最后，我们将保存修改后的 Excel 文件。使用以下代码：

```csharp
//保存 Excel 文件。
wb.Save(dataDir + "output.out.xls", SaveFormat.Excel97To2003);
```

确保指定正确的路径以保存修改后的 Excel 文件。

### 使用 Aspose.Cells for .NET 在 Excel 工作表中保护行的示例源代码 
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
//定义样式标志对象。
StyleFlag flag;
//遍历工作表中的所有列并解锁它们。
for (int i = 0; i <= 255; i++)
{
    style = sheet.Cells.Columns[(byte)i].Style;
    style.IsLocked = false;
    flag = new StyleFlag();
    flag.Locked = true;
    sheet.Cells.Columns[(byte)i].ApplyStyle(style, flag);
}
//获取第一行样式。
style = sheet.Cells.Rows[0].Style;
//锁定它。
style.IsLocked = true;
//实例化标志。
flag = new StyleFlag();
//设置锁定设置。
flag.Locked = true;
//将样式应用于第一行。
sheet.Cells.ApplyRowStyle(0, style, flag);
//保护床单。
sheet.Protect(ProtectionType.All);
//保存 excel 文件。
wb.Save(dataDir + "output.out.xls", SaveFormat.Excel97To2003);
```

## 结论

恭喜！您现在拥有 C# 源代码，允许您使用 .NET 的 Aspose.Cells 库保护 Excel 电子表格中的行。请务必仔细遵循这些步骤并根据您的特定需求自定义代码。

### FAQ（常见问题）

#### 此代码是否适用于最新版本的 Excel？
是的，此代码适用于最新版本的 Excel，包括 Excel 2010 及更高版本格式的文件。

#### 我可以只保护特定行而不是工作表中的所有行吗？
是的，您可以修改代码以指定要保护的特定行。您将需要相应地调整循环和索引。

#### 如何再次解锁锁定的线路？
您可以使用`IsLocked`的方法`Style`将值设置为的对象`false`并解锁行。

#### 是否可以保护同一个 Excel 工作簿中的多个工作表？
是的，您可以重复创建工作表、设置样式和保护工作簿中每个工作表的步骤。

#### 如何更改电子表格保护密码？
您可以使用更改密码`Protect`方法并将新密码指定为参数。