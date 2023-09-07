---
title: 访问 Web 扩展信息
linktitle: 访问 Web 扩展信息
second_title: Aspose.Cells for .NET API 参考
description: 使用 Aspose.Cells for .NET 访问 Web 扩展信息。
type: docs
weight: 10
url: /zh/net/excel-workbook/access-web-extension-information/
---
使用 Aspose.Cells for .NET 开发应用程序时，访问 Web 扩展信息是一项重要功能。在本分步指南中，我们将解释提供的 C# 源代码，该源代码将允许您使用 Aspose.Cells for .NET 访问 Web 扩展信息。我们还将以 Markdown 格式为您提供结论和答案，以使其更易于理解。请按照以下步骤获取有关 Web 扩展的有价值的信息。

## 第1步：设置源目录

```csharp
//源目录
string sourceDir = RunExamples.Get_SourceDirectory();
```

在第一步中，我们定义将用于加载包含 Web 扩展信息的 Excel 文件的源目录。

## 第 2 步：加载 Excel 文件

```csharp
//加载示例 Excel 文件
Workbook workbook = new Workbook(sourceDir + "WebExtensionsSample.xlsx");
```

这里我们加载示例 Excel 文件，其中包含我们要检索的 Web 扩展信息。

## 步骤 3：从 Web 扩展任务窗口访问信息

```csharp
WebExtensionTaskPaneCollection taskPanes = workbook.Worksheets.WebExtensionTaskPanes;
foreach(WebExtensionTaskPane taskPane in taskPanes)
{
Console.WriteLine("Width: " + taskPane.Width);
Console.WriteLine("Is visible: " + taskPane.IsVisible);
Console.WriteLine("Is locked: " + taskPane.IsLocked);
Console.WriteLine("Docking State: " + taskPane.DockState);
Console.WriteLine("Store Name: " + taskPane.WebExtension.Reference.StoreName);
Console.WriteLine("Store type: " + taskPane.WebExtension.Reference.StoreType);
Console.WriteLine("Web Extension ID: " + taskPane.WebExtension.Id);
}
```

在此步骤中，我们访问 Excel 文件中存在的每个 Web 扩展任务窗口的信息。我们显示不同的属性，例如宽度、可见性、锁定状态、主状态、商店名称、商店类型和 Web 扩展 ID。

## 第四步：显示成功信息

```csharp
Console.WriteLine("AccessWebExtensionInformation executed successfully.");
```

最后，我们会显示一条消息，表明 Web 扩展信息已成功访问。

### 使用 Aspose.Cells for .NET 访问 Web 扩展信息的示例源代码 
```csharp
//源码目录
string sourceDir = RunExamples.Get_SourceDirectory();
//加载示例 Excel 文件
Workbook workbook = new Workbook(sourceDir + "WebExtensionsSample.xlsx");
WebExtensionTaskPaneCollection taskPanes = workbook.Worksheets.WebExtensionTaskPanes;
foreach (WebExtensionTaskPane taskPane in taskPanes)
{
	Console.WriteLine("Width: " + taskPane.Width);
	Console.WriteLine("IsVisible: " + taskPane.IsVisible);
	Console.WriteLine("IsLocked: " + taskPane.IsLocked);
	Console.WriteLine("DockState: " + taskPane.DockState);
	Console.WriteLine("StoreName: " + taskPane.WebExtension.Reference.StoreName);
	Console.WriteLine("StoreType: " + taskPane.WebExtension.Reference.StoreType);
	Console.WriteLine("WebExtension.Id: " + taskPane.WebExtension.Id);
}
Console.WriteLine("AccessWebExtensionInformation executed successfully.");
```

## 结论

在本教程中，我们学习了如何使用 Aspose.Cells for .NET 访问 Web 扩展信息。通过按照提供的步骤操作，您将能够轻松地将任务窗口信息从 Web 扩展提取到 Excel 文件中。


### 常见问题解答

#### 问：什么是 Aspose.Cells for .NET？

答：Aspose.Cells for .NET 是一个功能强大的类库，允许.NET 开发人员轻松创建、修改、转换和操作 Excel 文件。

#### 问：Aspose.Cells 支持其他编程语言吗？

答：是的，Aspose.Cells 支持多种编程语言，如 C#、VB.NET、Java、PHP、Python 等。

#### 问：我可以在商业项目中使用 Aspose.Cells 吗？

A：是的，Aspose.Cells是一个商业库，根据许可协议可以在商业项目中使用。

#### 问：是否有关于 Aspose.Cells 的附加文档？

答：是的，您可以在 Aspose 官方网站上查看完整的 Aspose.Cells 文档，以获取更多信息和资源。