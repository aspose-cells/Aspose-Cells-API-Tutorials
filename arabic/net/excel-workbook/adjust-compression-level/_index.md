---
title: ضبط مستوى الضغط
linktitle: ضبط مستوى الضغط
second_title: Aspose.Cells لمرجع .NET API
description: قم بتقليل حجم مصنفات Excel الخاصة بك عن طريق ضبط مستوى الضغط باستخدام Aspose.Cells for .NET.
type: docs
weight: 50
url: /ar/net/excel-workbook/adjust-compression-level/
---
في هذا البرنامج التعليمي خطوة بخطوة ، سنشرح كود المصدر C # المقدم والذي سيسمح لك بضبط مستوى الضغط باستخدام Aspose.Cells for .NET. اتبع الخطوات أدناه لضبط مستوى الضغط في مصنف Excel.

## الخطوة 1: تعيين أدلة المصدر والمخرجات

```csharp
// دليل المصدر
string sourceDir = RunExamples.Get_SourceDirectory();
// دليل الإخراج
string outDir = RunExamples.Get_OutputDirectory();
```

في هذه الخطوة الأولى ، نحدد مجلدات المصدر والمخرجات لملفات Excel.

## الخطوة 2: تحميل مصنف Excel

```csharp
//قم بتحميل مصنف Excel
Workbook workbook = new Workbook(sourceDir + "LargeSampleFile.xlsx");
```

 نقوم بتحميل مصنف Excel من الملف المحدد باستخدام امتداد`Workbook` فئة من Aspose.Cells.

## الخطوة 3: تعيين خيارات النسخ الاحتياطي

```csharp
// تحديد خيارات النسخ الاحتياطي
XlsbSaveOptions options = new XlsbSaveOptions();
```

 نقوم بإنشاء مثيل لـ`XlsbSaveOptions` فئة لتعيين خيارات الحفظ.

## الخطوة 4: ضبط مستوى الضغط (المستوى 1)

```csharp
// ضبط مستوى الضغط (المستوى 1)
options.CompressionType = OoxmlCompressionType.Level1;
var watch = System.Diagnostics.Stopwatch.StartNew();
workbook.Save(outDir + "LargeSampleFile_level_1_out.xlsb", options);
watch.Stop();
let elapsedMs = watch.ElapsedMilliseconds;
Console.WriteLine("Elapsed time (Level 1): " + elapsedMs);
```

 نقوم بضبط مستوى الضغط عن طريق الضبط`CompressionType` ل`Level1`. ثم نقوم بحفظ مصنف Excel مع تحديد خيار الضغط هذا.

## الخطوة 5: ضبط مستوى الضغط (المستوى 6)

```csharp
// ضبط مستوى الضغط (المستوى 6)
options.CompressionType = OoxmlCompressionType.Level6;
watch = System.Diagnostics.Stopwatch.StartNew();
workbook.Save(outDir + "LargeSampleFile_level_6_out.xlsb", options);
watch.Stop();
elapsedMs = watch. ElapsedMilliseconds;
Console.WriteLine("Elapsed time (Level 6): " + elapsedMs);
```

 نكرر العملية لضبط مستوى الضغط على`Level6` وحفظ مصنف Excel باستخدام هذا الخيار.

## الخطوة 6: ضبط مستوى الضغط (المستوى 9)

```csharp
// ضبط مستوى الضغط (المستوى 9)
options.CompressionType = OoxmlCompressionType.Level9;
watch = System.Diagnostics.Stopwatch.StartNew();
workbook.Save(outDir + "LargeSampleFile_level_9_out.xlsb", options);
watch.Stop();
elapsedMs = watch. ElapsedMilliseconds;
Console.WriteLine("Elapsed time (Level 9): " + elapsedMs);
```

 نكرر العملية مرة أخيرة لضبط مستوى الضغط إلى`Level9` وحفظ مصنف Excel باستخدام هذا الخيار.

### نموذج التعليمات البرمجية المصدر لضبط مستوى الضغط باستخدام Aspose.Cells for .NET 
```csharp
//دليل المصدر
string sourceDir = RunExamples.Get_SourceDirectory();
string outDir = RunExamples.Get_OutputDirectory();
Workbook workbook = new Workbook(sourceDir + "LargeSampleFile.xlsx");
XlsbSaveOptions options = new XlsbSaveOptions();
options.CompressionType = OoxmlCompressionType.Level1;
var watch = System.Diagnostics.Stopwatch.StartNew();
workbook.Save(outDir + "LargeSampleFile_level_1_out.xlsb", options);
watch.Stop();
var elapsedMs = watch.ElapsedMilliseconds;
Console.WriteLine("Level 1 Elapsed Time: " + elapsedMs);
watch = System.Diagnostics.Stopwatch.StartNew();
options.CompressionType = OoxmlCompressionType.Level6;
workbook.Save(outDir + "LargeSampleFile_level_6_out.xlsb", options);
watch.Stop();
elapsedMs = watch.ElapsedMilliseconds;
Console.WriteLine("Level 6 Elapsed Time: " + elapsedMs);
watch = System.Diagnostics.Stopwatch.StartNew();
options.CompressionType = OoxmlCompressionType.Level9;
workbook.Save(outDir + "LargeSampleFile_level_9_out.xlsb", options);
watch.Stop();
elapsedMs = watch.ElapsedMilliseconds;
Console.WriteLine("Level 9 Elapsed Time: " + elapsedMs);
Console.WriteLine("AdjustCompressionLevel executed successfully.");
```

## خاتمة

تهنئة ! لقد تعلمت كيفية ضبط مستوى الضغط في مصنف Excel باستخدام Aspose.Cells لـ .NET. جرب مستويات مختلفة من الضغط للعثور على المستوى الذي يناسب احتياجاتك.

### أسئلة وأجوبة

#### س: ما هو الضغط في مصنف Excel؟

ج: الضغط في مصنف Excel هو عملية لتقليل حجم الملف باستخدام خوارزميات الضغط. يؤدي ذلك إلى تقليل مساحة التخزين المطلوبة وتحسين الأداء عند تحميل الملف ومعالجته.

#### س: ما هي مستويات الضغط المتوفرة مع Aspose.Cells؟

ج: باستخدام Aspose.Cells ، يمكنك ضبط مستوى الضغط من 1 إلى 9. وكلما زاد مستوى الضغط ، كان حجم الملف أصغر ، ولكن يمكنه أيضًا زيادة وقت المعالجة.

#### س: كيف أختار مستوى الضغط المناسب لمصنف Excel الخاص بي؟

ج: يعتمد اختيار مستوى الضغط على احتياجاتك الخاصة. إذا كنت تريد أقصى ضغط ولا يمثل وقت المعالجة مشكلة ، يمكنك الانتقال إلى المستوى 9. إذا كنت تفضل حل وسط بين حجم الملف ووقت المعالجة ، فيمكنك اختيار مستوى متوسط.

#### س: هل يؤثر الضغط على جودة البيانات في مصنف Excel؟

ج: لا ، لا يؤثر الضغط على جودة البيانات في مصنف Excel. إنه ببساطة يقلل من حجم الملف باستخدام تقنيات الضغط دون تغيير البيانات نفسها.

#### س: هل يمكنني ضبط مستوى الضغط بعد حفظ ملف Excel؟

ج: لا ، بمجرد حفظ ملف Excel بمستوى ضغط معين ، لا يمكنك ضبط مستوى الضغط لاحقًا. ستحتاج إلى حفظ الملف مرة أخرى بمستوى الضغط الجديد إذا كنت ترغب في تعديله.