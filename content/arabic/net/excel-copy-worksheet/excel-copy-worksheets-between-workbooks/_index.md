---
title: Excel نسخ أوراق العمل بين المصنفات
linktitle: Excel نسخ أوراق العمل بين المصنفات
second_title: Aspose.Cells لمرجع .NET API
description: انسخ أوراق العمل بسهولة بين مصنفات Excel باستخدام Aspose.Cells for .NET.
type: docs
weight: 30
url: /ar/net/excel-copy-worksheet/excel-copy-worksheets-between-workbooks/
---
في هذا البرنامج التعليمي ، سنوجهك عبر خطوات نسخ أوراق العمل بين مصنفات Excel باستخدام مكتبة Aspose.Cells لـ .NET. اتبع التعليمات أدناه لإكمال هذه المهمة.

## الخطوة الأولى: التحضير

تأكد من تثبيت Aspose.Cells لـ .NET وإنشاء مشروع C # في بيئة التطوير المتكاملة المفضلة لديك (IDE).

## الخطوة 2: قم بتعيين مسار دليل المستند

 تعلن أ`dataDir` متغير وتهيئته بالمسار إلى دليل المستندات. على سبيل المثال :

```csharp
string dataDir = "YOUR_DIRECTORY_OF_DOCUMENTS";
```

 تأكد من استبدال`"YOUR_DOCUMENTS_DIRECTORY"` مع المسار الفعلي للدليل الخاص بك.

## الخطوة 3: تحديد مسار ملف الإدخال

 نعلن`InputPath` متغيرًا وتهيئته بالمسار الكامل لملف Excel الذي تريد نسخ جدول البيانات منه. على سبيل المثال :

```csharp
string InputPath = dataDir + "book1.xls";
```

 تأكد من أن لديك ملف Excel`book1.xls` في دليل المستندات الخاص بك أو تحديد اسم الملف الصحيح والموقع.

## الخطوة 4: قم بإنشاء أول مصنف Excel

 استخدم ال`Workbook` فئة Aspose.Cells لإنشاء أول مصنف Excel وفتح الملف المحدد:

```csharp
Workbook excelWorkbook0 = new Workbook(InputPath);
```

## الخطوة 5: قم بإنشاء مصنف Excel ثانٍ

قم بإنشاء مصنف Excel ثانٍ:

```csharp
Workbook excelWorkbook1 = new Workbook();
```

## الخطوة 6: انسخ ورقة العمل من المصنف الأول إلى المصنف الثاني

 استخدم ال`Copy`طريقة لنسخ ورقة العمل الأولى من المصنف الأول إلى المصنف الثاني:

```csharp
excelWorkbook1.Worksheets[0].Copy(excelWorkbook0.Worksheets[0]);
```

## الخطوة 7: احفظ ملف Excel

احفظ ملف Excel الذي يحتوي على جدول البيانات المنسوخ:

```csharp
excelWorkbook1.Save(dataDir + "Copy WorksheetsBetweenWorkbooks_out.xls");
```

تأكد من تحديد المسار المطلوب واسم الملف لملف الإخراج.

### نموذج التعليمات البرمجية المصدر لبرنامج Excel نسخ أوراق العمل بين المصنفات باستخدام Aspose.Cells for .NET 
```csharp
// المسار إلى دليل المستندات.
string dataDir = "YOUR DOCUMENT DIRECTORY";
string InputPath = dataDir + "book1.xls";
// قم بإنشاء مصنف.
// افتح ملفًا في الكتاب الأول.
Workbook excelWorkbook0 = new Workbook(InputPath);
// قم بإنشاء مصنف آخر.
Workbook excelWorkbook1 = new Workbook();
// انسخ الورقة الأولى من الكتاب الأول في الكتاب الثاني.
excelWorkbook1.Worksheets[0].Copy(excelWorkbook0.Worksheets[0]);
// حفظ الملف.
excelWorkbook1.Save(dataDir + "CopyWorksheetsBetweenWorkbooks_out.xls");
```

## خاتمة

تهنئة ! لقد تعلمت الآن كيفية نسخ أوراق العمل بين مصنفات Excel باستخدام Aspose.Cells for .NET. لا تتردد في استخدام هذه الطريقة في مشاريعك الخاصة لمعالجة ملفات Excel بكفاءة.

### أسئلة وأجوبة

#### س: ما هي المكتبات اللازمة لاستخدام Aspose.Cells لـ .NET؟

A. لاستخدام Aspose.Cells لـ .NET ، يجب عليك تضمين مكتبة Aspose.Cells في مشروعك. تأكد من الرجوع إلى هذه المكتبة بشكل صحيح في بيئة التطوير المتكاملة (IDE).

#### س: هل تدعم Aspose.Cells تنسيقات ملفات Excel الأخرى ، مثل XLSX؟

A. نعم ، Aspose.Cells يدعم العديد من تنسيقات ملفات Excel بما في ذلك XLSX و XLS و CSV و HTML وغيرها الكثير. يمكنك معالجة تنسيقات الملفات هذه باستخدام ميزات Aspose.Cells for .NET.

#### س هل يمكنني تخصيص خيارات التخطيط عند نسخ جدول البيانات؟

A.  نعم ، يمكنك تخصيص خيارات إعداد الصفحة عند نسخ جدول البيانات باستخدام خصائص ملف`PageSetup` هدف. يمكنك تحديد رؤوس الصفحات ، والتذييلات ، والهوامش ، والاتجاهات ، وما إلى ذلك.