---
title: 控制工作表的缩放系数
linktitle: 控制工作表的缩放系数
second_title: Aspose.Cells for .NET API 参考
description: 使用 Aspose.Cells for .NET 控制 Excel 工作表的缩放系数。
type: docs
weight: 20
url: /zh/net/excel-display-settings-csharp-tutorials/controll-zoom-factor-of-worksheet/
---
使用 .NET 的 Aspose.Cells 库处理 Excel 文件时，控制工作表的缩放系数是一项重要功能。在本指南中，我们将逐步向您展示如何使用 Aspose.Cells 使用 C# 源代码控制工作表的缩放系数。

## 第1步：导入所需的库

在开始之前，请确保您已安装适用于 .NET 的 Aspose.Cells 库并将必要的库导入到您的 C# 项目中。

```csharp
using System;
using System.IO;
using Aspose.Cells;
```

## 第2步：设置目录路径并打开Excel文件

首先，设置包含 Excel 文件的目录的路径，然后使用`FileStream`对象并实例化`Workbook`对象来表示 Excel 工作簿。

```csharp
string dataDir = "YOUR DOCUMENTS DIRECTORY";
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
Workbook workbook = new Workbook(fstream);
```

## 步骤 3：访问电子表格并更改缩放系数

在此步骤中，我们使用索引访问 Excel 工作簿的第一个工作表`0`并将工作表缩放系数设置为`75`.

```csharp
Worksheet worksheet = workbook.Worksheets[0];
worksheet. Zoom = 75;
```

## 步骤 4：保存更改并关闭文件

更改工作表缩放系数后，我们使用以下命令将更改保存到 Excel 文件中：`Save`的方法`Workbook`目的。然后我们关闭文件流以释放所有使用的资源。

```csharp
workbook.Save(dataDir + "output.xls");
fstream.Close();
```

### 使用 Aspose.Cells for .NET 控制工作表缩放系数的示例源代码 

```csharp
//文档目录的路径。
string dataDir = "YOUR DOCUMENT DIRECTORY";
//创建包含要打开的 Excel 文件的文件流
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
//实例化 Workbook 对象
//通过文件流打开Excel文件
Workbook workbook = new Workbook(fstream);
//访问 Excel 文件中的第一个工作表
Worksheet worksheet = workbook.Worksheets[0];
//将工作表的缩放系数设置为 75
worksheet.Zoom = 75;
//保存修改后的Excel文件
workbook.Save(dataDir + "output.xls");
//关闭文件流以释放所有资源
fstream.Close();
```

## 结论

本分步指南向您展示了如何使用 Aspose.Cells for .NET 控制工作表的缩放系数。使用提供的 C# 源代码，您可以轻松调整 .NET 应用程序中工作表的缩放系数。

### 常见问题 (FAQ)

#### 什么是 Aspose.Cells for .NET？

Aspose.Cells for .NET 是一个功能丰富的归档库，用于在 .NET 应用程序中操作 Excel 文件。

#### 如何安装 Aspose.Cells for .NET？

要安装Aspose.Cells for .NET，您需要从以下位置下载相应的NuGet包[Aspose 发布](https://releases/aspose.com/cells/net/)并将其添加到您的 .NET 项目中。

#### Aspose.Cells for .NET 提供哪些功能？

Aspose.Cells for .NET 提供了 Excel 文件的创建、编辑、转换和高级操作等功能。

#### Aspose.Cells for .NET 支持哪些文件格式？

Aspose.Cells for .NET 支持多种文件格式，包括 XLSX、XLSM、CSV、HTML、PDF 等。
