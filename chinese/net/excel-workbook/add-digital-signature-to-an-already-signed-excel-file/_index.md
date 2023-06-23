---
title: 将数字签名添加到已签名的 Excel 文件
linktitle: 将数字签名添加到已签名的 Excel 文件
second_title: Aspose.Cells for .NET API 参考
description: 使用 Aspose.Cells for .NET 轻松将数字签名添加到现有 Excel 文件。
type: docs
weight: 30
url: /zh/net/excel-workbook/add-digital-signature-to-an-already-signed-excel-file/
---
在本分步指南中，我们将解释提供的 C# 源代码，该源代码允许您使用 Aspose.Cells for .NET 将数字签名添加到已签名的 Excel 文件中。按照以下步骤向现有 Excel 文件添加新的数字签名。

## 第 1 步：设置源目录和输出目录

```csharp
//源目录
string sourceDir = RunExamples.Get_SourceDirectory();

//输出目录
string outputDir = RunExamples.Get_OutputDirectory();
```

在第一步中，我们定义将用于加载现有 Excel 文件并使用新数字签名保存文件的源目录和输出目录。

## 第 2 步：加载现有 Excel 文件

```csharp
//加载已签名的 Excel 工作簿
Aspose.Cells.Workbook workbook = new Aspose.Cells.Workbook(sourceDir + "sampleDigitallySignedByCells.xlsx");
```

这里我们使用以下命令加载已经签名的 Excel 文件`Workbook`Aspose.Cells 类。

## 步骤 3：创建数字签名集合

```csharp
//创建数字签名集合
Aspose.Cells.DigitalSignatures.DigitalSignatureCollection dsCollection = new Aspose.Cells.DigitalSignatures.DigitalSignatureCollection();
```

我们使用以下方法创建了一个新的数字签名集合`DigitalSignatureCollection`班级。

## 第 4 步：创建新证书

```csharp
//创建新证书
System.Security.Cryptography.X509Certificates.X509Certificate2 certificate = new System.Security.Cryptography.X509Certificates.X509Certificate2(certFileName, password);
```

在这里，我们根据提供的文件和密码创建一个新证书。

## 步骤 5：将新的数字签名添加到集合中

```csharp
//创建新的数字签名
Aspose.Cells.DigitalSignatures.DigitalSignature signature = new Aspose.Cells.DigitalSignatures.DigitalSignature(certificate, "Aspose.Cells added a new digital signature to the already signed workbook.", DateTime.Now);

//将数字签名添加到集合中
dsCollection.Add(signature);
```

我们使用以下方法创建一个新的数字签名`DigitalSignature`类并将其添加到数字签名集合中。

## 步骤 6：将数字签名集合添加到工作簿中

```csharp
//将数字签名集合添加到工作簿中
workbook.AddDigitalSignature(dsCollection);
```

我们使用以下命令将数字签名集合添加到现有 Excel 工作簿中`AddDigitalSignature()`方法。

## 步骤 7：保存并关闭工作簿

```csharp
//保存工作簿并关闭它
workbook.Save(outputDir + "outputDigitallySignedByCells.xlsx");
workbook.Dispose();
```

我们将带有新数字签名的工作簿保存到指定的输出目录，然后关闭它并释放关联的资源。

### 使用 Aspose.Cells for .NET 将数字签名添加到已签名的 Excel 文件的示例源代码 
```csharp
//源码目录
string sourceDir = RunExamples.Get_SourceDirectory();
//输出目录
string outputDir = RunExamples.Get_OutputDirectory();
//证书文件及其密码
string certFileName = sourceDir + "AsposeDemo.pfx";
string password = "aspose";
//加载已经数字签名的工作簿以添加新的数字签名
Aspose.Cells.Workbook workbook = new Aspose.Cells.Workbook(sourceDir + "sampleDigitallySignedByCells.xlsx");
//创建数字签名集合
Aspose.Cells.DigitalSignatures.DigitalSignatureCollection dsCollection = new Aspose.Cells.DigitalSignatures.DigitalSignatureCollection();
//创建新证书
System.Security.Cryptography.X509Certificates.X509Certificate2 certificate = new System.Security.Cryptography.X509Certificates.X509Certificate2(certFileName, password);
//创建新的数字签名并将其添加到数字签名集合中
Aspose.Cells.DigitalSignatures.DigitalSignature signature = new Aspose.Cells.DigitalSignatures.DigitalSignature(certificate, "Aspose.Cells added new digital signature in existing digitally signed workbook.", DateTime.Now);
dsCollection.Add(signature);
//在工作簿中添加数字签名集合
workbook.AddDigitalSignature(dsCollection);
//保存工作簿并将其丢弃。
workbook.Save(outputDir + "outputDigitallySignedByCells.xlsx");
workbook.Dispose();
Console.WriteLine("AddDigitalSignatureToAnAlreadySignedExcelFile executed successfully.\r\n");
```

## 结论

恭喜！您现在已经了解了如何使用 Aspose.Cells for .NET 将数字签名添加到已签名的 Excel 文件中。数字签名为您的 Excel 文件添加了额外的安全层，确保其真实性和完整性。

### 常见问题解答

#### 问：什么是 Aspose.Cells for .NET？

答：Aspose.Cells for .NET 是一个功能强大的类库，允许.NET 开发人员轻松创建、修改、转换和操作 Excel 文件。

#### 问：什么是 Excel 文件中的数字签名？

答：Excel文件中的数字签名是保证文档真实性、完整性和来源的电子标记。它用于验证文件自签名以来未被修改过并且来自可靠的来源。

#### 问：向 Excel 文件添加数字签名有什么好处？

答：向 Excel 文件添加数字签名有多种好处，包括防止未经授权的更改、确保数据完整性、验证文档作者的身份以及提供对其所包含信息的信心。

#### 问：我可以在 Excel 文件中添加多个数字签名吗？

答：是的，Aspose.Cells 允许您向 Excel 文件添加多个数字签名。您可以创建数字签名集合并通过一次操作将它们添加到文件中。

#### 问：Excel 文件添加数字签名有什么要求？

答：要向 Excel 文件添加数字签名，您需要一个有效的数字证书来签署文档。在添加数字签名之前，请确保您拥有正确的证书和密码。