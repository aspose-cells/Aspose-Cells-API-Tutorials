---
title: 使用 Aspose.Cells 保护工作表中的行
linktitle: 使用 Aspose.Cells 保护工作表中的行
second_title: Aspose.Cells .NET Excel 处理 API
description: 了解如何使用 Aspose.Cells for .NET 保护 Excel 工作表中的行。使用行级保护保护您的数据并防止意外更改。
type: docs
weight: 18
url: /zh/net/worksheet-security/protect-rows/
---
## 介绍
以编程方式处理 Excel 文件通常是一项不仅需要数据操作还需要数据保护的任务。无论您需要保护敏感数据还是防止意外编辑，保护工作表中的行都是至关重要的一步。在本教程中，我们将深入研究如何使用 Aspose.Cells for .NET 保护 Excel 工作表中的特定行。我们将以简单易懂的方式介绍所有必要的步骤，从准备环境到实施保护功能。
## 先决条件
在开始保护工作表中的行之前，您需要做好以下几件事：
1.  Aspose.Cells for .NET：确保您的开发机器上安装了 Aspose.Cells for .NET。如果您尚未完成此操作，您可以轻松从[Aspose Cells 下载页面](https://releases.aspose.com/cells/net/).
2. Visual Studio 或任何 .NET IDE：要实施解决方案，您需要设置开发环境。Visual Studio 是一个很好的选择，但任何兼容 .NET 的 IDE 都可以使用。
3. 基本 C# 知识：了解 C# 编程的基础知识将帮助您跟随教程并修改示例代码以满足您的需要。
4.  Aspose.Cells API 文档：熟悉[Aspose.Cells for .NET 文档](https://reference.aspose.com/cells/net/)获得库中使用的类结构和方法的概述。
如果您已满足所有先决条件，我们就可以直接开始实施。
## 导入包
首先，您需要导入所需的包。这些库对于在 C# 项目中与 Excel 文件交互至关重要。
```csharp
using System.IO;
using Aspose.Cells;
```
一旦导入了必要的包，就可以开始编码。 
现在，让我们将流程分解为更小的步骤，让您轻松遵循。每个步骤将侧重于实施的特定部分，确保您能够快速理解和应用它。 
## 步骤 1：创建新的工作簿和工作表
在应用任何保护设置之前，您需要创建一个新的工作簿并选择要使用的工作表。这将是您的工作文档。
```csharp
//文档目录的路径。
string dataDir = "Your Document Directory";
//如果目录尚不存在，则创建目录。
bool IsExists = System.IO.Directory.Exists(dataDir);
if (!IsExists)
	System.IO.Directory.CreateDirectory(dataDir);
//创建新工作簿。
Workbook wb = new Workbook();
//创建一个工作表对象并获取第一个工作表。
Worksheet sheet = wb.Worksheets[0];
```
在此示例中，我们将创建一个包含单个工作表的新工作簿（这是使用 Aspose.Cells 创建新工作簿时的默认设置）。然后，我们获取工作簿中的第一个工作表，这将是我们行保护的目标。
## 第 2 步：定义 Style 和 StyleFlag 对象
下一步是定义样式和样式标志对象。这些对象允许您修改单元格的属性，例如它是锁定还是解锁。
```csharp
//定义样式对象。
Style style;
//定义 styleflag 对象。
StyleFlag flag;
```
您将在后面的步骤中使用这些对象来自定义单元格属性并将其应用到您的工作表。
## 步骤 3：解锁工作表中的所有列
默认情况下，Excel 工作表中的所有单元格都是锁定的。但是，当您保护工作表时，锁定状态将被强制执行。要确保只有特定的行或单元格受到保护，您可以先解锁所有列。如果您只想保护某些行，此步骤至关重要。
```csharp
//循环遍历工作表中的所有列并将其解锁。
for (int i = 0; i <= 255; i++)
{
    style = sheet.Cells.Columns[(byte)i].Style;
    style.IsLocked = false;
    flag = new StyleFlag();
    flag.Locked = true;
    sheet.Cells.Columns[(byte)i].ApplyStyle(style, flag);
}
```
在此代码中，我们循环遍历工作表中的所有 256 列（Excel 工作表最多有 256 列，索引从 0 到 255），并设置它们的`IsLocked`财产`false`。此操作确保所有列均已解锁，但我们稍后仍将锁定特定行。
## 步骤 4：锁定第一行
解锁列后，下一步是锁定要保护的特定行。在此示例中，我们将锁定第一行。这可确保用户无法修改它，而其他行仍处于解锁状态。
```csharp
//获取第一行样式。
style = sheet.Cells.Rows[0].Style;
//锁上。
style.IsLocked = true;
//实例化标志。
flag = new StyleFlag();
//设定锁定设置。
flag.Locked = true;
//将样式应用到第一行。
sheet.Cells.ApplyRowStyle(0, style, flag);
```
在这里，我们访问第一行的样式并设置其`IsLocked`财产`true`之后，我们使用`ApplyRowStyle()`方法将锁定样式应用于整行。您可以重复此步骤来锁定您想要保护的任何其他行。
## 步骤 5：保护工作表
现在我们已经解锁和锁定了必要的行，是时候保护工作表了。保护可确保除非删除保护密码（如果提供），否则任何人都无法修改锁定的行或单元格。
```csharp
//保护纸张。
sheet.Protect(ProtectionType.All);
```
在此步骤中，我们使用`ProtectionType.All`。这种保护意味着工作表的所有方面（包括锁定的行和单元格）都受到保护。您还可以根据需要通过指定不同的保护类型来自定义此保护。
## 步骤 6：保存工作簿
最后，我们需要在应用必要的样式和保护后保存工作簿。工作簿可以保存为多种格式，例如Excel 97-2003，Excel 2010等。
```csharp
//保存 Excel 文件。
wb.Save(dataDir + "output.out.xls", SaveFormat.Excel97To2003);
```
这行代码将工作簿保存为 Excel 97-2003 格式，并应用更改。您可以根据需要选择多种文件格式来更改文件格式`SaveFormat`选项。
## 结论
就这样！您已经成功学会了如何使用 Aspose.Cells for .NET 保护工作表中的行。按照上述步骤，您可以根据需要解锁或锁定任何行或列，并应用保护以确保数据的完整性。
## 常见问题解答
### 我怎样才能同时保护多行？  
您可以循环遍历多行并将锁定样式分别应用于每一行。只需替换`0`使用您想要锁定的行索引。
### 我可以设置工作表保护密码吗？  
是的！您可以将密码传递给`sheet.Protect()`强制密码保护的方法。
### 我可以解锁单元格而不是整个列吗？  
是的！您无需解锁列，只需修改单元格的样式属性即可解锁单个单元格。
### 如果我尝试编辑受保护的行会发生什么？  
当某行受到保护时，Excel 将阻止对锁定的单元格进行任何编辑，除非您取消对工作表的保护。
### 我可以连续保护特定范围吗？  
是的！您可以通过设置`IsLocked`范围内特定单元格的属性。