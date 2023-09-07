---
title: 删除工作表的现有打印机设置
linktitle: 删除工作表的现有打印机设置
second_title: Aspose.Cells for .NET API 参考
description: 了解如何使用 Aspose.Cells for .NET 从 Excel 电子表格中删除现有打印机设置。
type: docs
weight: 80
url: /zh/net/excel-page-setup/remove-existing-printer-settings-of-worksheets/
---
在本教程中，我们将逐步引导您了解如何使用 Aspose.Cells for .NET 从 Excel 工作表中删除现有打印机设置。我们将使用 C# 源代码来说明该过程。

## 第一步：搭建环境

确保您的计算机上安装了 Aspose.Cells for .NET。还可以在您首选的开发环境中创建一个新项目。

## 第二步：导入必要的库

在您的代码文件中，导入使用 Aspose.Cells 所需的库。这是相应的代码：

```csharp
using Aspose.Cells;
```

## 步骤 3：设置源目录和输出目录

分别设置原始 Excel 文件所在的源目录和输出目录以及要保存修改后的文件的位置。使用以下代码：

```csharp
string sourceDir = "SOURCE DIRECTORY PATH";
string outputDir = "OUTPUT DIRECTORY PATH";
```

请务必指定完整目录路径。

## 第 4 步：加载源 Excel 文件

使用以下代码加载源 Excel 文件：

```csharp
Workbook wb = new Workbook(sourceDir + "fileName.xlsx");
```

这会将指定的 Excel 文件加载到 Workbook 对象中。

## 第 5 步：浏览工作表

使用循环遍历工作簿中的所有工作表。使用以下代码：

```csharp
int sheetCount = wb. Worksheets. Count;

for (int i = 0; i < sheetCount; i++)
{
     Worksheet ws = wb.Worksheets[i];
     //其余代码将在下一步中添加。
}
```

## 步骤 6：删除现有打印机设置

检查每个工作表是否存在打印机设置，并在必要时将其删除。使用以下代码：

```csharp
PageSetup ps = ws.PageSetup;

if (ps.PrinterSettings != null)
{
     Console.WriteLine("Printer settings for this spreadsheet exist.");
     Console.WriteLine("Sheet name: " + ws.Name);
     Console.WriteLine("Paper size: " + ps.PaperSize);

     ps.PrinterSettings = null;

     Console.WriteLine("Printer settings for this spreadsheet have been removed by setting them to null.");
     Console.WriteLine("");
}
```

## 步骤7：保存修改后的工作簿

使用以下代码保存修改后的工作簿：

```csharp
wb.Save(outputDir + "modifiedFilename.xlsx");
```

这会将修改后的工作簿保存到指定的输出目录。

### 使用 Aspose.Cells for .NET 删除工作表的现有打印机设置的示例源代码 
```csharp
//源码目录
string sourceDir = RunExamples.Get_SourceDirectory();
//输出目录
string outputDir = RunExamples.Get_OutputDirectory();
//加载源 Excel 文件
Workbook wb = new Workbook(sourceDir + "sampleRemoveExistingPrinterSettingsOfWorksheets.xlsx");
//获取工作簿的页数
int sheetCount = wb.Worksheets.Count;
//迭代所有工作表
for (int i = 0; i < sheetCount; i++)
{
    //访问第 i 个工作表
    Worksheet ws = wb.Worksheets[i];
    //访问工作表页面设置
    PageSetup ps = ws.PageSetup;
    //检查此工作表的打印机设置是否存在
    if (ps.PrinterSettings != null)
    {
        //打印以下消息
        Console.WriteLine("PrinterSettings of this worksheet exist.");
        //打印纸张名称及其纸张尺寸
        Console.WriteLine("Sheet Name: " + ws.Name);
        Console.WriteLine("Paper Size: " + ps.PaperSize);
        //通过将打印机设置设置为空来删除它们
        ps.PrinterSettings = null;
        Console.WriteLine("Printer settings of this worksheet are now removed by setting it null.");
        Console.WriteLine("");
    }//如果
}//为了
//保存工作簿
wb.Save(outputDir + "outputRemoveExistingPrinterSettingsOfWorksheets.xlsx");
```

## 结论

您现在已经了解了如何使用 Aspose.Cells for .NET 从 Excel 中的工作表中删除现有打印机设置。本教程将引导您完成该过程的每一步，从设置环境到浏览电子表格和清除打印机设置。您现在可以使用这些知识来管理 Excel 文件中的打印机设置。

### 常见问题解答

#### 问题 1：我如何知道电子表格是否有现有的打印机设置？

 A1：您可以通过访问工作表来检查工作表是否存在打印机设置`PrinterSettings`的财产`PageSetup`目的。如果该值非空，则表示存在现有的打印机设置。

#### 问题 2：我可以仅删除特定电子表格的打印机设置吗？

 A2：是的，您可以使用相同的方法通过访问特定工作表的打印机设置来删除该工作表的打印机设置。`PageSetup`目的。

#### Q3：此方法是否也会删除其他布局设置？

A3：不，此方法仅删除打印机设置。其他布局设置，例如边距、纸张方向等保持不变。

#### 问题 4：此方法是否适用于所有 Excel 文件格式，例如 .xls 和 .xlsx？

A4：是的，此方法适用于 Aspose.Cells 支持的所有 Excel 文件格式，包括 .xls 和 .xlsx。

#### 问题 5：对打印机设置所做的更改会永久保留在编辑的 Excel 文件中吗？

A5：是的，对打印机设置的更改会永久保存在编辑的 Excel 文件中。