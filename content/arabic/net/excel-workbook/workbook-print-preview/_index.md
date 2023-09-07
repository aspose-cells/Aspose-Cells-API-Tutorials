---
title: معاينة طباعة المصنف
linktitle: معاينة طباعة المصنف
second_title: Aspose.Cells لمرجع .NET API
description: تعرف على كيفية إنشاء معاينة قبل الطباعة لمصنف باستخدام Aspose.Cells for .NET.
type: docs
weight: 170
url: /ar/net/excel-workbook/workbook-print-preview/
---
تعد معاينة الطباعة لمصنف عمل ميزة أساسية عند العمل مع ملفات Excel باستخدام Aspose.Cells for .NET. يمكنك بسهولة إنشاء معاينة قبل الطباعة باتباع الخطوات التالية:

## الخطوة 1: حدد دليل المصدر

أولاً ، تحتاج إلى تحديد الدليل المصدر حيث يوجد ملف Excel الذي تريد معاينته. هيريس كيفية القيام بذلك:

```csharp
// دليل المصدر
string sourceDir = RunExamples.Get_SourceDirectory();
```

## الخطوة 2: قم بتحميل المصنف

ثم تحتاج إلى تحميل مصنف المصنف من ملف Excel المحدد. هيريس كيفية القيام بذلك:

```csharp
// قم بتحميل مصنف المصنف
Workbook workbook = new Workbook(sourceDir + "Book1.xlsx");
```

## الخطوة 3: تكوين خيارات الصورة والطباعة

قبل إنشاء معاينة الطباعة ، يمكنك تكوين خيارات الصورة والطباعة حسب الحاجة. في هذا المثال ، نستخدم الخيارات الافتراضية. هيريس كيفية القيام بذلك:

```csharp
// خيارات الصورة والطباعة
ImageOrPrintOptions imgOptions = new ImageOrPrintOptions();
```

## الخطوة 4: قم بإنشاء معاينة قبل الطباعة للمصنف

يمكنك الآن إنشاء معاينة الطباعة لمصنف المصنف باستخدام فئة WorkbookPrintingPreview. هيريس كيفية القيام بذلك:

```csharp
// معاينة قبل الطباعة للمصنف
WorkbookPrintingPreview preview = new WorkbookPrintingPreview(workbook, imgOptions);
Console.WriteLine("Workbook page count: " + preview.EvaluatedPageCount);
```

## الخطوة 5: قم بإنشاء معاينة قبل الطباعة لورقة العمل

إذا كنت ترغب في إنشاء معاينة الطباعة لورقة عمل معينة ، يمكنك استخدام فئة SheetPrintingPreview. هنا مثال :

```csharp
// معاينة قبل طباعة ورقة العمل
SheetPrintingPreview preview2 = new SheetPrintingPreview(workbook.Worksheets[0], imgOptions);
Console.WriteLine("Number of worksheet pages: " + preview2.EvaluatedPageCount);
```

### نموذج التعليمات البرمجية المصدر لـ Workbook Print Preview باستخدام Aspose.Cells for .NET 
```csharp
//دليل المصدر
string sourceDir = RunExamples.Get_SourceDirectory();
Workbook workbook = new Workbook(sourceDir + "Book1.xlsx");
ImageOrPrintOptions imgOptions = new ImageOrPrintOptions();
WorkbookPrintingPreview preview = new WorkbookPrintingPreview(workbook, imgOptions);
Console.WriteLine("Workbook page count: " + preview.EvaluatedPageCount);
SheetPrintingPreview preview2 = new SheetPrintingPreview(workbook.Worksheets[0], imgOptions);
Console.WriteLine("Worksheet page count: " + preview2.EvaluatedPageCount);
Console.WriteLine("PrintPreview executed successfully.");
```

## خاتمة

يعد إنشاء معاينة قبل الطباعة لأحد المصنفات ميزة قوية تقدمها Aspose.Cells لـ .NET. باتباع الخطوات المذكورة أعلاه ، يمكنك بسهولة معاينة مصنف Excel والحصول على معلومات حول عدد الصفحات المطلوب طباعتها.

### أسئلة وأجوبة

#### س: كيف يمكنني تحديد دليل مصدر مختلف لتحميل المصنف الخاص بي؟
    
 ج: يمكنك استخدام ملف`Set_SourceDirectory` طريقة لتحديد دليل مصدر مختلف. على سبيل المثال:`RunExamples.Set_SourceDirectory("Path_to_the_source_directory")`.

#### س: هل يمكنني تخصيص الصورة وخيارات الطباعة عند إنشاء معاينة قبل الطباعة؟
    
 ج: نعم ، يمكنك تخصيص خيارات الصورة والطباعة عن طريق تغيير خصائص ملف`ImageOrPrintOptions` هدف. على سبيل المثال ، يمكنك ضبط دقة الصورة وتنسيق ملف الإخراج وما إلى ذلك.

#### س: هل من الممكن إنشاء معاينة قبل الطباعة لعدة أوراق عمل في مصنف؟
    
ج: نعم ، يمكنك التكرار عبر أوراق العمل المختلفة في المصنف وإنشاء معاينة قبل الطباعة لكل ورقة باستخدام`SheetPrintingPreview` فصل.

#### س: كيف أحفظ معاينة الطباعة كصورة أو ملف PDF؟
    
 ج: يمكنك استخدام ملفات`ToImage` أو`ToPdf` طريقة`WorkbookPrintingPreview` أو`SheetPrintingPreview` كائن لحفظ معاينة الطباعة كصورة أو ملف PDF.

#### س: ماذا يمكنني أن أفعل بمعاينة الطباعة بمجرد إنشائها؟
    
ج: بمجرد إنشاء معاينة الطباعة ، يمكنك عرضها على الشاشة أو حفظها كصورة أو ملف PDF أو استخدامها لعمليات أخرى مثل الإرسال بالبريد الإلكتروني أو الطباعة.
	