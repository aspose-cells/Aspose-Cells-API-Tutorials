---
title: Excel 工作表的高级保护设置
linktitle: Excel 工作表的高级保护设置
second_title: Aspose.Cells for .NET API 参考
description: 通过使用 Aspose.Cells for .NET 设置高级保护设置来保护您的 Excel 文件。
type: docs
weight: 10
url: /zh/net/excel-security/advanced-protection-settings-for-excel-worksheet/
---
在本教程中，我们将引导您完成使用 .NET 的 Aspose.Cells 库为 Excel 电子表格设置高级保护设置的步骤。请按照以下说明完成此任务。

## 第 1 步：准备

确保您已安装 Aspose.Cells for .NET 并在您首选的集成开发环境 (IDE) 中创建了 C# 项目。

## 第二步：设置文档目录路径

声明一个`dataDir`变量并使用文档目录的路径对其进行初始化。例如 ：

```csharp
string dataDir = "YOUR_DIRECTORY_OF_DOCUMENTS";
```

一定要更换`"YOUR_DOCUMENTS_DIRECTORY"`与目录的实际路径。

## 步骤 3：创建文件流以打开 Excel 文件

创建一个`FileStream`包含要打开的 Excel 文件的对象：

```csharp
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
```

确保您有 Excel 文件`book1.xls`在您的文档目录中或指定正确的文件名和位置。

## 步骤 4：实例化 Workbook 对象并打开 Excel 文件

使用`Workbook`Aspose.Cells 中的类实例化 Workbook 对象并通过文件流打开指定的 Excel 文件：

```csharp
Workbook excel = new Workbook(fstream);
```

## 第 5 步：访问第一个工作表

导航到 Excel 文件的第一个工作表：

```csharp
Worksheet worksheet = excel.Worksheets[0];
```

## 步骤 6：设置工作表保护设置

使用工作表对象属性根据需要设置工作表保护设置。例如 ：

```csharp
worksheet.Protection.AllowDeletingColumn = false;
worksheet.Protection.AllowDeletingRow = false;
worksheet.Protection.AllowEditingContent = false;
worksheet.Protection.AllowEditingObject = false;
// ...根据需要设置其他保护设置...
```

## 步骤7：保存修改后的Excel文件

使用以下命令保存修改后的 Excel 文件`Save`Workbook对象的方法：

```csharp
excel.Save(dataDir + "output.xls", SaveFormat.Excel97To2003);
```

请务必指定输出文件所需的路径和文件名。

## 第8步：关闭文件流

保存后，关闭文件流以释放所有关联资源：

```csharp
fstream.Close();
```
	
### 使用 Aspose.Cells for .NET 的 Excel 工作表高级保护设置的示例源代码 
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
//限制用户删除工作表的列
worksheet.Protection.AllowDeletingColumn = false;
//限制用户删除工作表的行
worksheet.Protection.AllowDeletingRow = false;
//限制用户编辑工作表内容
worksheet.Protection.AllowEditingContent = false;
//限制用户编辑工作表的对象
worksheet.Protection.AllowEditingObject = false;
//限制用户编辑工作表的场景
worksheet.Protection.AllowEditingScenario = false;
//限制用户过滤
worksheet.Protection.AllowFiltering = false;
//允许用户设置工作表单元格的格式
worksheet.Protection.AllowFormattingCell = true;
//允许用户设置工作表行的格式
worksheet.Protection.AllowFormattingRow = true;
//允许用户在工作表中插入列
worksheet.Protection.AllowFormattingColumn = true;
//允许用户在工作表中插入超链接
worksheet.Protection.AllowInsertingHyperlink = true;
//允许用户在工作表中插入行
worksheet.Protection.AllowInsertingRow = true;
//允许用户选择工作表的锁定单元格
worksheet.Protection.AllowSelectingLockedCell = true;
//允许用户选择工作表中未锁定的单元格
worksheet.Protection.AllowSelectingUnlockedCell = true;
//允许用户排序
worksheet.Protection.AllowSorting = true;
//允许用户在工作表中使用数据透视表
worksheet.Protection.AllowUsingPivotTable = true;
//保存修改后的Excel文件
excel.Save(dataDir + "output.xls", SaveFormat.Excel97To2003);
//关闭文件流以释放所有资源
fstream.Close();
```

## 结论

恭喜！您现在已经了解了如何使用 Aspose.Cells for .NET 为 Excel 电子表格设置高级保护设置。使用这些知识来保护您的 Excel 文件并限制用户操作。

### 常见问题解答

#### 问：如何在 IDE 中创建新的 C# 项目？

答：创建新 C# 项目的步骤可能会有所不同，具体取决于您使用的 IDE。有关详细说明，请参阅 IDE 的文档。

#### 问：除了教程中提到的设置之外，是否可以设置自定义保护设置？

答：是的，Aspose.Cells 提供了广泛的保护设置，您可以根据自己的特定需求进行自定义。有关更多详细信息，请参阅 Aspose.Cells 文档。

#### Q：示例代码中修改后的Excel文件用什么文件格式保存？

答：示例代码中，修改后的Excel文件以Excel 97-2003（.xls）格式保存。如果需要，您可以选择 Aspose.Cells 支持的其他格式。

#### 问：如何访问 Excel 文件中的其他工作表？

答：您可以使用索引或工作表名称访问其他工作表，例如：`Worksheet worksheet = excel.Worksheets[1];`或者`Worksheet worksheet = excel.Worksheets[" SheetName"];`.