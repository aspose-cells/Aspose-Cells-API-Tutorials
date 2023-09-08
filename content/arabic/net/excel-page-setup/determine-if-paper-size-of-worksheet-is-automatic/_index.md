---
title: تحديد ما إذا كان حجم ورق ورقة العمل تلقائيًا
linktitle: تحديد ما إذا كان حجم ورق ورقة العمل تلقائيًا
second_title: Aspose.Cells لمرجع .NET API
description: تعرف على كيفية تحديد ما إذا كان حجم ورق جدول البيانات تلقائيًا باستخدام Aspose.Cells لـ .NET.
type: docs
weight: 20
url: /ar/net/excel-page-setup/determine-if-paper-size-of-worksheet-is-automatic/
---
في هذه المقالة، سنأخذك خطوة بخطوة لشرح التعليمات البرمجية المصدر لـ C# التالية: تحديد ما إذا كان حجم ورق ورقة العمل تلقائيًا باستخدام Aspose.Cells لـ .NET. سوف نستخدم مكتبة Aspose.Cells لـ .NET لإجراء هذه العملية. اتبع الخطوات الموضحة أدناه لتحديد ما إذا كان حجم ورق ورقة العمل تلقائيًا.

## الخطوة 1: تحميل المصنفات
الخطوة الأولى هي تحميل المصنفات. سيكون لدينا مصنفين: أحدهما مع تعطيل حجم الورق التلقائي والآخر مع تمكين حجم الورق التلقائي. وهذا هو الكود لتحميل المصنفات:

```csharp
// دليل المصدر
string sourceDir = "YOUR_SOURCE_DIR";
// دليل الإخراج
string outputDir = "YOUR_OUTPUT_DIRECTORY";

// قم بتحميل المصنف الأول مع تعطيل حجم الورق التلقائي
Workbook wb1 = new Workbook(sourceDir + "samplePageSetupIsAutomaticPaperSize-False.xlsx");

// قم بتحميل المصنف الثاني مع تمكين حجم الورق التلقائي
Workbook wb2 = new Workbook(sourceDir + "samplePageSetupIsAutomaticPaperSize-True.xlsx");
```

## الخطوة 2: الوصول إلى جداول البيانات
الآن بعد أن قمنا بتحميل المصنفات، نحتاج إلى الوصول إلى أوراق العمل حتى نتمكن من التحقق من حجم الورق التلقائي. سوف نذهب إلى ورقة العمل الأولى من المصنفين. إليك الرمز للوصول إليه:

```csharp
//انتقل إلى ورقة العمل الأولى من المصنف الأول
Worksheet ws11 = wb1.Worksheets[0];

// انتقل إلى ورقة العمل الأولى من المصنف الثاني
Worksheet ws12 = wb2.Worksheets[0];
```

## الخطوة 3: التحقق من حجم الورق التلقائي
 في هذه الخطوة، سوف نتحقق مما إذا كان حجم ورق ورقة العمل تلقائيًا. سوف نستخدم`PageSetup.IsAutomaticPaperSize` الخاصية للحصول على هذه المعلومات. وسوف نقوم بعد ذلك بعرض النتيجة. هنا هو الرمز لذلك:

```csharp
// عرض الخاصية IsAutomaticPaperSize لورقة العمل الأولى في المصنف الأول
Console.WriteLine("First worksheet in first workbook - IsAutomaticPaperSize: " + ws11.PageSetup.IsAutomaticPaperSize);

// عرض الخاصية IsAutomaticPaperSize لورقة العمل الأولى في المصنف الثاني
Console.WriteLine("First worksheet of second workbook - IsAutomaticPaperSize: " + ws12.PageSetup.IsAutomaticPaperSize);

```

### نموذج التعليمات البرمجية المصدر لتحديد ما إذا كان حجم ورق ورقة العمل تلقائيًا باستخدام Aspose.Cells لـ .NET 
```csharp
//دليل المصدر
string sourceDir = "YOUR_SOURCE_DIRECTORY";
//دليل الإخراج
string outputDir = "YOUR_OUTPUT_DIRECTORY";
//قم بتحميل المصنف الأول الذي يحتوي على حجم ورق تلقائي خطأ
Workbook wb1 = new Workbook(sourceDir + "samplePageSetupIsAutomaticPaperSize-False.xlsx");
//قم بتحميل المصنف الثاني بحجم ورق تلقائي صحيح
Workbook wb2 = new Workbook(sourceDir + "samplePageSetupIsAutomaticPaperSize-True.xlsx");
//الوصول إلى ورقة العمل الأولى لكلا المصنفين
Worksheet ws11 = wb1.Worksheets[0];
Worksheet ws12 = wb2.Worksheets[0];
//طباعة الخاصية PageSetup.IsAutomaticPaperSize لكلا ورقتي العمل
Console.WriteLine("First Worksheet of First Workbook - IsAutomaticPaperSize: " + ws11.PageSetup.IsAutomaticPaperSize);
Console.WriteLine("First Worksheet of Second Workbook - IsAutomaticPaperSize: " + ws12.PageSetup.IsAutomaticPaperSize);
Console.WriteLine();
Console.WriteLine("DetermineIfPaperSizeOfWorksheetIsAutomatic executed successfully.\r\n");
```


## خاتمة
في هذه المقالة، تعلمنا كيفية تحديد ما إذا كان حجم ورق ورقة العمل تلقائيًا باستخدام Aspose.Cells لـ .NET. اتبعنا الخطوات التالية: تحميل المصنفات،

الوصول إلى جداول البيانات والتحقق التلقائي من حجم الورق. يمكنك الآن استخدام هذه المعرفة لتحديد ما إذا كان حجم ورق جداول البيانات لديك تلقائيًا أم لا.

### الأسئلة الشائعة

#### س: كيف يمكنني تحميل المصنفات باستخدام Aspose.Cells لـ .NET؟

ج: يمكنك تحميل المصنفات باستخدام فئة Workbook من مكتبة Aspose.Cells. استخدم الأسلوب Workbook.Load لتحميل مصنف من ملف.

#### س: هل يمكنني التحقق من حجم الورق التلقائي لجداول البيانات الأخرى؟

ج: نعم، يمكنك التحقق من حجم الورق التلقائي لأي ورقة عمل عن طريق الوصول إلى خاصية PageSetup.IsAutomaticPaperSize لكائن ورقة العمل المقابل.

#### س: كيف يمكنني تغيير حجم الورق التلقائي لجدول البيانات؟

ج: لتغيير حجم الورق التلقائي لورقة العمل، يمكنك استخدام الخاصية PageSetup.IsAutomaticPaperSize وتعيينها إلى القيمة المطلوبة (صواب أو خطأ).

#### س: ما هي الميزات الأخرى التي يقدمها Aspose.Cells لـ .NET؟

ج: يقدم Aspose.Cells for .NET العديد من الميزات للعمل مع جداول البيانات، مثل إنشاء المصنفات وتعديلها وتحويلها، بالإضافة إلى معالجة البيانات والصيغ والتنسيقات.