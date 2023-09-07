---
title: إنشاء مصنف مشترك
linktitle: إنشاء مصنف مشترك
second_title: Aspose.Cells لمرجع .NET API
description: قم بإنشاء مصنف Excel مشترك باستخدام Aspose.Cells for .NET لتمكين تعاون البيانات المتزامن.
type: docs
weight: 70
url: /ar/net/excel-workbook/create-shared-workbook/
---
في هذا البرنامج التعليمي ، سنرشدك عبر الكود المصدري C # المقدم والذي سيسمح لك بإنشاء مصنف مشترك باستخدام Aspose.Cells for .NET. اتبع الخطوات أدناه لإجراء هذه العملية.

## الخطوة 1: تعيين دليل الإخراج

```csharp
// دليل الإخراج
string outputDir = RunExamples.Get_OutputDirectory();
```

في هذه الخطوة الأولى ، نحدد دليل الإخراج حيث سيتم حفظ المصنف المشترك.

## الخطوة 2: إنشاء كائن مصنف

```csharp
// قم بإنشاء كائن مصنف
Workbook wb = new Workbook();
```

نحن بصدد إنشاء كائن مصنف جديد سيمثل مصنف Excel الخاص بنا.

## الخطوة 3: تمكين مشاركة المصنف

```csharp
// شارك المصنف
wb.Settings.Shared = true;
```

 نقوم بتمكين ميزة مشاركة المصنف عن طريق تعيين`Shared` الكائن في المصنف`true`.

## الخطوة 4: احفظ المصنف المشترك

```csharp
// احفظ المصنف المشترك
wb.Save(outputDir + "outputSharedWorkbook.xlsx");
```

نحفظ المصنف المشترك عن طريق تحديد مسار واسم ملف الإخراج.

### نموذج التعليمات البرمجية المصدر لـ Create Shared Workbook باستخدام Aspose.Cells for .NET 
```csharp
//دليل الإخراج
string outputDir = RunExamples.Get_OutputDirectory();
//إنشاء كائن المصنف
Workbook wb = new Workbook();
//شارك المصنف
wb.Settings.Shared = true;
//احفظ المصنف المشترك
wb.Save(outputDir + "outputSharedWorkbook.xlsx");
Console.WriteLine("CreateSharedWorkbook executed successfully.\r\n");
```

## خاتمة

تهنئة ! لقد تعلمت كيفية إنشاء مصنف مشترك باستخدام Aspose.Cells for .NET. يمكن استخدام المصنف المشترك من قبل عدة مستخدمين في وقت واحد للتعاون في البيانات. جرب بياناتك الخاصة واستكشف ميزات Aspose.Cells لإنشاء مصنفات Excel قوية ومخصصة.

### أسئلة وأجوبة

#### س: ما هو المصنف المشترك؟

ج: المصنف المشترك هو مصنف Excel يمكن استخدامه في وقت واحد من قبل عدة مستخدمين للتعاون في البيانات. يمكن لكل مستخدم إجراء تغييرات على المصنف وسيرى المستخدمون الآخرون التحديثات في الوقت الفعلي.

#### س: كيف يمكن تمكين مشاركة مصنف في Aspose.Cells for .NET؟

 ج: لتمكين مشاركة مصنف في Aspose.Cells لـ .NET ، يجب عليك تعيين`Shared` الكائن في المصنف`true`. سيسمح هذا للمستخدمين بالعمل على المصنف في وقت واحد.

#### س: هل يمكنني تقييد أذونات المستخدم في مصنف مشترك؟

ج: نعم ، يمكنك تقييد أذونات المستخدم في مصنف مشترك باستخدام ميزات أمان Excel. يمكنك تعيين أذونات محددة لكل مستخدم ، مثل القدرة على التعديل ، والقراءة فقط ، وما إلى ذلك.

#### س: كيف يمكنني مشاركة المصنف مع مستخدمين آخرين؟

ج: بمجرد إنشاء المصنف المشترك ، يمكنك مشاركته مع مستخدمين آخرين عن طريق إرسال ملف Excel إليهم. سيتمكن المستخدمون الآخرون من فتح الملف والعمل عليه في وقت واحد.

#### س: هل كل ميزات Excel مدعومة في مصنف مشترك؟

ج: يتم دعم معظم ميزات Excel في مصنف مشترك. ومع ذلك ، قد يكون لبعض الميزات المتقدمة ، مثل وحدات الماكرو والوظائف الإضافية ، قيود أو قيود عند استخدامها في مصنف مشترك.