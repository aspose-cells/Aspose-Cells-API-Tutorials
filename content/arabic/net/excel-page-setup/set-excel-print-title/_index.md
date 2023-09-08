---
title: تعيين عنوان طباعة Excel
linktitle: تعيين عنوان طباعة Excel
second_title: Aspose.Cells لمرجع .NET API
description: تعلم كيفية التعامل بسهولة مع ملفات Excel وتخصيص خيارات الطباعة باستخدام Aspose.Cells لـ .NET.
type: docs
weight: 170
url: /ar/net/excel-page-setup/set-excel-print-title/
---
سنرشدك في هذا الدليل إلى كيفية تعيين عناوين الطباعة في جدول بيانات Excel باستخدام Aspose.Cells for .NET. اتبع الخطوات أدناه لإنجاز هذه المهمة.

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

## الخطوة 4: إنشاء كائن مصنف

قم بإنشاء مثيل لكائن مصنف يمثل مصنف Excel الذي تريد إنشاءه:

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

قمنا هنا بتعريف العمودين A وB كأعمدة عنوان. يمكنك ضبط هذه القيمة وفقًا لاحتياجاتك.

## الخطوة 7: تحديد خطوط العنوان

حدد سطور العنوان باستخدام الكود التالي:

```csharp
pageSetup.PrintTitleRows = "$1:$2";
```

لقد قمنا بتعريف الصفوف 1 و 2 كصفوف عنوان. يمكنك ضبط هذه القيم وفقًا لاحتياجاتك.

## الخطوة 8: حفظ مصنف Excel

 لحفظ مصنف Excel مع عناوين الطباعة المحددة، استخدم الملف`Save` طريقة كائن المصنف:

```csharp
workbook.Save(dataDir + "SetPrintTitle_out.xls");
```

سيؤدي هذا إلى حفظ مصنف Excel باسم الملف "SetPrintTitle_out.xls" في الدليل المحدد.

### نموذج التعليمات البرمجية المصدر لـ Set Excel Print Title باستخدام Aspose.Cells لـ .NET 
```csharp
//المسار إلى دليل المستندات.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// إنشاء مثيل لكائن المصنف
Workbook workbook = new Workbook();
// الحصول على مرجع PageSetup لورقة العمل
Aspose.Cells.PageSetup pageSetup = workbook.Worksheets[0].PageSetup;
// تحديد أرقام الأعمدة A وB كأعمدة عنوان
pageSetup.PrintTitleColumns = "$A:$B";
// تحديد أرقام الصفوف 1 و 2 كصفوف عنوان
pageSetup.PrintTitleRows = "$1:$2";
// احفظ المصنف.
workbook.Save(dataDir + "SetPrintTitle_out.xls");
```

## خاتمة

تهنئة ! لقد تعلمت كيفية تعيين عناوين الطباعة في جدول بيانات Excel باستخدام Aspose.Cells لـ .NET. تسمح لك عناوين الطباعة بعرض صفوف وأعمدة محددة في كل صفحة مطبوعة، مما يسهل قراءة البيانات والرجوع إليها.

### الأسئلة الشائعة

#### 1. هل يمكنني تعيين عناوين الطباعة لأعمدة محددة في Excel؟

 نعم، باستخدام Aspose.Cells for .NET، يمكنك تعيين أعمدة محددة كعناوين مطبوعة باستخدام`PrintTitleColumns` ملكية`PageSetup` هدف.

#### 2. هل من الممكن تحديد عناوين الأعمدة وصفوف الطباعة؟

 نعم، يمكنك تعيين عناوين الأعمدة والصفوف للطباعة باستخدام الزر`PrintTitleColumns` و`PrintTitleRows` خصائص`PageSetup` هدف.

#### 3. ما هي إعدادات التخطيط الأخرى التي يمكنني تخصيصها باستخدام Aspose.Cells لـ .NET؟

باستخدام Aspose.Cells for .NET، يمكنك تخصيص إعدادات تخطيط الصفحة المختلفة، مثل الهوامش واتجاه الصفحة ومقياس الطباعة والمزيد.