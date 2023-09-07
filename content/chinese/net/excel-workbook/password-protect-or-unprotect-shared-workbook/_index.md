---
title: 密码保护或取消保护共享工作簿
linktitle: 密码保护或取消保护共享工作簿
second_title: Aspose.Cells for .NET API 参考
description: 了解如何使用 Aspose.Cells for .NET 对共享工作簿进行密码保护或取消保护。
type: docs
weight: 120
url: /zh/net/excel-workbook/password-protect-or-unprotect-shared-workbook/
---
使用密码保护共享工作簿对于确保数据隐私非常重要。借助 Aspose.Cells for .NET，您可以使用密码轻松保护或取消保护共享工作簿。请按照以下步骤操作以获得所需的结果：

## 第1步：指定输出目录

首先，您需要指定保存受保护的 Excel 文件的输出目录。以下是使用 Aspose.Cells 执行此操作的方法：

```csharp
//输出目录
string outputDir = RunExamples.Get_OutputDirectory();
```

## 步骤 2：创建一个空的 Excel 文件

然后，您可以创建一个要对其应用保护或取消保护的空 Excel 文件。这是示例代码：

```csharp
//创建一个空的 Excel 工作簿
Workbook wb = new Workbook();
```

## 步骤 3：保护或取消保护共享工作簿

创建工作簿后，您可以通过指定适当的密码来保护或取消保护共享工作簿。就是这样：

```csharp
//使用密码保护共享工作簿
wb.ProtectSharedWorkbook("1234");

//取消注释此行以取消对共享工作簿的保护
//wb.UnprotectSharedWorkbook("1234");
```

## 步骤 4：保存输出 Excel 文件

应用保护或取消保护后，您可以将受保护的 Excel 文件保存到指定的输出目录。操作方法如下：

```csharp
//保存输出的 Excel 文件
wb.Save(outputDir + "outputProtectSharedWorkbook.xlsx");
Console.WriteLine("PasswordProtectOrUnprotectSharedWorkbook executed successfully.\r\n");
```

### 使用 Aspose.Cells for .NET 进行密码保护或取消保护共享工作簿的示例源代码 
```csharp
//输出目录
string outputDir = RunExamples.Get_OutputDirectory();
//创建空 Excel 文件
Workbook wb = new Workbook();
//使用密码保护共享工作簿
wb.ProtectSharedWorkbook("1234");
//取消注释此行以取消对共享工作簿的保护
//wb.UnprotectSharedWorkbook("1234");
//保存输出的 Excel 文件
wb.Save(outputDir + "outputProtectSharedWorkbook.xlsx");
Console.WriteLine("PasswordProtectOrUnprotectSharedWorkbook executed successfully.\r\n");
```

## 结论

使用密码保护或取消保护共享工作簿对于确保数据安全至关重要。使用 Aspose.Cells for .NET，您可以轻松地将此功能添加到您的 Excel 文件中。通过按照本指南中的步骤操作，您可以使用密码有效地保护或取消保护您的共享工作簿。尝试使用您自己的 Excel 文件，并确保维护敏感数据的安全。

### 常见问题解答

#### 问：我可以对与 Aspose.Cells 共享的工作簿应用哪些类型的保护？
    
答：使用Aspose.Cells，您可以通过指定密码来保护共享工作簿，以防止未经授权的访问、修改或删除数据。

#### 问：我可以在不指定密码的情况下保护共享工作簿吗？
    
答：是的，您无需指定密码即可保护共享工作簿。但是，建议使用强密码以获得更好的安全性。

#### 问：如何取消保护与 Aspose.Cells 共享的工作簿？
    
答：要取消对共享工作簿的保护，您必须指定与保护工作簿时使用的密码相同的密码。这样就可以解除保护并自由访问数据。

#### 问：保护共享工作簿是否会影响工作簿中的功能和公式？
    
答：当您保护共享工作簿时，用户仍然可以访问工作簿中的功能和公式。保护仅影响工作簿的结构更改。