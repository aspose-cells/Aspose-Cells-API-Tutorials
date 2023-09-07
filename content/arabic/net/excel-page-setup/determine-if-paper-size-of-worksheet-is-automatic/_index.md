---
title: حدد ما إذا كان حجم ورقة ورقة العمل تلقائيًا
linktitle: حدد ما إذا كان حجم ورقة ورقة العمل تلقائيًا
second_title: Aspose.Cells لمرجع .NET API
description: تعرف على كيفية تحديد ما إذا كان حجم ورق جدول البيانات تلقائيًا باستخدام Aspose.Cells for .NET.
type: docs
weight: 20
url: /ar/net/excel-page-setup/determine-if-paper-size-of-worksheet-is-automatic/
---
في هذه المقالة ، سوف نأخذك خطوة بخطوة لشرح التعليمات البرمجية المصدر C # التالية: تحديد ما إذا كان حجم ورقة ورقة العمل تلقائيًا باستخدام Aspose.Cells for .NET. سنستخدم مكتبة Aspose.Cells لـ .NET لإجراء هذه العملية. اتبع الخطوات أدناه لتحديد ما إذا كان حجم ورقة ورقة العمل تلقائيًا.

## الخطوة 1: تحميل المصنفات
الخطوة الأولى هي تحميل المصنفات. سيكون لدينا مصنفان: أحدهما معطل تلقائيًا لحجم الورق والآخر مع تمكين حجم الورق التلقائي. هذا هو الكود لتحميل المصنفات:

```csharp
// دليل المصدر
string sourceDir = "YOUR_SOURCE_DIR";
// دليل الإخراج
string outputDir = "YOUR_OUTPUT_DIRECTORY";

// قم بتحميل أول مصنف مع تعطيل حجم الورق التلقائي
Workbook wb1 = new Workbook(sourceDir + "samplePageSetupIsAutomaticPaperSize-False.xlsx");

// تحميل المصنف الثاني مع تمكين حجم الورق التلقائي
Workbook wb2 = new Workbook(sourceDir + "samplePageSetupIsAutomaticPaperSize-True.xlsx");
```

## الخطوة 2: الوصول إلى جداول البيانات
الآن بعد أن قمنا بتحميل المصنفات ، نحتاج إلى الوصول إلى أوراق العمل حتى نتمكن من التحقق من حجم الورق التلقائي. سننتقل إلى ورقة العمل الأولى من المصنفين. ها هو الكود للوصول إليه:

```csharp
//انتقل إلى ورقة العمل الأولى من المصنف الأول
Worksheet ws11 = wb1.Worksheets[0];

// انتقل إلى ورقة العمل الأولى من المصنف الثاني
Worksheet ws12 = wb2.Worksheets[0];
```

## الخطوة 3: تحقق من حجم الورق التلقائي
 في هذه الخطوة ، سوف نتحقق مما إذا كان حجم ورقة العمل تلقائيًا. سوف نستخدم ملف`PageSetup.IsAutomaticPaperSize` خاصية الحصول على هذه المعلومات. ثم سنعرض النتيجة. هذا هو الكود الخاص بذلك:

```csharp
// اعرض خاصية IsAutomaticPaperSize لورقة العمل الأولى في المصنف الأول
Console.WriteLine("First worksheet in first workbook - IsAutomaticPaperSize: " + ws11.PageSetup.IsAutomaticPaperSize);

// اعرض خاصية IsAutomaticPaperSize لورقة العمل الأولى في المصنف الثاني
Console.WriteLine("First worksheet of second workbook - IsAutomaticPaperSize: " + ws12.PageSetup.IsAutomaticPaperSize);

```

### نموذج التعليمات البرمجية المصدر لتحديد ما إذا كان حجم ورقة ورقة العمل تلقائيًا باستخدام Aspose.Cells لـ .NET 
```csharp
//دليل المصدر
string sourceDir = "YOUR_SOURCE_DIRECTORY";
//دليل الإخراج
string outputDir = "YOUR_OUTPUT_DIRECTORY";
//قم بتحميل أول مصنف يحتوي على خطأ تلقائي في حجم الورق
Workbook wb1 = new Workbook(sourceDir + "samplePageSetupIsAutomaticPaperSize-False.xlsx");
//قم بتحميل المصنف الثاني الذي يحتوي على حجم ورق تلقائي صحيح
Workbook wb2 = new Workbook(sourceDir + "samplePageSetupIsAutomaticPaperSize-True.xlsx");
//الوصول إلى ورقة العمل الأولى لكلا المصنفين
Worksheet ws11 = wb1.Worksheets[0];
Worksheet ws12 = wb2.Worksheets[0];
//اطبع خاصية PageSetup.IsAutomaticPaperSize لكلتا ورقتي العمل
Console.WriteLine("First Worksheet of First Workbook - IsAutomaticPaperSize: " + ws11.PageSetup.IsAutomaticPaperSize);
Console.WriteLine("First Worksheet of Second Workbook - IsAutomaticPaperSize: " + ws12.PageSetup.IsAutomaticPaperSize);
Console.WriteLine();
Console.WriteLine("DetermineIfPaperSizeOfWorksheetIsAutomatic executed successfully.\r\n");
```


## خاتمة
في هذه المقالة ، تعلمنا كيفية تحديد ما إذا كان حجم ورقة ورقة العمل تلقائيًا باستخدام Aspose.Cells لـ .NET. لقد اتبعنا الخطوات التالية: تحميل المصنفات ،

الوصول إلى جداول البيانات والتحقق التلقائي من حجم الورق. يمكنك الآن استخدام هذه المعرفة لتحديد ما إذا كان حجم الورق في جداول البيانات الخاصة بك تلقائيًا.

### أسئلة وأجوبة

#### س: كيف يمكنني تحميل المصنفات باستخدام Aspose.Cells for .NET؟

ج: يمكنك تحميل المصنفات باستخدام فئة المصنف من مكتبة Aspose.Cells. استخدم طريقة Workbook.Load لتحميل مصنف من ملف.

#### س: هل يمكنني التحقق من حجم الورق التلقائي لجداول البيانات الأخرى؟

ج: نعم ، يمكنك التحقق من حجم الورق التلقائي لأي ورقة عمل عن طريق الوصول إلى خاصية PageSetup.IsAutomaticPaperSize الخاصة بكائن ورقة العمل المقابل.

#### س: كيف يمكنني تغيير حجم الورق التلقائي لجدول بيانات؟

ج: لتغيير حجم الورق التلقائي لورقة العمل ، يمكنك استخدام خاصية PageSetup.IsAutomaticPaperSize وضبطها على القيمة المطلوبة (صواب أو خطأ).

#### س: ما هي الميزات الأخرى التي تقدمها Aspose.Cells for .NET؟

ج: يوفر Aspose.Cells for .NET العديد من الميزات للعمل مع جداول البيانات ، مثل إنشاء المصنفات وتعديلها وتحويلها ، بالإضافة إلى معالجة البيانات والصيغ والتنسيق.