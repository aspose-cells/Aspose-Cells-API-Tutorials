---
title: قم بتعيين خيارات طباعة Excel
linktitle: قم بتعيين خيارات طباعة Excel
second_title: Aspose.Cells لمرجع .NET API
description: تعلم كيفية التعامل مع ملفات Excel وتخصيص خيارات الطباعة بسهولة باستخدام Aspose.Cells for .NET.
type: docs
weight: 150
url: /ar/net/excel-page-setup/set-excel-print-options/
---
سنرشدك في هذا الدليل إلى كيفية تعيين خيارات الطباعة لمصنف Excel باستخدام Aspose.Cells for .NET. سنأخذك خطوة بخطوة عبر كود مصدر C# المقدم لإنجاز هذه المهمة.

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

لتعيين خيارات الطباعة، نحتاج أولاً إلى الحصول على مرجع PageSetup من ورقة العمل. استخدم الكود التالي للحصول على المرجع:

```csharp
PageSetup pageSetup = workbook.Worksheets[0].PageSetup;
```

## الخطوة 6: تمكين طباعة خطوط الشبكة

لتمكين طباعة خطوط الشبكة، استخدم الكود التالي:

```csharp
pageSetup. PrintGridlines = true;
```

## الخطوة 7: تمكين طباعة رأس الصف/العمود

لتمكين طباعة رؤوس الصفوف والأعمدة، استخدم الكود التالي:

```csharp
pageSetup.PrintHeadings = true;
```

## الخطوة 8: تمكين وضع الطباعة بالأبيض والأسود

لتمكين طباعة ورقة العمل بالأبيض والأسود، استخدم الكود التالي:

```csharp
pageSetup.BlackAndWhite = true;
```

## الخطوة 9: تمكين طباعة الملاحظات

للسماح بطباعة التعليقات كما تظهر في جدول البيانات، استخدم الكود التالي:

```csharp
pageSetup.PrintComments = PrintCommentsType.PrintInPlace;
```

## الخطوة 10: تمكين طباعة وضع المسودة

لتمكين طباعة جدول البيانات في وضع المسودة، استخدم الكود التالي:

```csharp
pageSetup.PrintDraft = true;
```

## الخطوة 11: تمكين أخطاء خلية الطباعة كـ N/A

للسماح بطباعة أخطاء الخلايا كـ

  من N/A، استخدم الكود التالي:

```csharp
pageSetup.PrintErrors = PrintErrorsType.PrintErrorsNA;
```

## الخطوة 12: حفظ مصنف Excel

 لحفظ مصنف Excel مع مجموعة خيارات الطباعة، استخدم`Save` طريقة كائن المصنف:

```csharp
workbook.Save(dataDir + "OtherPrintOptions_out.xls");
```

سيؤدي هذا إلى حفظ مصنف Excel باسم الملف "OtherPrintOptions_out.xls" في الدليل المحدد.

### نموذج التعليمات البرمجية المصدر لتعيين خيارات طباعة Excel باستخدام Aspose.Cells لـ .NET 
```csharp
//المسار إلى دليل المستندات.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// إنشاء مثيل لكائن المصنف
Workbook workbook = new Workbook();
// الحصول على مرجع PageSetup لورقة العمل
PageSetup pageSetup = workbook.Worksheets[0].PageSetup;
// السماح بطباعة خطوط الشبكة
pageSetup.PrintGridlines = true;
// السماح بطباعة عناوين الصفوف/الأعمدة
pageSetup.PrintHeadings = true;
// السماح بطباعة ورقة العمل في الوضع الأسود والأبيض
pageSetup.BlackAndWhite = true;
// السماح بطباعة التعليقات كما هو معروض في ورقة العمل
pageSetup.PrintComments = PrintCommentsType.PrintInPlace;
// السماح بطباعة ورقة العمل بجودة المسودة
pageSetup.PrintDraft = true;
// السماح بطباعة أخطاء الخلايا كـ N/A
pageSetup.PrintErrors = PrintErrorsType.PrintErrorsNA;
// احفظ المصنف.
workbook.Save(dataDir + "OtherPrintOptions_out.xls");
```
## خاتمة

لقد تعلمت الآن كيفية تعيين خيارات الطباعة لمصنف Excel باستخدام Aspose.Cells لـ .NET. تتيح لك هذه المكتبة القوية وسهلة الاستخدام تخصيص إعدادات الطباعة لمصنفات Excel الخاصة بك بطريقة سهلة وفعالة.

### الأسئلة الشائعة


#### 1. هل يمكنني تخصيص خيارات الطباعة بشكل أكبر، مثل الهوامش أو اتجاه الصفحة؟

نعم، يوفر Aspose.Cells for .NET نطاقًا واسعًا من خيارات الطباعة القابلة للتخصيص، مثل الهوامش واتجاه الصفحة والمقياس وما إلى ذلك.

#### 2. هل يدعم Aspose.Cells for .NET تنسيقات ملفات Excel الأخرى؟

نعم، يدعم Aspose.Cells for .NET مجموعة متنوعة من تنسيقات ملفات Excel، مثل XLSX، وXLS، وCSV، وHTML، وPDF، وما إلى ذلك.

#### 3. هل يتوافق Aspose.Cells for .NET مع كافة إصدارات .NET Framework؟

يتوافق Aspose.Cells for .NET مع .NET Framework 2.0 أو الإصدارات الأحدث، بما في ذلك الإصدارات 3.5 و4.0 و4.5 و4.6 وما إلى ذلك.