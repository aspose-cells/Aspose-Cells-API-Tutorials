---
title: تحديد المؤلف أثناء الكتابة لحماية مصنف Excel
linktitle: تحديد المؤلف أثناء الكتابة لحماية مصنف Excel
second_title: Aspose.Cells لمرجع .NET API
description: تعرف على كيفية حماية مصنفات Excel وتخصيصها باستخدام Aspose.Cells for .NET. البرنامج التعليمي خطوة بخطوة في C#.
type: docs
weight: 30
url: /ar/net/excel-security/specify-author-while-write-protecting-excel-workbook/
---

سنوضح لك في هذا البرنامج التعليمي كيفية تحديد المؤلف عند حماية الكتابة لمصنف Excel باستخدام مكتبة Aspose.Cells لـ .NET.

## الخطوة 1: إعداد البيئة

قبل البدء، تأكد من تثبيت Aspose.Cells for .NET على جهازك. قم بتنزيل المكتبة من موقع Aspose الرسمي واتبع تعليمات التثبيت المتوفرة.

## الخطوة 2: تكوين أدلة المصدر والإخراج

في كود المصدر المقدم، يجب عليك تحديد دليل المصدر والإخراج. تعديل`sourceDir` و`outputDir` المتغيرات عن طريق استبدال "YOUR SOURCE DIRECTORY" و"YOUR OUTPUT DIRECTORY" بالمسارات المطلقة المعنية على جهازك.

```csharp
// دليل المصدر
string sourceDir = "PATH TO YOUR SOURCE DIRECTORY";

// دليل الإخراج
string outputDir = "YOUR OUTPUT DIRECTORY PATH";
```

## الخطوة 3: إنشاء مصنف Excel فارغ

للبدء، نقوم بإنشاء كائن مصنف يمثل مصنف Excel فارغًا.

```csharp
// إنشاء مصنف فارغ.
Workbook wb = new Workbook();
```

## الخطوة 4: كتابة الحماية بكلمة المرور

 بعد ذلك، نحدد كلمة مرور لكتابة حماية مصنف Excel باستخدام الملف`WriteProtection.Password` خاصية كائن المصنف.

```csharp
// كتابة مصنف الحماية بكلمة مرور.
wb.Settings.WriteProtection.Password = "YOUR_PASSWORD";
```

## الخطوة 5: مواصفات المؤلف

 الآن نحدد مؤلف مصنف Excel باستخدام الملف`WriteProtection.Author` خاصية كائن المصنف.

```csharp
// حدد المؤلف أثناء كتابة مصنف الحماية.
wb.Settings.WriteProtection.Author = "YOUR_AUTHOR";
```

## الخطوة 6: النسخ الاحتياطي لمصنف Excel المحمي

 بمجرد تحديد الحماية ضد الكتابة والمؤلف، يمكننا حفظ مصنف Excel بتنسيق XLSX باستخدام الملف`Save()` طريقة.

```csharp
// احفظ المصنف بتنسيق XLSX.
wb.Save(outputDir + "outputSpecifyAuthorWhileWriteProtectingWorkbook.xlsx");
```

### نموذج التعليمات البرمجية المصدر لمصنف Excel "تحديد المؤلف أثناء حماية الكتابة" باستخدام Aspose.Cells لـ .NET 
```csharp
//دليل المصدر
string sourceDir = "YOUR SOURCE DIRECTORY";

//دليل الإخراج
string outputDir = "YOUR OUTPUT DIRECTORY";

// إنشاء مصنف فارغ.
Workbook wb = new Workbook();

// كتابة مصنف الحماية بكلمة مرور.
wb.Settings.WriteProtection.Password = "YOUR_PASSWORD";

// حدد المؤلف أثناء كتابة مصنف الحماية.
wb.Settings.WriteProtection.Author = "YOUR_AUTHOR";

// احفظ المصنف بتنسيق XLSX.
wb.Save(outputDir + "outputSpecifyAuthorWhileWriteProtectingWorkbook.xlsx");

```

## خاتمة

تهنئة ! لقد تعلمت الآن كيفية تحديد المؤلف عند حماية مصنف Excel من الكتابة باستخدام Aspose.Cells for .NET. يمكنك تطبيق هذه الخطوات على مشاريعك الخاصة لحماية مصنفات Excel وتخصيصها.

لا تتردد في استكشاف المزيد من ميزات Aspose.Cells for .NET لإجراء المزيد من العمليات المتقدمة على ملفات Excel.

## الأسئلة الشائعة

#### س: هل يمكنني الكتابة لحماية مصنف Excel دون تحديد كلمة مرور؟

 ج: نعم، يمكنك استخدام كائنات المصنف`WriteProtect()` الطريقة دون تحديد كلمة مرور لحماية مصنف Excel من الكتابة. سيؤدي هذا إلى تقييد التغييرات في المصنف دون الحاجة إلى كلمة مرور.

#### س: كيف يمكنني إزالة الحماية ضد الكتابة من مصنف Excel؟

 ج: لإزالة الحماية ضد الكتابة من مصنف Excel، يمكنك استخدام`Unprotect()` طريقة كائن ورقة العمل أو`RemoveWriteProtection()` طريقة كائن المصنف، اعتمادًا على حالة الاستخدام المحددة الخاصة بك. .

#### س: لقد نسيت كلمة المرور لحماية مصنف Excel الخاص بي. ماذا يمكنني أن أفعل ؟

ج: إذا نسيت كلمة المرور لحماية مصنف Excel الخاص بك، فلن تتمكن من إزالتها مباشرة. ومع ذلك، يمكنك محاولة استخدام أدوات خارجية متخصصة توفر ميزات استعادة كلمة المرور لملفات Excel المحمية.

#### س: هل من الممكن تحديد مؤلفين متعددين عند حماية مصنف Excel من الكتابة؟

ج: لا، تسمح مكتبة Aspose.Cells for .NET بتحديد مؤلف واحد عند حماية مصنف Excel من الكتابة. إذا كنت تريد تحديد مؤلفين متعددين، فستحتاج إلى التفكير في حلول مخصصة من خلال التعامل مباشرة مع ملف Excel.