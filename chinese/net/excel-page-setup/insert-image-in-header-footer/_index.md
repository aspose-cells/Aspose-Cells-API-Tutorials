---
title: 在页眉页脚中插入图像
linktitle: 在页眉页脚中插入图像
second_title: Aspose.Cells for .NET API 参考
description: 了解如何使用 Aspose.Cells for .NET 将图像插入到 Excel 文档的页眉或页脚中。使用 C# 编写源代码的分步指南。
type: docs
weight: 60
url: /zh/net/excel-page-setup/insert-image-in-header-footer/
---
在 Excel 文档的页眉或页脚中插入图像的功能对于自定义报告或添加公司徽标非常有用。在本文中，我们将逐步指导您使用 Aspose.Cells for .NET 在 Excel 文档的页眉或页脚中插入图像。您将学习如何使用 C# 源代码完成此操作。

## 第 1 步：设置环境

在开始之前，请确保您的机器上安装了 Aspose.Cells for .NET。还要在您喜欢的开发环境中创建一个新项目。

## 第二步：导入必要的库

在您的代码文件中，导入使用 Aspose.Cells 所需的库。下面是相应的代码：

```csharp
using Aspose.Cells;
```

## 第三步：设置文档目录

设置要使用的 Excel 文档所在的目录。使用以下代码设置目录：

```csharp
string dataDir = "YOUR DOCUMENTS DIRECTORY";
```

请务必指定完整的目录路径。

## 第 4 步：创建工作簿对象

Workbook 对象表示您将使用的 Excel 文档。您可以使用以下代码创建它：

```csharp
Workbook workbook = new Workbook();
```

这将创建一个新的空工作簿对象。

## 第 5 步：存储图像 URL

定义要在页眉或页脚中插入的图像的 URL 或路径。使用以下代码存储图像 URL：

```csharp
string logo_url = dataDir + "aspose-logo.jpg";
```

确保指定的路径正确并且图像存在于该位置。

## 第 6 步：打开图像文件

要打开图像文件，我们将使用 FileStream 对象并从图像中读取二进制数据。下面是相应的代码：

```csharp
FileStream inFile;
byte[] binaryData;

inFile = new System.IO.FileStream(logo_url, System.IO.FileMode.Open, System.IO.FileAccess.Read);
binaryData = new Byte[inFile.Length];
long bytesRead = inFile.Read(binaryData, 0, (int)inFile.Length);
```

确保图像路径正确并且您具有访问它的正确权限。

## 第 7 步：配置页面设置

PageSetup 对象用于设置 Excel 文档页面设置，包括页眉和页脚。使用以下代码获取第一个工作表的 PageSetup 对象：

```csharp
PageSetup pageSetup = workbook. Worksheets

[0].PageSetup;
```

这将允许您访问工作簿中第一个工作表的页面设置。

## 第 8 步：将图像添加到页眉

使用 PageSetup 对象的 SetHeaderPicture() 方法在页眉的中间部分设置图像。下面是相应的代码：

```csharp
pageSetup.SetHeaderPicture(1, binaryData);
```

这会将指定的图像添加到页眉。

## 第 9 步：将脚本添加到标头

要将脚本添加到页眉，请使用 PageSetup 对象的 SetHeader() 方法。下面是相应的代码：

```csharp
pageSetup.SetHeader(1, "&G");
```

这会将指定的脚本添加到页眉。在此示例中，“&G”脚本显示页码。

## 第 10 步：将工作表名称添加到页眉

要在页眉中显示工作表名称，请再次使用 PageSetup 对象的 SetHeader() 方法。下面是相应的代码：

```csharp
pageSetup.SetHeader(2, "&A");
```

这会将工作表名称添加到页眉。 “&A”脚本用于表示工作表名称。

## 步骤 11：保存工作簿

要保存对工作簿的更改，请使用 Workbook 对象的 Save() 方法。下面是相应的代码：

```csharp
workbook.Save(dataDir + "InsertImageInHeaderFooter_out.xls");
```

这会将包含更改的工作簿保存到指定目录。

## 第 12 步：关闭 FileStream

从图像中读取二进制数据后，一定要关闭 FileStream 以释放资源。使用以下代码关闭 FileStream：

```csharp
inFile.Close();
```

确保在使用完 FileStreams 后始终将其关闭。

### 使用 Aspose.Cells for .NET 在页眉页脚中插入图像的示例源代码 
```csharp
//文档目录的路径。
string dataDir = "YOUR DOCUMENT DIRECTORY";
//创建工作簿对象
Workbook workbook = new Workbook();
//创建一个字符串变量来存储徽标/图片的 url
string logo_url = dataDir + "aspose-logo.jpg";
//声明一个 FileStream 对象
FileStream inFile;
//声明一个字节数组
byte[] binaryData;
//创建 FileStream 对象的实例以在流中打开徽标/图片
inFile = new System.IO.FileStream(logo_url, System.IO.FileMode.Open, System.IO.FileAccess.Read);
//实例化 FileStream 对象大小的字节数组
binaryData = new Byte[inFile.Length];
//从流中读取一个字节块并将数据写入给定的字节数组缓冲区。
long bytesRead = inFile.Read(binaryData, 0, (int)inFile.Length);
//创建PageSetup对象获取工作簿第一个工作表的页面设置
PageSetup pageSetup = workbook.Worksheets[0].PageSetup;
//在页眉的中央部分设置徽标/图片
pageSetup.SetHeaderPicture(1, binaryData);
//设置徽标/图片的脚本
pageSetup.SetHeader(1, "&G");
//使用脚本在页眉的右侧部分设置工作表名称
pageSetup.SetHeader(2, "&A");
//保存工作簿
workbook.Save(dataDir + "InsertImageInHeaderFooter_out.xls");
//关闭 FileStream 对象
inFile.Close();       
```
## 结论

恭喜！您现在知道如何使用 Aspose.Cells for .NET 在 Excel 文档的页眉或页脚中插入图像。本教程向您介绍了该过程的每一步，从设置环境到保存修改后的工作簿。随意尝试更多 Aspose.Cells 的功能来创建个性化和专业的 Excel 文档。

### 常见问题解答

#### Q1：Excel文档的页眉页脚可以插入多张图片吗？

A1：是的，您可以通过对每个附加图像重复步骤 8 和 9 将多个图像插入 Excel 文档的页眉或页脚。

#### Q2：在页眉或页脚中插入支持哪些图像格式？
A2：Aspose.Cells支持JPEG、PNG、GIF、BMP等多种常见图片格式。

#### Q3：我可以进一步自定义页眉或页脚的外观吗？

A3：是的，您可以使用特殊的脚本和代码来进一步格式化和自定义页眉或页脚的外观。有关自定义选项的更多信息，请参阅 Aspose.Cells 文档。

#### Q4：Aspose.Cells 是否适用于不同版本的 Excel？

A4：是的，Aspose.Cells兼容不同版本的Excel，包括Excel 2003、Excel 2007、Excel 2010、Excel 2013、Excel 2016和Excel 2019。

#### Q5：是否可以在Excel文档的其他部分插入图片，比如单元格或图表？

A5：是的，Aspose.Cells 提供了将图像插入到 Excel 文档的不同部分的广泛功能，包括单元格、图表和绘图对象。