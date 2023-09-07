---
title: Xades 签名支持
linktitle: Xades 签名支持
second_title: Aspose.Cells for .NET API 参考
description: 了解如何使用 Aspose.Cells for .NET 将 Xades 签名添加到 Excel 文件。
type: docs
weight: 190
url: /zh/net/excel-workbook/xades-signature-support/
---
在本文中，我们将带您一步步解释下面的 C# 源代码，该源代码是关于使用 Aspose.Cells 库用于 .NET 的 Xades 签名支持。您将了解如何使用此库将 Xades 数字签名添加到 Excel 文件。我们还将向您提供签名流程及其执行的概述。请按照以下步骤获取结论性结果。

## 第 1 步：定义源目录和输出目录
首先，我们需要在代码中定义源目录和输出目录。这些目录指示源文件所在的位置以及输出文件的保存位置。这是相应的代码：

```csharp
//源码目录
string sourceDir = RunExamples.Get_SourceDirectory();
//输出目录
string outputDir = RunExamples.Get_OutputDirectory();
```

请务必根据需要调整目录路径。

## 第 2 步：加载 Excel 工作簿
下一步是加载我们要添加 Xades 数字签名的 Excel 工作簿。这是加载工作簿的代码：

```csharp
Workbook workbook = new Workbook(sourceDir + "sourceFile.xlsx");
```

确保在代码中正确指定源文件名。

## 步骤3：配置数字签名
现在我们将通过提供必要的信息来配置 Xades 数字签名。我们必须指定包含数字证书的 PFX 文件以及关联的密码。这是相应的代码：

```csharp
string password = "pfxPassword";
string pfx = "pfxFile";
DigitalSignature signature = new DigitalSignature(File.ReadAllBytes(pfx), password, "testXAdES", DateTime.Now);
signature.XAdESType = XAdESType.XAdES;
```

请务必将“pfxPassword”替换为您的实际密码，将“pfxFile”替换为 PFX 文件的路径。

## 第四步：添加数字签名
现在我们已经配置了数字签名，我们可以将其添加到 Excel 工作簿中。这是相应的代码：

```csharp
DigitalSignatureCollection dsCollection = new DigitalSignatureCollection();
dsCollection.Add(signature);
workbook.SetDigitalSignature(dsCollection);
```

此步骤将 Xades 数字签名添加到 Excel 工作簿。

## 步骤 5：保存带有签名的工作簿
最后，我们保存添加了数字签名的 Excel 工作簿。这是相应的代码：

```csharp
workbook.Save(outputDir + "XAdESSignatureSupport_out.xlsx");
```

确保根据您的需要调整输出文件的名称。

### 使用 Aspose.Cells for .NET 的 Xades 签名支持示例源代码 
```csharp
//源码目录
string sourceDir = RunExamples.Get_SourceDirectory();
//输出目录
string outputDir = RunExamples.Get_OutputDirectory();
Workbook workbook = new Workbook(sourceDir + "sourceFile.xlsx");
string password = "pfxPassword";
string pfx = "pfxFile";
DigitalSignature signature = new DigitalSignature(File.ReadAllBytes(pfx), password, "testXAdES", DateTime.Now);
signature.XAdESType = XAdESType.XAdES;
DigitalSignatureCollection dsCollection = new DigitalSignatureCollection();
dsCollection.Add(signature);
workbook.SetDigitalSignature(dsCollection);
workbook.Save(outputDir + "XAdESSignatureSupport_out.xlsx");
Console.WriteLine("XAdESSignatureSupport executed successfully.");
```

## 结论
恭喜！您已了解如何使用适用于 .NET 的 Aspose.Cells 库将 Xades 数字签名添加到 Excel 文件。通过遵循本文中提供的步骤，您将能够在自己的项目中实现此功能。请随意尝试更多该库并发现它提供的其他强大功能。

### 常见问题解答

#### 问：Xades 是什么？

答：Xades 是一种先进的电子签名标准，用于确保数字文档的完整性和真实性。

#### 问：我可以在 Aspose.Cells 中使用其他类型的数字签名吗？

答：是的，Aspose.Cells 还支持其他类型的数字签名，例如 XMLDSig 签名和 PKCS#7 签名。

#### 问：我可以将签名应用到 Excel 文件以外的其他文件类型吗？
 
答：是的，Aspose.Cells 还允许将数字签名应用于其他支持的文件类型，例如 Word、PDF 和 PowerPoint 文件。