---
title: 以编程方式使用 Excel 中的内置数字格式
linktitle: 以编程方式使用 Excel 中的内置数字格式
second_title: Aspose.Cells .NET Excel 处理 API
description: 使用 Aspose.Cells for .NET 自动格式化 Excel 中的数字。了解如何以编程方式应用日期、百分比和货币格式。
type: docs
weight: 10
url: /zh/net/number-and-display-formats-in-excel/using-built-in-number-formats/
---
## 介绍
在本教程中，我们将引导您了解如何使用 Aspose.Cells for .NET 在 Excel 中使用内置数字格式。我们将介绍从设置环境到应用不同格式（如日期、百分比和货币）的所有内容。无论您是经验丰富的专业人士还是刚刚涉足 .NET 生态系统，本指南都可以让您轻松格式化 Excel 单元格。
## 先决条件
在深入研究之前，请确保您已准备好以下事项：
- 已安装 Aspose.Cells for .NET 库。您可以[点击下载](https://releases.aspose.com/cells/net/).
- 具备 C# 和基本 .NET 编程的工作知识。
- 您的机器上安装有 Visual Studio 或任何 .NET IDE。
- 有效的 Aspose 许可证或[临时执照](https://purchase.aspose.com/temporary-license/).
- 安装.NET框架（4.0或更高版本）。
  
如果您缺少上述任何一项，请按照提供的链接进行设置。准备好了吗？让我们进入有趣的部分吧！
## 导入包
在开始本教程之前，请确保导入使用 Aspose.Cells for .NET 所需的命名空间：
```csharp
using System.IO;
using Aspose.Cells;
using System;
```
导入这些文件后，您就可以以编程方式操作 Excel 文件了。现在，让我们深入了解分步指南！
## 步骤 1：创建或访问您的 Excel 工作簿
在此步骤中，您将创建一个新的工作簿。您可以将其视为打开一个新的 Excel 文件，只不过您是通过代码来完成的！
```csharp
//文档目录的路径。
string dataDir = "Your Document Directory";
//如果目录尚不存在，则创建目录。
bool IsExists = System.IO.Directory.Exists(dataDir);
if (!IsExists)
	System.IO.Directory.CreateDirectory(dataDir);
//实例化 Workbook 对象
Workbook workbook = new Workbook();
```
这里我们只是实例化了一个新的`Workbook`对象。这充当您的 Excel 文件，可供数据操作。您还可以通过提供其路径来加载现有文件。
## 第 2 步：访问工作表
Excel 工作簿可以包含多个工作表。在此步骤中，我们将访问工作簿中的第一个工作表：
```csharp
Worksheet worksheet = workbook.Worksheets[0];
```
我们现在正在访问工作簿中的第一个工作表。如果您需要操作其他工作表，可以使用其索引或名称来引用它们。
## 步骤 3：向单元格添加数据
让我们开始向特定单元格添加一些数据。首先，我们将当前系统日期插入单元格“A1”中：
```csharp
worksheet.Cells["A1"].PutValue(DateTime.Now);
```
此行将当前日期插入单元格 A1。很酷，对吧？想象一下手动对数百个单元格执行此操作 - 这将是一场噩梦。现在，我们继续进行格式化！
## 步骤 4：在单元格“A1”中格式化日期
接下来，让我们将该日期格式化为更易读的格式，例如“15-Oct-24”。这是 Aspose.Cells 真正出彩的地方：
1. 检索单元格的样式：
```csharp
Style style = worksheet.Cells["A1"].GetStyle();
```
这里，我们获取单元格 A1 的样式。可以将其视为在进行任何调整之前获取单元格的“样式”。
2.设置日期格式：
```csharp
style.Number = 15;
```
设置`Number`属性设置为 15 即可应用所需的日期格式。这是内置的数字格式代码，用于以“d-mmm-yy”格式显示日期。
3. 将样式应用于单元格：
```csharp
worksheet.Cells["A1"].SetStyle(style);
```
此行将样式更改应用于单元格。现在，您将看到更加用户友好的日期格式，而不是默认日期格式，例如“15-Oct-24”。
## 步骤 5：在单元格“A2”中添加并设置百分比格式
让我们继续格式化百分比。假设您想要插入一个值并将其显示为百分比。在此步骤中，我们将向单元格“A2”添加一个数值并将其格式化为百分比：
1. 插入数值：
```csharp
worksheet.Cells["A2"].PutValue(20);
```
这会将数字 20 插入到单元格 A2 中。您可能会想，“这只是一个普通的数字 — 我如何将其转换为百分比？”好吧，我们即将开始讨论。
2. 检索样式并设置百分比格式：
```csharp
style = worksheet.Cells["A2"].GetStyle();
style.Number = 9;  //格式为百分比
worksheet.Cells["A2"].SetStyle(style);
    ```
Setting the `Number` property to 9 applies the built-in percentage format. Now the value in A2 will be displayed as "2000%." (Yes, 20 is treated as 2000% in percentage formatting).
## Step 6: Add and Format Currency in Cell "A3"
Now, let’s add a numeric value in cell A3 and format it as currency. This is a common use case for financial reports.
1. Insert Numeric Value:
```csharp
worksheet.Cells["A3"].PutValue(2546);
```
在这里，我们将 2546 添加到单元格 A3。接下来，我们将格式化此数字以显示为货币。
2. 检索样式并设置货币格式：
```csharp
style = worksheet.Cells["A3"].GetStyle();
style.Number = 6;  //格式化为货币
worksheet.Cells["A3"].SetStyle(style);
```
设置`Number`属性设置为 6 则应用货币格式。现在单元格 A3 中的值将显示为“2,546.00”，带有逗号和两位小数。
## 步骤 7：保存 Excel 文件
现在我们已经应用了所有的格式化魔法，是时候保存文件了：
```csharp
//保存 Excel 文件
workbook.Save(dataDir + "book1.out.xls", SaveFormat.Excel97To2003);
```
此行将 Excel 文件保存为 Excel 97-2003 格式。您可以更改`SaveFormat`以满足您的需求。就这样，您已经以编程方式创建并格式化了一个 Excel 文件！
## 结论
恭喜！您已成功学会如何使用 Aspose.Cells for .NET 将内置数字格式应用于 Excel 文件中的单元格。从日期到百分比和货币，我们涵盖了 Excel 数据处理的一些最常见的格式化需求。现在，您无需手动格式化单元格，而是可以自动化整个过程 - 节省时间并减少错误。
## 常见问题解答
### 我可以使用 Aspose.Cells for .NET 应用自定义数字格式吗？
是的！除了内置格式外，Aspose.Cells 还支持自定义数字格式。您可以使用`Custom`财产在`Style`班级。
### 如何将单元格格式化为具有特定符号的货币？
要应用特定的货币符号，您可以通过设置自定义格式来`Style.Custom`财产。
### 我可以格式化整行或整列吗？
当然！您可以使用`Rows`或者`Columns`收藏品`Worksheet`目的。
### 如何一次性格式化多个单元格？
您可以使用`Range`对象来选择多个单元格并一次性将样式应用于它们。
### 我需要安装 Microsoft Excel 才能使用 Aspose.Cells 吗？
不是，Aspose.Cells 独立于 Microsoft Excel 运行，因此您的机器上不需要安装 Excel。