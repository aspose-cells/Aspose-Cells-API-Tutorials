---
title: قم بتعيين عنوان طباعة Excel
linktitle: قم بتعيين عنوان طباعة Excel
second_title: Aspose.Cells لمرجع .NET API
description: تعلم كيفية التعامل مع ملفات Excel بسهولة وتخصيص خيارات الطباعة باستخدام Aspose.Cells for .NET.
type: docs
weight: 170
url: /ar/net/excel-page-setup/set-excel-print-title/
---
في هذا الدليل ، سنرشدك إلى كيفية تعيين عناوين الطباعة في جدول بيانات Excel باستخدام Aspose.Cells for .NET. اتبع الخطوات أدناه لإنجاز هذه المهمة.

## الخطوة الأولى: تهيئة البيئة

تأكد من قيامك بإعداد بيئة التطوير الخاصة بك وتثبيت Aspose.Cells لـ .NET. يمكنك تنزيل أحدث إصدار من المكتبة من موقع Aspose الرسمي.

## الخطوة 2: استيراد مساحات الأسماء المطلوبة

في مشروع C # الخاص بك ، قم باستيراد مساحات الأسماء الضرورية للعمل مع Aspose.

```csharp
using Aspose.Cells;
```

## الخطوة 3: تحديد المسار إلى دليل المستندات

 تعلن أ`dataDir` متغير لتحديد المسار إلى الدليل حيث تريد حفظ ملف Excel الذي تم إنشاؤه:

```csharp
string dataDir = "YOUR_DIRECTORY_OF_DOCUMENTS";
```

 تأكد من استبدال`"YOUR_DOCUMENT_DIRECTORY"` مع المسار الصحيح على نظامك.

## الخطوة 4: إنشاء كائن مصنف

إنشاء كائن مصنف يمثل مصنف Excel الذي تريد إنشاءه:

```csharp
Workbook workbook = new Workbook();
```

## الخطوة 5: الوصول إلى ورقة العمل الأولى

انتقل إلى ورقة العمل الأولى في مصنف Excel باستخدام الكود التالي:

```csharp
Worksheet worksheet = workbook.Worksheets[0];
```

## الخطوة 6: تحديد أعمدة العنوان

حدد أعمدة العنوان باستخدام الكود التالي:

```csharp
pageSetup.PrintTitleColumns = "$A:$B";
```

هنا قمنا بتعريف الأعمدة A و B كأعمدة عنوان. يمكنك ضبط هذه القيمة وفقًا لاحتياجاتك.

## الخطوة 7: تحديد خطوط العنوان

حدد سطور العنوان باستخدام الكود التالي:

```csharp
pageSetup.PrintTitleRows = "$1:$2";
```

لقد حددنا الصفوف 1 و 2 كصفوف عنوان. يمكنك ضبط هذه القيم وفقًا لاحتياجاتك.

## الخطوة 8: حفظ مصنف Excel

 لحفظ مصنف Excel مع تحديد عناوين الطباعة ، استخدم ملحق`Save` طريقة كائن المصنف:

```csharp
workbook.Save(dataDir + "SetPrintTitle_out.xls");
```

سيؤدي هذا إلى حفظ مصنف Excel باسم الملف "SetPrintTitle_out.xls" في الدليل المحدد.

### نموذج التعليمات البرمجية المصدر لـ Set Excel Print Title باستخدام Aspose.Cells for .NET 
```csharp
// المسار إلى دليل المستندات.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// إنشاء كائن مصنف
Workbook workbook = new Workbook();
// الحصول على مرجع إعداد الصفحة الخاص بورقة العمل
Aspose.Cells.PageSetup pageSetup = workbook.Worksheets[0].PageSetup;
// تحديد أرقام العمود A & B كأعمدة عنوان
pageSetup.PrintTitleColumns = "$A:$B";
// تحديد أرقام الصفوف 1 و 2 كصفوف عنوان
pageSetup.PrintTitleRows = "$1:$2";
// احفظ المصنف.
workbook.Save(dataDir + "SetPrintTitle_out.xls");
```

## خاتمة

تهنئة ! لقد تعلمت كيفية تعيين عناوين الطباعة في جدول بيانات Excel باستخدام Aspose.Cells لـ .NET. تسمح لك عناوين الطباعة بعرض صفوف وأعمدة محددة على كل صفحة مطبوعة ، مما يسهل قراءة البيانات والرجوع إليها.

### أسئلة وأجوبة

#### 1. هل يمكنني تعيين عناوين طباعة لأعمدة معينة في Excel؟

 نعم ، باستخدام Aspose.Cells for .NET ، يمكنك تعيين أعمدة محددة كعناوين طباعة باستخدام امتداد`PrintTitleColumns` ممتلكات`PageSetup` هدف.

#### 2. هل من الممكن تحديد كل من عناوين الأعمدة وصفوف الطباعة؟

 نعم ، يمكنك تعيين كل من عناوين أعمدة الطباعة والصفوف باستخدام ملف`PrintTitleColumns` و`PrintTitleRows` خصائص`PageSetup` هدف.

#### 3. ما هي إعدادات التخطيط الأخرى التي يمكنني تخصيصها باستخدام Aspose.Cells for .NET؟

باستخدام Aspose.Cells for .NET ، يمكنك تخصيص العديد من إعدادات تخطيط الصفحة ، مثل الهوامش واتجاه الصفحة ومقياس الطباعة والمزيد.