---
title: استبدال Regex
linktitle: استبدال Regex
second_title: Aspose.Cells لمرجع .NET API
description: تعرف على كيفية إجراء استبدال Regex في ملفات Excel باستخدام Aspose.Cells for .NET.
type: docs
weight: 140
url: /ar/net/excel-workbook/regex-replace/
---
يعد استبدال النص بناءً على التعبيرات العادية (Regex) مهمة شائعة عند معالجة البيانات في ملفات Excel. باستخدام Aspose.Cells for .NET ، يمكنك بسهولة إجراء استبدال Regex باتباع الخطوات التالية:

## الخطوة 1: تحديد دليل المصدر ودليل الإخراج

بادئ ذي بدء ، يجب عليك تحديد الدليل المصدر حيث يوجد ملف Excel الذي يحتوي على البيانات المراد استبدالها ، بالإضافة إلى دليل الإخراج حيث تريد حفظ الملف المعدل. إليك كيفية القيام بذلك باستخدام Aspose.Cells:

```csharp
// دليل المصدر
string sourceDir = RunExamples.Get_SourceDirectory();

// دليل الإخراج
string outputDir = RunExamples.Get_OutputDirectory();
```

## الخطوة 2: قم بتحميل ملف Excel المصدر

بعد ذلك ، تحتاج إلى تحميل ملف Excel المصدر الذي تريد إجراء استبدال Regex عليه. هيريس كيفية القيام بذلك:

```csharp
// قم بتحميل ملف Excel المصدر
Workbook workbook = new Workbook(sourceDir + "SampleRegexReplace.xlsx");
```

## الخطوة 3: إجراء استبدال Regex

بعد تحميل الملف ، يمكنك تعيين خيارات الاستبدال ، بما في ذلك حساسية حالة الأحرف والمطابقة الدقيقة لمحتوى الخلية. إليك نموذج التعليمات البرمجية لإجراء استبدال Regex:

```csharp
// اضبط خيارات الاستبدال
ReplaceOptions replace = new ReplaceOptions();
replace.CaseSensitive = false;
replace.MatchEntireCellContents = false;

// حدد أن مفتاح البحث هو تعبير عادي
replace. RegexKey = true;

// قم بإجراء استبدال Regex
workbook. Replace("\\bKIM\\b", "^^^TIM^^^", replace);
```

## الخطوة 4: احفظ ملف Excel الناتج

بمجرد الانتهاء من استبدال Regex ، يمكنك حفظ ملف Excel المعدل في دليل الإخراج المحدد. هيريس كيفية القيام بذلك:

```csharp
// احفظ ملف Excel الناتج
workbook.Save(outputDir + "RegexReplace_out.xlsx");
Console.WriteLine("RegexReplace executed successfully.\r\n");
```

### نموذج التعليمات البرمجية المصدر لـ Regex Replace باستخدام Aspose.Cells for .NET 
```csharp
//دليل المصدر
string sourceDir = RunExamples.Get_SourceDirectory();
//دليل الإخراج
string outputDir = RunExamples.Get_OutputDirectory();
Workbook workbook = new Workbook(sourceDir + "SampleRegexReplace.xlsx");
ReplaceOptions replace = new ReplaceOptions();
replace.CaseSensitive = false;
replace.MatchEntireCellContents = false;
// اضبط على صواب للإشارة إلى أن المفتاح الذي تم البحث عنه هو regex
replace.RegexKey = true;
workbook.Replace("\\bKIM\\b", "^^^TIM^^^", replace);
workbook.Save(outputDir + "RegexReplace_out.xlsx");
Console.WriteLine("RegexReplace executed successfully.");
```

## خاتمة

يعد استبدال Regex أسلوبًا قويًا لتعديل البيانات ديناميكيًا في ملف Excel. باستخدام Aspose.Cells for .NET ، يمكنك بسهولة إجراء استبدال Regex باتباع الخطوات الموضحة أعلاه. جرب تعابيرك المعتادة واستفد من المرونة التي توفرها Aspose.Cells.

### أسئلة وأجوبة

#### س: ما هو استبدال Regex؟
    
ج: استبدال Regex هو أسلوب يستخدم لاستبدال أنماط النص بناءً على التعبيرات العادية في ملف Excel. هذا يسمح بإجراء تغييرات سريعة ودقيقة على البيانات.

#### س: هل استبدال Regex حساس لحالة الأحرف؟
    
ج: لا ، مع Aspose.Cells يمكنك تحديد ما إذا كان يجب أن يكون استبدال Regex حساسًا لحالة الأحرف أم لا. لديك سيطرة كاملة على هذه الميزة.

#### س: كيف يمكنني تحديد مطابقة تامة لمحتوى الخلية عند استبدال Regex؟
    
ج: Aspose.Cells يسمح لك بتحديد ما إذا كان يجب أن يتطابق استبدال Regex تمامًا مع محتوى الخلية أم لا. يمكنك ضبط هذا الخيار وفقًا لاحتياجاتك.

#### س: هل يمكنني استخدام التعبيرات النمطية المتقدمة عند استبدال Regex بـ Aspose.Cells؟
    
ج: نعم ، يدعم Aspose.Cells التعبيرات العادية المتقدمة ، مما يسمح لك بإجراء عمليات استبدال معقدة ومعقدة في ملفات Excel الخاصة بك.

#### س: كيف يمكنني التحقق من نجاح استبدال Regex؟
    
ج: بعد إجراء استبدال Regex ، يمكنك التحقق مما إذا كانت العملية ناجحة عن طريق التحقق من الإخراج والتأكد من إنشاء ملف Excel الناتج بشكل صحيح.
	