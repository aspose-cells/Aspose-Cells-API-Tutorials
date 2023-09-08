---
title: ضبط ترتيب صفحات Excel
linktitle: ضبط ترتيب صفحات Excel
second_title: Aspose.Cells لمرجع .NET API
description: دليل خطوة بخطوة لتعيين ترتيب الصفحات في Excel باستخدام Aspose.Cells لـ .NET. تم تضمين تعليمات مفصلة وكود المصدر.
type: docs
weight: 120
url: /ar/net/excel-page-setup/set-excel-page-order/
---
في هذه المقالة، سنرشدك خطوة بخطوة لشرح كود مصدر C# التالي لتعيين ترتيب صفحات Excel باستخدام Aspose.Cells لـ .NET. سنوضح لك كيفية إعداد دليل المستندات، وإنشاء كائن مصنف، والحصول على مرجع PageSetup، وتعيين ترتيب طباعة الصفحة، وحفظ المصنف.

## الخطوة 1: إعداد دليل المستندات

 قبل البدء، تحتاج إلى تكوين دليل المستند حيث تريد حفظ ملف Excel. يمكنك تحديد مسار الدليل عن طريق استبدال قيمة الملف`dataDir` متغير مع المسار الخاص بك.

```csharp
//المسار إلى دليل المستندات.
string dataDir = "YOUR_DIRECTORY_OF_DOCUMENTS";
```

## الخطوة 2: إنشاء مثيل لكائن المصنف

الخطوة الأولى هي إنشاء كائن مصنف. يمثل هذا مصنف Excel الذي سنعمل معه.

```csharp
// إنشاء مثيل لكائن المصنف
Workbook workbook = new Workbook();
```

## الخطوة 3: الحصول على مرجع PageSetup

بعد ذلك، نحتاج إلى الحصول على مرجع كائن PageSetup لورقة العمل التي نريد ضبط ترتيب الصفحات عليها.

```csharp
// الحصول على مرجع PageSetup لورقة العمل
PageSetup pageSetup = workbook.Worksheets[0].PageSetup;
```

## الخطوة 4: تحديد ترتيب طباعة الصفحات

الآن يمكننا ضبط ترتيب طباعة الصفحات. في هذا المثال، نستخدم خيار "OverThenDown"، مما يعني أنه سيتم طباعة الصفحات من اليسار إلى اليمين، ثم من الأعلى إلى الأسفل.

```csharp
// اضبط ترتيب طباعة الصفحة على "OverThenDown"
pageSetup.Order = PrintOrderType.OverThenDown;
```

## الخطوة 5: حفظ المصنف

وأخيرا، نقوم بحفظ مصنف Excel مع تغييرات ترتيب الصفحات.

```csharp
// احفظ المصنف
workbook.Save(dataDir + "SetPageOrder_out.xls");
```

### نموذج التعليمات البرمجية المصدر لـ Set Excel Page Order باستخدام Aspose.Cells لـ .NET 
```csharp
//المسار إلى دليل المستندات.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// إنشاء مثيل لكائن المصنف
Workbook workbook = new Workbook();
// الحصول على مرجع PageSetup لورقة العمل
PageSetup pageSetup = workbook.Worksheets[0].PageSetup;
// ضبط ترتيب طباعة الصفحات إلى أعلى ثم إلى أسفل
pageSetup.Order = PrintOrderType.OverThenDown;
// احفظ المصنف.
workbook.Save(dataDir + "SetPageOrder_out.xls");
```

## خاتمة

في هذا البرنامج التعليمي، شرحنا كيفية ضبط ترتيب الصفحات في ملف Excel باستخدام Aspose.Cells لـ .NET. باتباع الخطوات المتوفرة، يمكنك بسهولة تكوين دليل المستند، وإنشاء كائن مصنف، والحصول على مرجع PageSetup، وتعيين ترتيب طباعة الصفحة، وحفظ المصنف.

### الأسئلة الشائعة

#### س1: ما سبب أهمية تعيين ترتيب الصفحات في ملف Excel؟

يعد تحديد ترتيب الصفحات في ملف Excel أمرًا مهمًا لأنه يحدد كيفية طباعة الصفحات أو عرضها. ومن خلال تحديد ترتيب معين، يمكنك تنظيم البيانات بشكل منطقي وتسهيل قراءة الملف أو طباعته.

#### س2: هل يمكنني استخدام أوامر طباعة صفحات أخرى مع Aspose.Cells لـ .NET؟

نعم، يدعم Aspose.Cells for .NET أوامر طباعة صفحات متعددة مثل "DownThenOver"، و"OverThenDown"، و"DownThenOverThenDownAgain"، وما إلى ذلك. ويمكنك اختيار الخيار الذي يناسب احتياجاتك.

#### س3: هل يمكنني تعيين خيارات إضافية لطباعة الصفحات باستخدام Aspose.Cells لـ .NET؟

نعم، يمكنك تعيين خيارات مختلفة لطباعة الصفحة مثل المقياس والاتجاه والهوامش وما إلى ذلك، باستخدام خصائص كائن PageSetup في Aspose.Cells لـ .NET.

#### س 4: هل يدعم Aspose.Cells for .NET تنسيقات ملفات Excel الأخرى؟

نعم، يدعم Aspose.Cells for .NET نطاقًا واسعًا من تنسيقات ملفات Excel مثل XLSX، وXLS، وCSV، وHTML، وPDF، وما إلى ذلك. ويمكنك التحويل بسهولة بين هذه التنسيقات باستخدام الميزات التي توفرها المكتبة.