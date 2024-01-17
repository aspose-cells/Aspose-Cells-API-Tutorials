---
title: ضبط عامل تحجيم Excel
linktitle: ضبط عامل تحجيم Excel
second_title: Aspose.Cells لمرجع .NET API
description: تعلم كيفية التعامل بسهولة مع ملفات Excel وتخصيص عامل القياس باستخدام Aspose.Cells لـ .NET.
type: docs
weight: 180
url: /ar/net/excel-page-setup/set-excel-scaling-factor/
---
في هذا الدليل، سنرشدك إلى كيفية تعيين عامل القياس في جدول بيانات Excel باستخدام Aspose.Cells for .NET. اتبع الخطوات أدناه لإنجاز هذه المهمة.

## الخطوة 1: تهيئة البيئة

تأكد من قيامك بإعداد بيئة التطوير الخاصة بك وتثبيت Aspose.Cells لـ .NET. يمكنك تنزيل أحدث إصدار من المكتبة من موقع Aspose الرسمي.

## الخطوة 2: استيراد مساحات الأسماء المطلوبة

في مشروع C# الخاص بك، قم باستيراد مساحات الأسماء الضرورية للعمل مع Aspose.Cells:

```csharp
using Aspose.Cells;
```

## الخطوة 3: تحديد المسار إلى دليل المستندات

 أعلن أ`dataDir` متغير لتحديد المسار إلى الدليل الذي تريد حفظ ملف Excel الذي تم إنشاؤه فيه:

```csharp
string dataDir = "YOUR_DIRECTORY_OF_DOCUMENTS";
```

 تأكد من استبدال`"YOUR_DOCUMENT_DIRECTORY"` بالمسار الصحيح على نظامك.

## الخطوة 4: إنشاء كائن المصنف

قم بإنشاء مثيل لكائن مصنف يمثل مصنف Excel الذي تريد إنشاءه:

```csharp
Workbook workbook = new Workbook();
```

## الخطوة 5: الوصول إلى ورقة العمل الأولى

انتقل إلى ورقة العمل الأولى في مصنف Excel باستخدام الكود التالي:

```csharp
Worksheet worksheet = workbook.Worksheets[0];
```

## الخطوة 6: تعيين عامل القياس

قم بتعيين عامل القياس باستخدام الكود التالي:

```csharp
worksheet.PageSetup.Zoom = 100;
```

لقد قمنا هنا بتعيين عامل القياس على 100، مما يعني أنه سيتم عرض جدول البيانات بنسبة 100% من الحجم الطبيعي عند طباعته.

## الخطوة 7: حفظ مصنف Excel

 لحفظ مصنف Excel بعامل القياس المحدد، استخدم الأمر`Save` طريقة كائن المصنف:

```csharp
workbook.Save(dataDir + "ScalingFactor_out.xls");
```

سيؤدي هذا إلى حفظ مصنف Excel باسم الملف "ScalingFactor_out.xls" في الدليل المحدد.

### نموذج التعليمات البرمجية المصدر لـ Set Excel Scaling Factor باستخدام Aspose.Cells لـ .NET 
```csharp
//المسار إلى دليل المستندات.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// إنشاء مثيل لكائن المصنف
Workbook workbook = new Workbook();
// الوصول إلى ورقة العمل الأولى في ملف Excel
Worksheet worksheet = workbook.Worksheets[0];
// ضبط عامل التحجيم على 100
worksheet.PageSetup.Zoom = 100;
// احفظ المصنف.
workbook.Save(dataDir + "ScalingFactor_out.xls");
```

## خاتمة

تهنئة ! لقد تعلمت كيفية تعيين عامل القياس في جدول بيانات Excel باستخدام Aspose.Cells لـ .NET. يتيح لك عامل القياس ضبط حجم جدول البيانات عند الطباعة للحصول على العرض الأمثل.

### الأسئلة الشائعة

#### 1. كيفية تعيين عامل القياس في جدول بيانات Excel باستخدام Aspose.Cells لـ .NET؟

 استخدم ال`Zoom` ملكية`PageSetup`كائن لتعيين عامل التحجيم. على سبيل المثال،`worksheet.PageSetup.Zoom = 100;` سيتم تعيين عامل التحجيم إلى 100%.

#### 2. هل يمكنني تخصيص عامل القياس وفقًا لاحتياجاتي؟

 نعم، يمكنك ضبط عامل القياس عن طريق تغيير القيمة المخصصة لـ`Zoom` ملكية. على سبيل المثال،`worksheet.PageSetup.Zoom = 75;` سيتم ضبط عامل التحجيم على 75٪.

#### 3. هل من الممكن حفظ مصنف Excel بعامل القياس المحدد؟

 نعم يمكنك استخدام`Save` طريقة`Workbook` كائن لحفظ مصنف Excel بعامل القياس المحدد.