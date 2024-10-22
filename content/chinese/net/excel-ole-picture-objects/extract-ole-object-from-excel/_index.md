---
title: 从 Excel 提取 OLE 对象
linktitle: 从 Excel 提取 OLE 对象
second_title: Aspose.Cells .NET Excel 处理 API
description: 了解如何使用 Aspose.Cells for .NET 从 Excel 文件中提取 OLE 对象。分步指南，轻松提取。
type: docs
weight: 10
url: /zh/net/excel-ole-picture-objects/extract-ole-object-from-excel/
---
## 介绍
在当今技术娴熟的世界里，处理 Excel 文件是一项常见任务，尤其是对于数据分析、财务和项目管理领域的人来说。一个经常被忽视的方面是 Excel 电子表格中 OLE（对象链接和嵌入）对象的处理。这些对象可能是嵌入的文档、图像，甚至是复杂的数据类型，它们在增强 Excel 文件的功能和丰富性方面起着至关重要的作用。如果您是 Aspose.Cells 用户，希望使用 .NET 以编程方式提取这些 OLE 对象，那么您来对地方了！本指南将逐步引导您完成该过程，确保您不仅了解如何操作，而且还了解该过程的每个部分为何如此重要。
## 先决条件
在我们深入研究提取 OLE 对象的具体细节之前，您必须做好以下几件事：
1. C# 基础知识：如果您熟悉 C#，那么您已经走在正确的道路上。如果不熟悉，也不用担心！我们会把事情讲得简单明了。
2. 已安装 Aspose.Cells：您需要 Aspose.Cells 库。您可以从网站下载[这里](https://releases.aspose.com/cells/net/).
3. 兼容的开发环境：确保您已设置好 .NET 开发环境，例如 Visual Studio。
4. 示例 Excel 文件：您需要一个嵌入了 OLE 对象的 Excel 文件来进行测试。 
一旦满足这些先决条件，我们就可以开始进入 OLE 对象提取的世界。
## 导入包
首先，让我们导入本教程中将要用到的必要包。在您的 C# 项目中，您需要包含 Aspose.Cells 命名空间。具体操作如下：
```csharp
using System.IO;
using Aspose.Cells;
```
## 步骤 1：设置文档目录
在此步骤中，我们将定义 Excel 文件所在的路径。您可能想知道为什么这很重要。这就像为演出搭建舞台一样 - 它可以帮助剧本知道在哪里找到演员（在我们的例子中是 Excel 文件）。
```csharp
string dataDir = "Your Document Directory";
```
代替`"Your Document Directory"`替换为 Excel 文件的实际路径（`book1.xls`) 被存储。
## 第 2 步：打开 Excel 文件
现在我们已经设置了文档目录，下一步是打开 Excel 文件。这就像在开始阅读之前先打开一本书——了解里面的内容至关重要。
```csharp
Workbook workbook = new Workbook(dataDir + "book1.xls");
```
## 步骤 3：访问 OLE 对象集合
Excel 工作簿中的每个工作表都可以包含各种对象，包括 OLE 对象。在这里，我们访问第一个工作表的 OLE 对象集合。这类似于选择一个页面来查看嵌入的图像和文档。
```csharp
Aspose.Cells.Drawing.OleObjectCollection oles = workbook.Worksheets[0].OleObjects;
```
## 步骤 4：循环遍历 OLE 对象
现在到了最有趣的部分——循环遍历我们集合中的所有 OLE 对象。这一步至关重要，因为它使我们能够高效地处理多个 OLE 对象。想象一下翻遍宝箱寻找贵重物品！
```csharp
for (int i = 0; i < oles.Count; i++)
{
    Aspose.Cells.Drawing.OleObject ole = oles[i];
    //处理每个对象的进一步逻辑
}
```
## 步骤 5：指定输出文件名
随着我们深入研究每个 OLE 对象，我们需要为提取的对象想出一个文件名。为什么？因为一旦我们提取它们，我们希望保持一切井然有序，以便我们以后可以轻松找到我们的宝藏。
```csharp
string fileName = dataDir + "ole_" + i + ".";
```
## 步骤 6：确定文件格式类型
每个 OLE 对象可以属于不同的类型（例如，文档、电子表格、图像）。确定格式类型对于正确提取至关重要。这就像了解一道菜的菜谱一样——您需要知道配料！
```csharp
switch (ole.FileFormatType)
{
    case FileFormatType.Doc:
        fileName += "doc";
        break;
    case FileFormatType.Xlsx:
        fileName += "xlsx";
        break;
    case FileFormatType.Ppt:
        fileName += "ppt";
        break;
    case FileFormatType.Pdf:
        fileName += "pdf";
        break;
    case FileFormatType.Unknown:
        fileName += "jpg";
        break;
    default:
        //处理其他文件格式
        break;
}
```
## 步骤 7：保存 OLE 对象
现在，让我们继续保存 OLE 对象。如果对象是 Excel 文件，我们将使用`MemoryStream`这使我们能够在写出数据之前处理内存中的数据。此步骤类似于在将您的财宝寄给朋友之前对其进行打包。
```csharp
if (ole.FileFormatType == FileFormatType.Xlsx)
{
    MemoryStream ms = new MemoryStream();
    ms.Write(ole.ObjectData, 0, ole.ObjectData.Length);
    Workbook oleBook = new Workbook(ms);
    oleBook.Settings.IsHidden = false;
    oleBook.Save(dataDir + "Excel_File" + i + ".out.xlsx");
}
```
对于其他类型的文件，我们将使用`FileStream`在磁盘上创建文件。
```csharp
else
{
    FileStream fs = File.Create(fileName);
    fs.Write(ole.ObjectData, 0, ole.ObjectData.Length);
    fs.Close();
}
```

## 结论
就这样，您已经成功地使用 Aspose.Cells for .NET 完成了 OLE 对象提取！按照以下步骤，您可以轻松地从 Excel 文件中提取和管理嵌入对象。请记住，就像任何宝贵的技能一样，熟能生巧。因此，花点时间尝试不同的 Excel 文件，很快您就会成为 OLE 提取专家！
## 常见问题解答
### Excel 中的 OLE 对象是什么？
OLE 对象是一种允许在 Excel 工作表中嵌入和链接到其他应用程序中的文档和数据的技术。
### 为什么我需要提取 OLE 对象？
提取 OLE 对象允许您独立于原始 Excel 文件访问和操作嵌入的文档或图像。
### Aspose.Cells 能处理所有类型的嵌入文件吗？
是的，Aspose.Cells 可以管理各种 OLE 对象，包括 Word 文档、Excel 工作表、PowerPoint 演示文稿和图像。
### 如何安装 Aspose.Cells for .NET？
您可以从他们的[发布页面](https://releases.aspose.com/cells/net/).
### 在哪里可以找到对 Aspose.Cells 的支持？
您可以在其上获得对 Aspose.Cells 的支持[支持论坛](https://forum.aspose.com/c/cells/9).