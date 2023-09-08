---
title: تجميع البيانات في الجداول المحورية
linktitle: تجميع البيانات في الجداول المحورية
second_title: Aspose.Cells واجهة برمجة تطبيقات معالجة Java Excel
description: تعرف على كيفية إنشاء جداول محورية في Excel باستخدام Aspose.Cells لـ Java. أتمتة تجميع البيانات وتحليلها باستخدام أمثلة التعليمات البرمجية المصدر.
type: docs
weight: 14
url: /ar/java/excel-pivot-tables/grouping-data-in-pivot-tables/
---

تعد الجداول المحورية أداة قوية لتحليل وتلخيص البيانات في جداول البيانات. إنها تسمح لك بتجميع البيانات وتصنيفها للحصول على رؤى قيمة. في هذه المقالة، سنستكشف كيفية تجميع البيانات بشكل فعال في الجداول المحورية باستخدام Aspose.Cells لـ Java، إلى جانب أمثلة التعليمات البرمجية المصدر.

## مقدمة

توفر الجداول المحورية طريقة مرنة لتنظيم وتلخيص البيانات من مجموعات البيانات الكبيرة. إنها تسمح لك بإنشاء طرق عرض مخصصة لبياناتك عن طريق تجميعها في فئات أو تسلسلات هرمية. يمكن أن يساعدك ذلك في تحديد الاتجاهات والأنماط والقيم المتطرفة في بياناتك بسهولة أكبر.

## الخطوة 1: إنشاء جدول محوري

لنبدأ بإنشاء جدول محوري باستخدام Aspose.Cells لـ Java. فيما يلي مثال لكيفية إنشاء جدول محوري من نموذج ملف Excel.

```java
// قم بتحميل ملف إكسل
Workbook workbook = new Workbook("sample.xlsx");

// الوصول إلى ورقة العمل التي تحتوي على البيانات
Worksheet worksheet = workbook.getWorksheets().get(0);

// تحديد نطاق البيانات
CellArea sourceData = new CellArea();
sourceData.startRow = 0;
sourceData.endRow = 19; // بافتراض 20 صفًا من البيانات
sourceData.startColumn = 0;
sourceData.endColumn = 3; // بافتراض 4 أعمدة من البيانات

// إنشاء جدول محوري بناءً على نطاق البيانات
int index = worksheet.getPivotTables().add(sourceData, "A1", "PivotTable1");

// الحصول على الجدول المحوري حسب الفهرس
PivotTable pivotTable = worksheet.getPivotTables().get(index);

// إضافة حقول إلى الصفوف والأعمدة
pivotTable.addFieldToArea("Product", PivotFieldType.ROW);
pivotTable.addFieldToArea("Region", PivotFieldType.COLUMN);

// إضافة القيم وتطبيق التجميع
pivotTable.addFieldToArea("Sales", PivotFieldType.DATA);
pivotTable.getDataFields().get(0).setFunction(PivotFieldFunction.SUM);

// احفظ ملف Excel المعدل
workbook.save("output.xlsx");
```

## الخطوة 2: بيانات المجموعة

 في Aspose.Cells for Java، يمكنك تجميع البيانات داخل الجدول المحوري باستخدام الملف`PivotField` فصل. فيما يلي مثال لكيفية تجميع حقل في الجدول المحوري:

```java
// قم بالوصول إلى حقل "المنتج" في الجدول المحوري
PivotField productField = pivotTable.getPivotFields().get("Product");

//قم بتجميع حقل "المنتج" حسب معيار محدد، على سبيل المثال، بحرف البداية
productField.setIsAutoSubtotals(false);
productField.setBaseField("Product");
productField.setAutoSort(true);
productField.setAutoShow(true);

// احفظ ملف Excel المعدل بالبيانات المجمعة
workbook.save("output_grouped.xlsx");
```

## الخطوة 3: تخصيص التجميع

يمكنك أيضًا تخصيص إعدادات التجميع، مثل تحديد فترات التجميع المستندة إلى التاريخ أو قواعد التجميع المخصصة. فيما يلي مثال لتخصيص التجميع على أساس التاريخ:

```java
// الوصول إلى حقل "التاريخ" في الجدول المحوري (بافتراض أنه حقل تاريخ)
PivotField dateField = pivotTable.getPivotFields().get("Date");

// تجميع التواريخ حسب الأشهر
dateField.setIsAutoSubtotals(false);
dateField.setIsDateGroup(true);
dateField.setDateGroupingType(PivotFieldDateGroupingType.MONTHS);

// احفظ ملف Excel المعدل بتجميع تاريخ مخصص
workbook.save("output_custom_grouping.xlsx");
```

## خاتمة

يعد تجميع البيانات في الجداول المحورية أسلوبًا قيمًا لتحليل البيانات وتلخيصها في Excel، كما أن Aspose.Cells for Java يجعل من السهل أتمتة هذه العملية. باستخدام أمثلة التعليمات البرمجية المصدر المتوفرة، يمكنك إنشاء جداول محورية وتخصيص التجميع والحصول على رؤى من بياناتك بكفاءة.

## الأسئلة الشائعة

### 1. ما هو الغرض من الجداول المحورية في Excel؟

تُستخدم الجداول المحورية في Excel لتلخيص مجموعات البيانات الكبيرة وتحليلها. فهي تسمح لك بإنشاء طرق عرض مخصصة لبياناتك، مما يسهل تحديد الأنماط والاتجاهات.

### 2. كيف يمكنني تخصيص تجميع البيانات في جدول محوري؟

 يمكنك تخصيص تجميع البيانات في جدول محوري باستخدام`PivotField` فئة في Aspose.Cells لجافا. يتيح لك ذلك تحديد معايير التجميع، مثل الفواصل الزمنية المستندة إلى التاريخ أو القواعد المخصصة.

### 3. هل يمكنني أتمتة عملية إنشاء الجداول المحورية باستخدام Aspose.Cells لـ Java؟

نعم، يمكنك أتمتة عملية إنشاء الجداول المحورية في Excel باستخدام Aspose.Cells لـ Java، كما هو موضح في أمثلة التعليمات البرمجية المصدر المتوفرة.