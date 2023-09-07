---
title: حدد المؤلف أثناء الكتابة حماية مصنف Excel
linktitle: حدد المؤلف أثناء الكتابة حماية مصنف Excel
second_title: Aspose.Cells لمرجع .NET API
description: تعرف على كيفية حماية مصنفات Excel الخاصة بك وتخصيصها باستخدام Aspose.Cells for .NET. تعليمي خطوة بخطوة في C #.
type: docs
weight: 30
url: /ar/net/excel-security/specify-author-while-write-protecting-excel-workbook/
---

في هذا البرنامج التعليمي ، سنوضح لك كيفية تحديد المؤلف عند حماية مصنف Excel باستخدام مكتبة Aspose.Cells لـ .NET.

## الخطوة الأولى: تهيئة البيئة

قبل أن تبدأ ، تأكد من تثبيت Aspose.Cells for .NET على جهازك. قم بتنزيل المكتبة من موقع Aspose الرسمي واتبع تعليمات التثبيت المتوفرة.

## الخطوة 2: تكوين أدلة المصدر والمخرجات

في كود المصدر المقدم ، يجب عليك تحديد مصدر ومجلد الإخراج. تعديل`sourceDir` و`outputDir` المتغيرات من خلال استبدال "YOUR SOURCE DIRECTORY" و "YOUR OUTPUT DIRECTORY" بالمسارات المطلقة ذات الصلة على جهازك.

```csharp
// دليل المصدر
string sourceDir = "PATH TO YOUR SOURCE DIRECTORY";

// دليل الإخراج
string outputDir = "YOUR OUTPUT DIRECTORY PATH";
```

## الخطوة 3: إنشاء مصنف Excel فارغ

للبدء ، نقوم بإنشاء كائن مصنف يمثل مصنف Excel فارغًا.

```csharp
// إنشاء مصنف فارغ.
Workbook wb = new Workbook();
```

## الخطوة 4: اكتب الحماية بكلمة مرور

 بعد ذلك ، نحدد كلمة مرور لكتابة حماية مصنف Excel باستخدام ملف`WriteProtection.Password` خاصية كائن المصنف.

```csharp
// اكتب حماية المصنف بكلمة مرور.
wb.Settings.WriteProtection.Password = "YOUR_PASSWORD";
```

## الخطوة 5: مواصفات المؤلف

 الآن نحدد مؤلف مصنف Excel باستخدام ملف`WriteProtection.Author` خاصية كائن المصنف.

```csharp
// حدد المؤلف أثناء كتابة حماية المصنف.
wb.Settings.WriteProtection.Author = "YOUR_AUTHOR";
```

## الخطوة 6: مصنف Excel المحمي احتياطيًا

 بمجرد تحديد الحماية ضد الكتابة والمؤلف ، يمكننا حفظ مصنف Excel بتنسيق XLSX باستخدام ملف`Save()` طريقة.

```csharp
// احفظ المصنف بتنسيق XLSX.
wb.Save(outputDir + "outputSpecifyAuthorWhileWriteProtectingWorkbook.xlsx");
```

### نموذج التعليمات البرمجية المصدر لتحديد المؤلف أثناء الكتابة حماية مصنف Excel باستخدام Aspose.Cells for .NET 
```csharp
//دليل المصدر
string sourceDir = "YOUR SOURCE DIRECTORY";

//دليل الإخراج
string outputDir = "YOUR OUTPUT DIRECTORY";

// إنشاء مصنف فارغ.
Workbook wb = new Workbook();

// اكتب حماية المصنف بكلمة مرور.
wb.Settings.WriteProtection.Password = "YOUR_PASSWORD";

// حدد المؤلف أثناء كتابة حماية المصنف.
wb.Settings.WriteProtection.Author = "YOUR_AUTHOR";

// احفظ المصنف بتنسيق XLSX.
wb.Save(outputDir + "outputSpecifyAuthorWhileWriteProtectingWorkbook.xlsx");

```

## خاتمة

تهنئة ! لقد تعلمت الآن كيفية تحديد المؤلف عند حماية مصنف Excel باستخدام Aspose.Cells for .NET. يمكنك تطبيق هذه الخطوات على مشاريعك الخاصة لحماية مصنفات Excel الخاصة بك وتخصيصها.

لا تتردد في استكشاف ميزات Aspose.Cells for .NET لمزيد من العمليات المتقدمة على ملفات Excel.

## أسئلة وأجوبة

#### س: هل يمكنني كتابة حماية مصنف Excel بدون تحديد كلمة مرور؟

 ج: نعم ، يمكنك استخدام كائن المصنف`WriteProtect()` طريقة دون تحديد كلمة مرور لحماية مصنف Excel من الكتابة. سيؤدي هذا إلى تقييد التغييرات في المصنف دون الحاجة إلى كلمة مرور.

#### س: كيف يمكنني إزالة الحماية ضد الكتابة من مصنف Excel؟

 ج: لإزالة الحماية ضد الكتابة من مصنف Excel ، يمكنك استخدام ملحق`Unprotect()` طريقة كائن ورقة العمل أو ملف`RemoveWriteProtection()` طريقة كائن المصنف ، اعتمادًا على حالة الاستخدام المحددة الخاصة بك. .

#### س: لقد نسيت كلمة المرور لحماية مصنف Excel الخاص بي. ماذا يمكنني أن أفعل ؟

ج: إذا نسيت كلمة المرور لحماية مصنف Excel ، فلا يمكنك إزالته مباشرة. ومع ذلك ، يمكنك محاولة استخدام أدوات الجهات الخارجية المتخصصة التي توفر ميزات استعادة كلمة المرور لملفات Excel المحمية.

#### س: هل من الممكن تحديد عدة مؤلفين عند حماية مصنف Excel من الكتابة؟

ج: لا ، تسمح مكتبة Aspose.Cells for .NET بتحديد مؤلف واحد عند حماية مصنف Excel من الكتابة. إذا كنت تريد تحديد مؤلفين متعددين ، فستحتاج إلى التفكير في حلول مخصصة من خلال معالجة ملف Excel مباشرة.