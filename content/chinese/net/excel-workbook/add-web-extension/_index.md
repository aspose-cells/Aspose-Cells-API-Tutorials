---
title: 添加网页扩展
linktitle: 添加网页扩展
second_title: Aspose.Cells for .NET API 参考
description: 使用 Aspose.Cells for .NET 轻松将 Web 扩展添加到您的 Excel 工作簿。
type: docs
weight: 40
url: /zh/net/excel-workbook/add-web-extension/
---
在本分步教程中，我们将解释提供的 C# 源代码，该源代码将允许您使用 Aspose.Cells for .NET 添加 Web 扩展。按照以下步骤将 Web 扩展添加到您的 Excel 工作簿。

## 第1步：设置输出目录

```csharp
//输出目录
string outDir = RunExamples.Get_OutputDirectory();
```

在第一步中，我们定义将保存修改后的 Excel 工作簿的输出目录。

## 第 2 步：创建新工作簿

```csharp
//创建新工作簿
Workbook workbook = new Workbook();
```

在这里，我们使用以下命令创建一个新的 Excel 工作簿`Workbook`来自 Aspose.Cells 的类。

## 第 3 步：访问 Web 扩展集合

```csharp
//访问 Web 扩展集合
WebExtensionCollection extensions = workbook.Worksheets.WebExtensions;
```

我们使用以下命令访问 Excel 工作簿的 Web 扩展集合`WebExtensions`的财产`Worksheets`目的。

## 第 4 步：添加新的 Web 扩展

```csharp
//添加新的网络扩展
int extensionIndex = extensions.Add();
WebExtension extension = extensions[extensionIndex];
extension.Reference.Id = "wa104379955";
extension.Reference.StoreName = "en-US";
extension.Reference.StoreType = WebExtensionStoreType.OMEX;
```

我们正在向扩展集合中添加一个新的 Web 扩展。我们定义扩展的参考 ID、商店名称和商店类型。

## 步骤 5：访问 Web 扩展任务窗格集合

```csharp
//访问 Web 扩展的任务窗格集合
WebExtensionTaskPaneCollection taskPanes = workbook.Worksheets.WebExtensionTaskPanes;
```

我们使用以下命令访问 Excel Workbook Web Extension 任务窗格集合`WebExtensionTaskPanes`的财产`Worksheets`目的。

## 步骤 6：添加新任务窗格

```csharp
//添加新任务窗格
int taskPaneIndex = taskPanes.Add();
WebExtensionTaskPane taskPane = taskPanes[taskPaneIndex];
taskPane. IsVisible = true;
taskPane. DockState = "right";
taskPane. WebExtension = extension;
```

我们正在向任务窗格集合添加一个新的任务窗格。我们设置窗格的可见性、其停靠状态以及关联的 Web 扩展。

## 步骤 7：保存并关闭工作簿

```csharp
//保存并关闭工作簿
workbook.Save(outDir + "AddWebExtension_Out.xlsx");
Console.WriteLine("AddWebExtension executed successfully.");
```

我们将修改后的工作簿保存到指定的输出目录，然后关闭它。

### 使用 Aspose.Cells for .NET 添加 Web 扩展的示例源代码 
```csharp
//源码目录
string outDir = RunExamples.Get_OutputDirectory();
Workbook workbook = new Workbook();
WebExtensionCollection extensions = workbook.Worksheets.WebExtensions;
WebExtensionTaskPaneCollection taskPanes = workbook.Worksheets.WebExtensionTaskPanes;
int extensionIndex = extensions.Add();
int taskPaneIndex = taskPanes.Add();
WebExtension extension = extensions[extensionIndex];
extension.Reference.Id = "wa104379955";
extension.Reference.StoreName = "en-US";
extension.Reference.StoreType = WebExtensionStoreType.OMEX;
WebExtensionTaskPane taskPane = taskPanes[taskPaneIndex];
taskPane.IsVisible = true;
taskPane.DockState = "right";
taskPane.WebExtension = extension;
workbook.Save(outDir + "AddWebExtension_Out.xlsx");
Console.WriteLine("AddWebExtension executed successfully.");
```

## 结论

恭喜！您现在已经了解了如何使用 Aspose.Cells for .NET 添加 Web 扩展。试验代码并探索 Aspose.Cells 的其他功能，以充分利用在 Excel 工作簿中操作 Web 扩展。

## 常见问题解答

#### 问：Excel 工作簿中的 Web 扩展是什么？

答：Excel 工作簿中的 Web 扩展是一个组件，允许您通过集成 Web 应用程序向 Excel 添加附加功能。它可以提供交互功能、自定义仪表板、外部集成等。

#### 问：如何使用 Aspose.Cells 将 Web 扩展添加到 Excel 工作簿？

答：要使用 Aspose.Cells 将 Web 扩展添加到 Excel 工作簿，您可以按照我们的分步指南中提供的步骤进行操作。使用`WebExtensionCollection`和`WebExtensionTaskPaneCollection`用于添加和配置 Web 扩展及关联任务窗格的类。

#### 问：添加 Web 扩展程序需要哪些信息？

答：添加 Web 扩展程序时，您必须提供扩展程序 SKU ID、商店名称和商店类型。此信息有助于正确识别和加载扩展。

#### 问：我可以向单个 Excel 工作簿添加多个 Web 扩展吗？

答：是的，您可以将多个 Web 扩展添加到单个 Excel 工作簿中。使用`Add`Web 扩展集合的方法来添加每个扩展，然后将它们与相应的任务窗格关联。