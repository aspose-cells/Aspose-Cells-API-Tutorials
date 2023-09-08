---
title: معاينة طباعة المصنف
linktitle: معاينة طباعة المصنف
second_title: Aspose.Cells لمرجع .NET API
description: تعرف على كيفية إنشاء معاينة قبل الطباعة لمصنف باستخدام Aspose.Cells لـ .NET.
type: docs
weight: 170
url: /ar/net/excel-workbook/workbook-print-preview/
---
تعد معاينة الطباعة للمصنف ميزة أساسية عند العمل مع ملفات Excel باستخدام Aspose.Cells لـ .NET. يمكنك بسهولة إنشاء معاينة قبل الطباعة باتباع الخطوات التالية:

## الخطوة 1: تحديد الدليل المصدر

أولاً، تحتاج إلى تحديد الدليل المصدر الذي يوجد به ملف Excel الذي تريد معاينته. هيريس كيفية القيام بذلك:

```csharp
// دليل المصدر
string sourceDir = RunExamples.Get_SourceDirectory();
```

## الخطوة 2: تحميل المصنف

فأنت بحاجة إلى تحميل المصنف Workbook من ملف Excel المحدد. هيريس كيفية القيام بذلك:

```csharp
// قم بتحميل المصنف المصنف
Workbook workbook = new Workbook(sourceDir + "Book1.xlsx");
```

## الخطوة 3: تكوين خيارات الصورة والطباعة

قبل إنشاء معاينة الطباعة، يمكنك تكوين خيارات الصورة والطباعة حسب الحاجة. في هذا المثال، نستخدم الخيارات الافتراضية. هيريس كيفية القيام بذلك:

```csharp
// خيارات الصورة والطباعة
ImageOrPrintOptions imgOptions = new ImageOrPrintOptions();
```

## الخطوة 4: إنشاء معاينة الطباعة للمصنف

يمكنك الآن إنشاء معاينة الطباعة لمصنف المصنف باستخدام فئة WorkbookPrintingPreview. هيريس كيفية القيام بذلك:

```csharp
// معاينة الطباعة للمصنف
WorkbookPrintingPreview preview = new WorkbookPrintingPreview(workbook, imgOptions);
Console.WriteLine("Workbook page count: " + preview.EvaluatedPageCount);
```

## الخطوة 5: إنشاء معاينة الطباعة لورقة العمل

إذا كنت تريد إنشاء معاينة الطباعة لورقة عمل معينة، فيمكنك استخدام فئة SheetPrintingPreview. هنا مثال :

```csharp
// معاينة طباعة ورقة العمل
SheetPrintingPreview preview2 = new SheetPrintingPreview(workbook.Worksheets[0], imgOptions);
Console.WriteLine("Number of worksheet pages: " + preview2.EvaluatedPageCount);
```

### نموذج التعليمات البرمجية المصدر لمعاينة طباعة المصنف باستخدام Aspose.Cells لـ .NET 
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

يعد إنشاء معاينة الطباعة للمصنف ميزة قوية تقدمها Aspose.Cells لـ .NET. باتباع الخطوات المذكورة أعلاه، يمكنك بسهولة معاينة مصنف Excel الخاص بك والحصول على معلومات حول عدد الصفحات المطلوب طباعتها.

### الأسئلة الشائعة

#### س: كيف يمكنني تحديد دليل مصدر مختلف لتحميل المصنف الخاص بي؟
    
 ج: يمكنك استخدام`Set_SourceDirectory` طريقة لتحديد دليل مصدر مختلف. على سبيل المثال:`RunExamples.Set_SourceDirectory("Path_to_the_source_directory")`.

#### س: هل يمكنني تخصيص خيارات الصورة والطباعة عند إنشاء معاينة الطباعة؟
    
 ج: نعم، يمكنك تخصيص خيارات الصورة والطباعة عن طريق تغيير خصائص الملف`ImageOrPrintOptions` هدف. على سبيل المثال، يمكنك ضبط دقة الصورة، وتنسيق ملف الإخراج، وما إلى ذلك.

#### س: هل من الممكن إنشاء معاينة قبل الطباعة لأوراق عمل متعددة في مصنف؟
    
ج: نعم، يمكنك تكرار أوراق العمل المختلفة في المصنف وإنشاء معاينة طباعة لكل ورقة باستخدام`SheetPrintingPreview` فصل.

#### س: كيف يمكنني حفظ معاينة الطباعة كصورة أو ملف PDF؟
    
 ج: يمكنك استخدام`ToImage` أو`ToPdf` طريقة`WorkbookPrintingPreview` أو`SheetPrintingPreview` كائن لحفظ معاينة الطباعة كصورة أو ملف PDF.

#### س: ماذا يمكنني أن أفعل بمعاينة الطباعة بمجرد إنشائها؟
    
ج: بمجرد إنشاء معاينة الطباعة، يمكنك عرضها على الشاشة، أو حفظها كصورة أو ملف PDF، أو استخدامها لعمليات أخرى مثل الإرسال عبر البريد الإلكتروني أو الطباعة.
	