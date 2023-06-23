---
title: 调整压缩级别
linktitle: 调整压缩级别
second_title: Aspose.Cells for .NET API 参考
description: 通过使用 Aspose.Cells for .NET 调整压缩级别来减小 Excel 工作簿的大小。
type: docs
weight: 50
url: /zh/net/excel-workbook/adjust-compression-level/
---
在本分步教程中，我们将解释提供的 C# 源代码，它允许您使用 Aspose.Cells for .NET 调整压缩级别。请按照以下步骤调整 Excel 工作簿中的压缩级别。

## 第 1 步：设置源目录和输出目录

```csharp
//源目录
string sourceDir = RunExamples.Get_SourceDirectory();
//输出目录
string outDir = RunExamples.Get_OutputDirectory();
```

在第一步中，我们定义 Excel 文件的源目录和输出目录。

## 第 2 步：加载 Excel 工作簿

```csharp
//加载 Excel 工作簿
Workbook workbook = new Workbook(sourceDir + "LargeSampleFile.xlsx");
```

我们使用以下命令从指定文件加载 Excel 工作簿`Workbook`来自 Aspose.Cells 的类。

## 第 3 步：设置备份选项

```csharp
//定义备份选项
XlsbSaveOptions options = new XlsbSaveOptions();
```

我们创建一个实例`XlsbSaveOptions`类设置保存选项。

## 步骤 4：调整压缩级别（级别 1）

```csharp
//调整压缩级别（级别 1）
options.CompressionType = OoxmlCompressionType.Level1;
var watch = System.Diagnostics.Stopwatch.StartNew();
workbook.Save(outDir + "LargeSampleFile_level_1_out.xlsb", options);
watch.Stop();
let elapsedMs = watch.ElapsedMilliseconds;
Console.WriteLine("Elapsed time (Level 1): " + elapsedMs);
```

我们通过设置来调整压缩级别`CompressionType`到`Level1`。然后，我们保存指定此压缩选项的 Excel 工作簿。

## 步骤 5：调整压缩级别（级别 6）

```csharp
//调整压缩级别（级别 6）
options.CompressionType = OoxmlCompressionType.Level6;
watch = System.Diagnostics.Stopwatch.StartNew();
workbook.Save(outDir + "LargeSampleFile_level_6_out.xlsb", options);
watch.Stop();
elapsedMs = watch. ElapsedMilliseconds;
Console.WriteLine("Elapsed time (Level 6): " + elapsedMs);
```

我们重复该过程以将压缩级别调整为`Level6`并使用此选项保存 Excel 工作簿。

## 第 6 步：调整压缩级别（级别 9）

```csharp
//调整压缩级别（9级）
options.CompressionType = OoxmlCompressionType.Level9;
watch = System.Diagnostics.Stopwatch.StartNew();
workbook.Save(outDir + "LargeSampleFile_level_9_out.xlsb", options);
watch.Stop();
elapsedMs = watch. ElapsedMilliseconds;
Console.WriteLine("Elapsed time (Level 9): " + elapsedMs);
```

我们最后一次重复该过程，将压缩级别调整为`Level9`并使用此选项保存 Excel 工作簿。

### 使用 Aspose.Cells for .NET 调整压缩级别的示例源代码 
```csharp
//源码目录
string sourceDir = RunExamples.Get_SourceDirectory();
string outDir = RunExamples.Get_OutputDirectory();
Workbook workbook = new Workbook(sourceDir + "LargeSampleFile.xlsx");
XlsbSaveOptions options = new XlsbSaveOptions();
options.CompressionType = OoxmlCompressionType.Level1;
var watch = System.Diagnostics.Stopwatch.StartNew();
workbook.Save(outDir + "LargeSampleFile_level_1_out.xlsb", options);
watch.Stop();
var elapsedMs = watch.ElapsedMilliseconds;
Console.WriteLine("Level 1 Elapsed Time: " + elapsedMs);
watch = System.Diagnostics.Stopwatch.StartNew();
options.CompressionType = OoxmlCompressionType.Level6;
workbook.Save(outDir + "LargeSampleFile_level_6_out.xlsb", options);
watch.Stop();
elapsedMs = watch.ElapsedMilliseconds;
Console.WriteLine("Level 6 Elapsed Time: " + elapsedMs);
watch = System.Diagnostics.Stopwatch.StartNew();
options.CompressionType = OoxmlCompressionType.Level9;
workbook.Save(outDir + "LargeSampleFile_level_9_out.xlsb", options);
watch.Stop();
elapsedMs = watch.ElapsedMilliseconds;
Console.WriteLine("Level 9 Elapsed Time: " + elapsedMs);
Console.WriteLine("AdjustCompressionLevel executed successfully.");
```

## 结论

恭喜！您学习了如何使用 Aspose.Cells for .NET 调整 Excel 工作簿中的压缩级别。尝试不同的压缩级别，找到最适合您需求的压缩级别。

### 常见问题解答

#### 问：Excel 工作簿中的压缩是什么？

答：Excel 工作簿中的压缩是使用压缩算法减小文件大小的过程。这减少了加载和操作文件时所需的存储空间并提高了性能。

#### 问：Aspose.Cells 提供什么级别的压缩？

答：使用Aspose.Cells，您可以将压缩级别从1调整到9。压缩级别越高，文件大小越小，但也会增加处理时间。

#### 问：如何为 Excel 工作簿选择正确的压缩级别？

答：压缩级别的选择取决于您的具体需求。如果您想要最大压缩并且处理时间不是问题，则可以选择级别 9。如果您希望在文件大小和处理时间之间进行折衷，则可以选择中间级别。

#### 问：压缩会影响 Excel 工作簿中的数据质量吗？

答：不会，压缩不会影响 Excel 工作簿中的数据质量。它只是使用压缩技术减小文件大小，而不改变数据本身。

#### 问：保存 Excel 文件后可以调整压缩级别吗？

答：不可以，一旦您以特定的压缩级别保存 Excel 文件，以后就无法调整压缩级别。如果您想修改文件，则需要使用新的压缩级别再次保存该文件。