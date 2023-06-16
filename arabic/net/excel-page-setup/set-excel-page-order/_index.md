---
title: قم بتعيين ترتيب صفحات Excel
linktitle: قم بتعيين ترتيب صفحات Excel
second_title: Aspose.Cells لمرجع .NET API
description: دليل خطوة بخطوة لتعيين ترتيب الصفحات في Excel باستخدام Aspose.Cells for .NET. تعليمات مفصلة وشفرة المصدر متضمنة.
type: docs
weight: 120
url: /ar/net/excel-page-setup/set-excel-page-order/
---
في هذه المقالة ، سنوجهك خطوة بخطوة لشرح التعليمات البرمجية المصدر C # التالية لتعيين ترتيب صفحات Excel باستخدام Aspose.Cells for .NET. سنوضح لك كيفية إعداد دليل المستندات وإنشاء مثيل لكائن مصنف والحصول على مرجع إعداد الصفحة وتعيين ترتيب طباعة الصفحة وحفظ المصنف.

## الخطوة 1: إعداد دليل المستند

 قبل أن تبدأ ، تحتاج إلى تكوين دليل المستند حيث تريد حفظ ملف Excel. يمكنك تحديد مسار الدليل عن طريق استبدال قيمة`dataDir` متغير مع المسار الخاص بك.

```csharp
// المسار إلى دليل المستندات.
string dataDir = "YOUR_DIRECTORY_OF_DOCUMENTS";
```

## الخطوة 2: إنشاء كائن مصنف

الخطوة الأولى هي إنشاء كائن مصنف. هذا يمثل مصنف Excel الذي سنعمل معه.

```csharp
// إنشاء كائن مصنف
Workbook workbook = new Workbook();
```

## الخطوة 3: الحصول على مرجع PageSetup

بعد ذلك ، نحتاج إلى الحصول على مرجع كائن PageSetup الخاص بورقة العمل التي نريد ضبط ترتيب الصفحات عليها.

```csharp
// احصل على مرجع PageSetup الخاص بورقة العمل
PageSetup pageSetup = workbook.Worksheets[0].PageSetup;
```

## الخطوة 4: تعيين ترتيب طباعة الصفحات

الآن يمكننا ضبط ترتيب طباعة الصفحات. في هذا المثال ، نستخدم خيار "OverThenDown" ، مما يعني أنه ستتم طباعة الصفحات من اليسار إلى اليمين ، ثم من أعلى إلى أسفل.

```csharp
// تعيين ترتيب طباعة الصفحة على "OverThenDown"
pageSetup.Order = PrintOrderType.OverThenDown;
```

## الخطوة 5: حفظ المصنف

أخيرًا ، نحفظ مصنف Excel مع تغييرات ترتيب الصفحات.

```csharp
// احفظ المصنف
workbook.Save(dataDir + "SetPageOrder_out.xls");
```

### نموذج التعليمات البرمجية المصدر لـ Set Excel Page Order باستخدام Aspose.Cells for .NET 
```csharp
// المسار إلى دليل المستندات.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// إنشاء كائن مصنف
Workbook workbook = new Workbook();
// الحصول على مرجع إعداد الصفحة الخاص بورقة العمل
PageSetup pageSetup = workbook.Worksheets[0].PageSetup;
// تعيين ترتيب طباعة الصفحات إلى أعلى ثم لأسفل
pageSetup.Order = PrintOrderType.OverThenDown;
// احفظ المصنف.
workbook.Save(dataDir + "SetPageOrder_out.xls");
```

## خاتمة

في هذا البرنامج التعليمي ، شرحنا كيفية تعيين ترتيب الصفحات في ملف Excel باستخدام Aspose.Cells for .NET. باتباع الخطوات المقدمة ، يمكنك بسهولة تكوين دليل المستند وإنشاء مثيل لكائن مصنف والحصول على مرجع إعداد الصفحة وتعيين ترتيب طباعة الصفحة وحفظ المصنف.

### التعليمات

#### س 1: ما سبب أهمية تعيين ترتيب الصفحات في ملف Excel؟

يعد تحديد ترتيب الصفحات في ملف Excel أمرًا مهمًا لأنه يحدد كيفية طباعة الصفحات أو عرضها. من خلال تحديد ترتيب معين ، يمكنك تنظيم البيانات منطقيًا وتسهيل قراءة الملف أو طباعته.

#### س 2: هل يمكنني استخدام أوامر طباعة الصفحة الأخرى مع Aspose.Cells for .NET؟

نعم ، يدعم Aspose.Cells for .NET أوامر طباعة صفحات متعددة مثل "DownThenOver" و "OverThenOver" و "DownThenOverThenDownAgain" وما إلى ذلك. يمكنك اختيار أفضل ما يناسب احتياجاتك.

#### Q3: هل يمكنني تعيين خيارات إضافية لطباعة الصفحات باستخدام Aspose.Cells for .NET؟

نعم ، يمكنك تعيين خيارات متنوعة لطباعة الصفحات مثل المقياس والاتجاه والهوامش وما إلى ذلك ، باستخدام خصائص كائن PageSetup في Aspose.Cells for .NET.

#### س 4: هل يدعم Aspose.Cells for .NET تنسيقات ملفات Excel الأخرى؟

نعم ، يدعم Aspose.Cells for .NET مجموعة كبيرة من تنسيقات ملفات Excel مثل XLSX و XLS و CSV و HTML و PDF وما إلى ذلك. يمكنك التحويل بسهولة بين هذه التنسيقات باستخدام الميزات التي توفرها المكتبة.