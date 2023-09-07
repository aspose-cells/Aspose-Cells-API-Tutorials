---
title: 工作簿打印预览
linktitle: 工作簿打印预览
second_title: Aspose.Cells for .NET API 参考
description: 了解如何使用 Aspose.Cells for .NET 生成工作簿的打印预览。
type: docs
weight: 170
url: /zh/net/excel-workbook/workbook-print-preview/
---
使用 Aspose.Cells for .NET 处理 Excel 文件时，工作簿的打印预览是一项重要功能。您可以按照以下步骤轻松生成打印预览：

## 第1步：指定源目录

首先，您需要指定要预览的Excel文件所在的源目录。操作方法如下：

```csharp
//源目录
string sourceDir = RunExamples.Get_SourceDirectory();
```

## 第 2 步：加载工作簿

然后需要从指定的Excel文件加载Workbook工作簿。操作方法如下：

```csharp
//加载工作簿工作簿
Workbook workbook = new Workbook(sourceDir + "Book1.xlsx");
```

## 步骤 3：配置图像和打印选项

在生成打印预览之前，您可以根据需要配置图像和打印选项。在此示例中，我们使用默认选项。操作方法如下：

```csharp
//图像和打印选项
ImageOrPrintOptions imgOptions = new ImageOrPrintOptions();
```

## 步骤 4：生成工作簿的打印预览

现在您可以使用 WorkbookPrintingPreview 类生成 Workbook 工作簿的打印预览。操作方法如下：

```csharp
//工作簿的打印预览
WorkbookPrintingPreview preview = new WorkbookPrintingPreview(workbook, imgOptions);
Console.WriteLine("Workbook page count: " + preview.EvaluatedPageCount);
```

## 步骤 5：生成工作表的打印预览

如果要生成特定工作表的打印预览，可以使用 SheetPrintingPreview 类。这是一个例子：

```csharp
//工作表的打印预览
SheetPrintingPreview preview2 = new SheetPrintingPreview(workbook.Worksheets[0], imgOptions);
Console.WriteLine("Number of worksheet pages: " + preview2.EvaluatedPageCount);
```

### 使用 Aspose.Cells for .NET 的工作簿打印预览的示例源代码 
```csharp
//源码目录
string sourceDir = RunExamples.Get_SourceDirectory();
Workbook workbook = new Workbook(sourceDir + "Book1.xlsx");
ImageOrPrintOptions imgOptions = new ImageOrPrintOptions();
WorkbookPrintingPreview preview = new WorkbookPrintingPreview(workbook, imgOptions);
Console.WriteLine("Workbook page count: " + preview.EvaluatedPageCount);
SheetPrintingPreview preview2 = new SheetPrintingPreview(workbook.Worksheets[0], imgOptions);
Console.WriteLine("Worksheet page count: " + preview2.EvaluatedPageCount);
Console.WriteLine("PrintPreview executed successfully.");
```

## 结论

生成工作簿的打印预览是 Aspose.Cells for .NET 提供的一项强大功能。通过执行上面给出的步骤，您可以轻松预览 Excel 工作簿并获取有关要打印的页数的信息。

### 常见问题解答

#### 问：如何指定不同的源目录来加载我的工作簿？
    
答：您可以使用`Set_SourceDirectory`方法指定不同的源目录。例如：`RunExamples.Set_SourceDirectory("Path_to_the_source_directory")`.

#### 问：生成打印预览时可以自定义图像和打印选项吗？
    
答：是的，您可以通过更改图像和打印选项的属性来自定义图像和打印选项。`ImageOrPrintOptions`目的。例如，您可以设置图像分辨率、输出文件格式等。

#### 问：是否可以为工作簿中的多个工作表生成打印预览？
    
答：是的，您可以迭代工作簿中的不同工作表，并使用`SheetPrintingPreview`班级。

#### 问：如何将打印预览保存为图像或 PDF 文件？
    
答：你可以使用`ToImage`或者`ToPdf`的方法`WorkbookPrintingPreview`或者`SheetPrintingPreview`对象将打印预览保存为图像或 PDF 文件。

#### 问：打印预览生成后可以做什么？
    
答：生成打印预览后，您可以在屏幕上查看它，将其另存为图像或 PDF 文件，或将其用于其他操作，例如通过电子邮件发送或打印。
	