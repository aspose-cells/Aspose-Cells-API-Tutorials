---
title: قم بتعيين منطقة طباعة Excel
linktitle: قم بتعيين منطقة طباعة Excel
second_title: Aspose.Cells لمرجع .NET API
description: دليل خطوة بخطوة لتعيين منطقة طباعة Excel باستخدام Aspose.Cells for .NET. قم بتحسين وتخصيص مصنفات Excel بسهولة.
type: docs
weight: 140
url: /ar/net/excel-page-setup/set-excel-print-area/
---
يمكن أن يؤدي استخدام Aspose.Cells for .NET إلى تسهيل إدارة ومعالجة ملفات Excel في تطبيقات .NET بشكل كبير. في هذا الدليل ، سنوضح لك كيفية تعيين منطقة الطباعة لمصنف Excel باستخدام Aspose.Cells for .NET. سنوجهك خطوة بخطوة عبر الكود المصدري C # لإنجاز هذه المهمة.

## الخطوة الأولى: تهيئة البيئة

قبل أن تبدأ ، تأكد من إعداد بيئة التطوير وتثبيت Aspose.Cells لـ .NET. يمكنك تنزيل أحدث إصدار من المكتبة من موقع Aspose الرسمي.

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

## الخطوة 5: الحصول على مرجع PageSetup الخاص بورقة العمل

لتعيين منطقة الطباعة ، نحتاج أولاً إلى الحصول على المرجع من PageSetup في ورقة العمل. استخدم الكود التالي للحصول على المرجع:

```csharp
PageSetup pageSetup = workbook.Worksheets[0].PageSetup;
```

## الخطوة 6: تحديد نطاق خلية منطقة الطباعة

الآن بعد أن أصبح لدينا مرجع PageSetup ، يمكننا تحديد نطاق الخلايا التي تشكل منطقة الطباعة. في هذا المثال ، سنقوم بتعيين نطاق الخلايا من A1 إلى T35 كمنطقة طباعة. استخدم الكود التالي:

```csharp
pageSetup.PrintArea = "A1:T35";
```

يمكنك ضبط نطاق الخلايا وفقًا لاحتياجاتك.

## الخطوة 7: حفظ مصنف Excel

 لحفظ مصنف Excel مع تحديد منطقة الطباعة ، استخدم ملحق`Save` طريقة كائن المصنف:

```csharp
workbook.Save(dataDir + "SetPrintArea_out.xls");
```

سيؤدي هذا إلى حفظ مصنف Excel باسم الملف "SetPrintArea_out.xls" في الدليل المحدد.

### نموذج التعليمات البرمجية المصدر لـ Set Excel Print Area باستخدام Aspose.Cells for .NET 
```csharp
// المسار إلى دليل المستندات.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// إنشاء كائن مصنف
Workbook workbook = new Workbook();
// الحصول على مرجع إعداد الصفحة الخاص بورقة العمل
PageSetup pageSetup = workbook.Worksheets[0].PageSetup;
// تحديد نطاق الخلايا (من خلية A1 إلى خلية T35) لمنطقة الطباعة
pageSetup.PrintArea = "A1:T35";
// احفظ المصنف.
workbook.Save(dataDir + "SetPrintArea_out.xls");
```

## خاتمة

تهنئة ! لقد تعلمت الآن كيفية تعيين منطقة الطباعة لمصنف Excel باستخدام Aspose.Cells لـ .NET. تسهل هذه المكتبة القوية وسهلة الاستخدام العمل مع ملفات Excel في تطبيقات .NET الخاصة بك. إذا كانت لديك أسئلة إضافية أو واجهت أي صعوبات ، فلا تتردد في مراجعة وثائق Aspose.Cells الرسمية لمزيد من المعلومات والموارد.

### التعليمات

#### 1. هل يمكنني تخصيص تخطيط منطقة الطباعة بشكل أكبر ، مثل الاتجاه والهوامش؟

نعم ، يمكنك الوصول إلى خصائص إعداد الصفحة الأخرى مثل اتجاه الصفحة والهوامش والمقياس وما إلى ذلك لتخصيص تخطيط منطقة الطباعة بشكل أكبر.

#### 2. هل يدعم Aspose.Cells for .NET تنسيقات ملفات Excel الأخرى ، مثل XLSX و CSV؟

نعم ، يدعم Aspose.Cells for .NET مجموعة متنوعة من تنسيقات ملفات Excel بما في ذلك XLSX و XLS و CSV و HTML و PDF وغيرها الكثير.

#### 3. هل Aspose.Cells for .NET متوافق مع كافة إصدارات .NET Framework؟

Aspose.Cells for .NET متوافق مع .NET Framework 2.0 أو أحدث ، بما في ذلك الإصدارات 3.5 و 4.0 و 4.5 و 4.6 وما إلى ذلك.