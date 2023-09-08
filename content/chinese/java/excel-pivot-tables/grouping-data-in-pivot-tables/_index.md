---
title: 对数据透视表中的数据进行分组
linktitle: 对数据透视表中的数据进行分组
second_title: Aspose.Cells Java Excel 处理 API
description: 了解如何使用 Aspose.Cells for Java 在 Excel 中创建数据透视表。使用源代码示例自动进行数据分组和分析。
type: docs
weight: 14
url: /zh/java/excel-pivot-tables/grouping-data-in-pivot-tables/
---

数据透视表是用于分析和汇总电子表格中的数据的强大工具。它们允许您对数据进行分组和分类以获得有价值的见解。在本文中，我们将探讨如何使用 Aspose.Cells for Java 以及源代码示例有效地对数据透视表中的数据进行分组。

## 介绍

数据透视表提供了一种灵活的方式来组织和汇总大型数据集中的数据。它们允许您通过将数据分组为类别或层次结构来创建数据的自定义视图。这可以帮助您更轻松地识别数据中的趋势、模式和异常值。

## 第 1 步：创建数据透视表

让我们首先使用 Aspose.Cells for Java 创建一个数据透视表。下面是如何从示例 Excel 文件创建数据透视表的示例。

```java
//加载 Excel 文件
Workbook workbook = new Workbook("sample.xlsx");

//访问包含数据的工作表
Worksheet worksheet = workbook.getWorksheets().get(0);

//指定数据范围
CellArea sourceData = new CellArea();
sourceData.startRow = 0;
sourceData.endRow = 19; //假设有20行数据
sourceData.startColumn = 0;
sourceData.endColumn = 3; //假设有4列数据

//根据数据范围创建数据透视表
int index = worksheet.getPivotTables().add(sourceData, "A1", "PivotTable1");

//通过索引获取数据透视表
PivotTable pivotTable = worksheet.getPivotTables().get(index);

//将字段添加到行和列
pivotTable.addFieldToArea("Product", PivotFieldType.ROW);
pivotTable.addFieldToArea("Region", PivotFieldType.COLUMN);

//添加值并应用聚合
pivotTable.addFieldToArea("Sales", PivotFieldType.DATA);
pivotTable.getDataFields().get(0).setFunction(PivotFieldFunction.SUM);

//保存修改后的Excel文件
workbook.save("output.xlsx");
```

## 第 2 步：对数据进行分组

在 Aspose.Cells for Java 中，您可以使用以下方法对数据透视表中的数据进行分组：`PivotField`班级。以下是如何对数据透视表中的字段进行分组的示例：

```java
//访问数据透视表中的“产品”字段
PivotField productField = pivotTable.getPivotFields().get("Product");

//按特定标准对“产品”字段进行分组，例如按起始字母
productField.setIsAutoSubtotals(false);
productField.setBaseField("Product");
productField.setAutoSort(true);
productField.setAutoShow(true);

//将修改后的 Excel 文件与分组数据一起保存
workbook.save("output_grouped.xlsx");
```

## 第 3 步：自定义分组

您可以进一步自定义分组设置，例如指定基于日期的分组间隔或自定义分组规则。以下是自定义基于日期的分组的示例：

```java
//访问数据透视表中的“日期”字段（假设它是日期字段）
PivotField dateField = pivotTable.getPivotFields().get("Date");

//按月份对日期进行分组
dateField.setIsAutoSubtotals(false);
dateField.setIsDateGroup(true);
dateField.setDateGroupingType(PivotFieldDateGroupingType.MONTHS);

//使用自定义日期分组保存修改后的 Excel 文件
workbook.save("output_custom_grouping.xlsx");
```

## 结论

在数据透视表中对数据进行分组是在 Excel 中分析和汇总数据的一项宝贵技术，而 Aspose.Cells for Java 可以轻松实现此过程的自动化。通过提供的源代码示例，您可以创建数据透视表、自定义分组并高效地从数据中获取见解。

## 常见问题解答

### 1. Excel 中数据透视表的用途是什么？

Excel 中的数据透视表用于汇总和分析大型数据集。它们允许您创建数据的自定义视图，从而更轻松地识别模式和趋势。

### 2. 如何自定义数据透视表中的数据分组？

您可以使用以下命令自定义数据透视表中的数据分组`PivotField`Aspose.Cells for Java 中的类。这允许您指定分组标准，例如基于日期的间隔或自定义规则。

### 3. 我可以使用 Aspose.Cells for Java 自动创建数据透视表吗？

是的，您可以使用 Aspose.Cells for Java 在 Excel 中自动创建数据透视表，如提供的源代码示例中所示。