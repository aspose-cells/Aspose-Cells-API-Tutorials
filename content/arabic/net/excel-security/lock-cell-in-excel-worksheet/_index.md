---
title: قفل الخلية في ورقة عمل Excel
linktitle: قفل الخلية في ورقة عمل Excel
second_title: Aspose.Cells لمرجع .NET API
description: دليل خطوة بخطوة لقفل خلية في ورقة عمل Excel باستخدام Aspose.Cells لـ .NET.
type: docs
weight: 20
url: /ar/net/excel-security/lock-cell-in-excel-worksheet/
---
غالبًا ما تُستخدم ورقة عمل Excel لتخزين البيانات المهمة وتنظيمها. في بعض الحالات، قد يكون من الضروري قفل خلايا معينة لمنع التعديل العرضي أو غير المصرح به. سنشرح في هذا الدليل كيفية قفل خلية معينة في ورقة عمل Excel باستخدام Aspose.Cells for .NET، وهي مكتبة شائعة لمعالجة ملفات Excel.

## الخطوة 1: إعداد المشروع

قبل أن تبدأ، تأكد من قيامك بتكوين مشروع C# الخاص بك لاستخدام Aspose.Cells. يمكنك القيام بذلك عن طريق إضافة مرجع إلى مكتبة Aspose.Cells إلى مشروعك واستيراد مساحة الاسم المطلوبة:

```csharp
using Aspose.Cells;
```

## الخطوة 2: تحميل ملف Excel

الخطوة الأولى هي تحميل ملف Excel الذي تريد قفل الخلية فيه. تأكد من تحديد المسار الصحيح لدليل المستند الخاص بك:

```csharp
//المسار إلى دليل المستندات.
string dataDir = "YOUR_DIRECTORY_OF_DOCUMENTS";
Workbook workbook = new Workbook(dataDir + "Book1.xlsx");
```

## الخطوة 3: الوصول إلى ورقة العمل

الآن وبعد أن قمنا بتحميل ملف Excel، يمكننا الانتقال إلى جدول البيانات الأول في الملف. في هذا المثال، نفترض أن ورقة العمل التي نريد تعديلها هي ورقة العمل الأولى (الفهرس 0):

```csharp
//الوصول إلى جدول البيانات الأول من ملف Excel
Worksheet worksheet = workbook.Worksheets[0];
```

## الخطوة 4: قفل الخلية

الآن وبعد أن وصلنا إلى ورقة العمل، يمكننا المتابعة لقفل الخلية المحددة. في هذا المثال، سوف نقوم بقفل الخلية A1. وإليك كيف يمكنك القيام بذلك:

```csharp
worksheet.Cells["A1"].GetStyle().IsLocked = true;
```

## الخطوة 5: حماية ورقة العمل

أخيرًا، لكي يصبح قفل الخلية ساري المفعول، نحتاج إلى حماية ورقة العمل. سيؤدي هذا إلى منع المزيد من التحرير للخلايا المقفلة:

```csharp
worksheet.Protect(ProtectionType.All);
```

## الخطوة 6: حفظ ملف Excel المعدل

بمجرد إجراء التغييرات التي تريدها، يمكنك حفظ ملف Excel المعدل:

```csharp
workbook.Save(dataDir + "output.xlsx");
```

تهنئة ! لقد نجحت الآن في تأمين خلية معينة في ورقة عمل Excel باستخدام Aspose.Cells لـ .NET.

### نموذج التعليمات البرمجية المصدر لورقة عمل Lock Cell In Excel باستخدام Aspose.Cells لـ .NET 
```csharp
//المسار إلى دليل المستندات.
string dataDir = "YOUR DOCUMENT DIRECTORY";
Workbook workbook = new Workbook(dataDir + "Book1.xlsx");
// الوصول إلى ورقة العمل الأولى في ملف Excel
Worksheet worksheet = workbook.Worksheets[0];
worksheet.Cells["A1"].GetStyle().IsLocked = true;
// أخيرًا، قم بحماية الورقة الآن.
worksheet.Protect(ProtectionType.All);
workbook.Save(dataDir + "output.xlsx");
```

## خاتمة

في هذا الدليل خطوة بخطوة، شرحنا كيفية قفل خلية في جدول بيانات Excel باستخدام Aspose.Cells for .NET. باتباع الخطوات المتوفرة، يمكنك بسهولة قفل خلايا معينة في ملفات Excel، مما قد يكون مفيدًا في حماية البيانات المهمة من التغييرات غير المصرح بها.

### الأسئلة الشائعة

#### س: هل يمكنني تأمين خلايا متعددة في ورقة عمل Excel؟
	 
A. نعم، يمكنك قفل أي عدد تريده من الخلايا باستخدام الطريقة الموضحة في هذا الدليل. كل ما عليك فعله هو تكرار الخطوتين 4 و5 لكل خلية تريد قفلها.

#### س. كيف يمكنني فتح خلية مقفلة في ورقة عمل Excel؟

A.  لفتح خلية مقفلة، يمكنك استخدام`IsLocked` الطريقة واضبطها على`false`. تأكد من الانتقال إلى الخلية الصحيحة في جدول البيانات.

#### س: هل يمكنني حماية جدول بيانات Excel بكلمة مرور؟

A.  نعم، يوفر Aspose.Cells إمكانية حماية جدول بيانات Excel بكلمة مرور. يمكنك استخدام ال`Protect` الطريقة عن طريق تحديد نوع الحماية`ProtectionType.All` وتوفير كلمة المرور.

#### س: هل يمكنني تطبيق الأنماط على الخلايا المقفلة؟

A. نعم، يمكنك تطبيق الأنماط على الخلايا المقفلة باستخدام الوظيفة التي توفرها Aspose.Cells. يمكنك تعيين أنماط الخطوط والتنسيق وأنماط الحدود وما إلى ذلك للخلايا المقفلة.

#### س: هل يمكنني تأمين نطاق من الخلايا بدلاً من خلية واحدة؟

A.  نعم، يمكنك قفل نطاق من الخلايا باستخدام نفس الخطوات الموضحة في هذا الدليل. بدلاً من تحديد خلية واحدة، يمكنك تحديد نطاق من الخلايا، على سبيل المثال:`worksheet.Cells["A1:B5"].GetStyle().IsLocked = true;`.