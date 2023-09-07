---
title: 创建共享工作簿
linktitle: 创建共享工作簿
second_title: Aspose.Cells for .NET API 参考
description: 使用 Aspose.Cells for .NET 创建 Excel 共享工作簿以实现并发数据协作。
type: docs
weight: 70
url: /zh/net/excel-workbook/create-shared-workbook/
---
在本教程中，我们将引导您完成所提供的 C# 源代码，该代码将允许您使用 Aspose.Cells for .NET 创建共享工作簿。请按照以下步骤执行此操作。

## 第1步：设置输出目录

```csharp
//输出目录
string outputDir = RunExamples.Get_OutputDirectory();
```

在第一步中，我们定义将保存共享工作簿的输出目录。

## 第 2 步：创建工作簿对象

```csharp
//创建工作簿对象
Workbook wb = new Workbook();
```

我们正在创建一个新的 Workbook 对象来代表我们的 Excel 工作簿。

## 步骤 3：启用工作簿共享

```csharp
//分享工作簿
wb.Settings.Shared = true;
```

我们通过设置来启用工作簿的共享功能`Shared`Workbook 对象的属性`true`.

## 步骤 4：保存共享工作簿

```csharp
//保存共享工作簿
wb.Save(outputDir + "outputSharedWorkbook.xlsx");
```

我们通过指定输出文件的路径和名称来保存共享工作簿。

### 使用 Aspose.Cells for .NET 创建共享工作簿的示例源代码 
```csharp
//输出目录
string outputDir = RunExamples.Get_OutputDirectory();
//创建工作簿对象
Workbook wb = new Workbook();
//分享工作簿
wb.Settings.Shared = true;
//保存共享工作簿
wb.Save(outputDir + "outputSharedWorkbook.xlsx");
Console.WriteLine("CreateSharedWorkbook executed successfully.\r\n");
```

## 结论

恭喜！您学习了如何使用 Aspose.Cells for .NET 创建共享工作簿。多个用户可以同时使用共享工作簿来协作处理数据。使用您自己的数据进行实验并进一步探索 Aspose.Cells 的功能，以创建强大且个性化的 Excel 工作簿。

### 常见问题解答

#### 问：什么是共享工作簿？

答：共享工作簿是可供多个用户同时使用以协作处理数据的 Excel 工作簿。每个用户都可以对工作簿进行更改，其他用户将实时看到更新。

#### 问：如何在 Aspose.Cells for .NET 中启用工作簿共享？

答：要在 Aspose.Cells for .NET 中启用工作簿共享，您必须设置`Shared`Workbook 对象的属性`true`。这将允许用户同时处理工作簿。

#### 问：我可以限制共享工作簿中的用户权限吗？

答：是的，您可以使用 Excel 的安全功能限制共享工作簿中的用户权限。您可以为每个用户设置特定的权限，例如编辑、只读等。

#### 问：如何与其他用户共享工作簿？

答：创建共享工作簿后，您可以通过向其他用户发送 Excel 文件来与他们共享。其他用户将能够打开该文件并同时对其进行处理。

#### 问：共享工作簿是否支持所有 Excel 功能？

答：共享工作簿支持大多数 Excel 功能。但是，某些高级功能（例如宏和加载项）在共享工作簿中使用时可能有限制或限制。