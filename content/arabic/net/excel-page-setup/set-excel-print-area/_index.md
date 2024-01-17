---
title: قم بتعيين منطقة طباعة Excel
linktitle: قم بتعيين منطقة طباعة Excel
second_title: Aspose.Cells لمرجع .NET API
description: دليل خطوة بخطوة لتعيين منطقة طباعة Excel باستخدام Aspose.Cells لـ .NET. قم بتحسين مصنفات Excel وتخصيصها بسهولة.
type: docs
weight: 140
url: /ar/net/excel-page-setup/set-excel-print-area/
---
يمكن أن يؤدي استخدام Aspose.Cells لـ .NET إلى تسهيل إدارة ملفات Excel ومعالجتها في تطبيقات .NET بشكل كبير. سنوضح لك في هذا الدليل كيفية تعيين منطقة الطباعة لمصنف Excel باستخدام Aspose.Cells for .NET. سنرشدك خطوة بخطوة عبر كود مصدر C# المقدم لإنجاز هذه المهمة.

## الخطوة 1: تهيئة البيئة

قبل أن تبدأ، تأكد من إعداد بيئة التطوير الخاصة بك وتثبيت Aspose.Cells لـ .NET. يمكنك تنزيل أحدث إصدار من المكتبة من موقع Aspose الرسمي.

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

## الخطوة 5: الحصول على مرجع PageSetup لورقة العمل

لتعيين منطقة الطباعة، نحتاج أولاً إلى الحصول على المرجع من PageSetup الخاص بورقة العمل. استخدم الكود التالي للحصول على المرجع:

```csharp
PageSetup pageSetup = workbook.Worksheets[0].PageSetup;
```

## الخطوة 6: تحديد نطاق خلايا منطقة الطباعة

الآن بعد أن أصبح لدينا مرجع PageSetup، يمكننا تحديد نطاق الخلايا التي تشكل منطقة الطباعة. في هذا المثال، سنقوم بتعيين نطاق الخلايا من A1 إلى T35 كمنطقة للطباعة. استخدم الكود التالي:

```csharp
pageSetup.PrintArea = "A1:T35";
```

يمكنك ضبط نطاق الخلايا وفقًا لاحتياجاتك.

## الخطوة 7: حفظ مصنف Excel

 لحفظ مصنف Excel مع تحديد منطقة الطباعة، استخدم الملف`Save` طريقة كائن المصنف:

```csharp
workbook.Save(dataDir + "SetPrintArea_out.xls");
```

سيؤدي هذا إلى حفظ مصنف Excel باسم الملف "SetPrintArea_out.xls" في الدليل المحدد.

### نموذج التعليمات البرمجية المصدر لـ Set Excel Print Area باستخدام Aspose.Cells لـ .NET 
```csharp
//المسار إلى دليل المستندات.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// إنشاء مثيل لكائن المصنف
Workbook workbook = new Workbook();
// الحصول على مرجع PageSetup لورقة العمل
PageSetup pageSetup = workbook.Worksheets[0].PageSetup;
// تحديد نطاق الخلايا (من الخلية A1 إلى الخلية T35) لمنطقة الطباعة
pageSetup.PrintArea = "A1:T35";
// احفظ المصنف.
workbook.Save(dataDir + "SetPrintArea_out.xls");
```

## خاتمة

تهنئة ! لقد تعلمت الآن كيفية تعيين منطقة الطباعة لمصنف Excel باستخدام Aspose.Cells لـ .NET. تعمل هذه المكتبة القوية وسهلة الاستخدام على تسهيل العمل مع ملفات Excel في تطبيقات .NET الخاصة بك. إذا كانت لديك أسئلة إضافية أو واجهت أي صعوبات، فلا تتردد في مراجعة وثائق Aspose.Cells الرسمية لمزيد من المعلومات والموارد.

### الأسئلة الشائعة

#### 1. هل يمكنني تخصيص تخطيط منطقة الطباعة بشكل أكبر، مثل الاتجاه والهوامش؟

نعم، يمكنك الوصول إلى خصائص PageSetup الأخرى مثل اتجاه الصفحة والهوامش والمقياس وما إلى ذلك لتخصيص تخطيط منطقة الطباعة بشكل أكبر.

#### 2. هل يدعم Aspose.Cells for .NET تنسيقات ملفات Excel الأخرى، مثل XLSX وCSV؟

نعم، يدعم Aspose.Cells for .NET مجموعة متنوعة من تنسيقات ملفات Excel بما في ذلك XLSX وXLS وCSV وHTML وPDF وغيرها الكثير.

#### 3. هل يتوافق Aspose.Cells for .NET مع كافة إصدارات .NET Framework؟

يتوافق Aspose.Cells for .NET مع .NET Framework 2.0 أو الإصدارات الأحدث، بما في ذلك الإصدارات 3.5 و4.0 و4.5 و4.6 وما إلى ذلك.