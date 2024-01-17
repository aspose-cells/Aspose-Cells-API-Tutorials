---
title: Excel نسخ أوراق العمل بين المصنفات
linktitle: Excel نسخ أوراق العمل بين المصنفات
second_title: Aspose.Cells لمرجع .NET API
description: انسخ أوراق العمل بسهولة بين مصنفات Excel باستخدام Aspose.Cells لـ .NET.
type: docs
weight: 30
url: /ar/net/excel-copy-worksheet/excel-copy-worksheets-between-workbooks/
---
في هذا البرنامج التعليمي، سنرشدك خلال خطوات نسخ أوراق العمل بين مصنفات Excel باستخدام مكتبة Aspose.Cells لـ .NET. اتبع الإرشادات أدناه لإكمال هذه المهمة.

## الخطوة 1: التحضير

تأكد من تثبيت Aspose.Cells لـ .NET وإنشاء مشروع C# في بيئة التطوير المتكاملة المفضلة لديك (IDE).

## الخطوة 2: قم بتعيين مسار دليل المستند

 أعلن أ`dataDir` متغير وقم بتهيئته بالمسار إلى دليل المستندات الخاص بك. على سبيل المثال :

```csharp
string dataDir = "YOUR_DIRECTORY_OF_DOCUMENTS";
```

 تأكد من استبدال`"YOUR_DOCUMENTS_DIRECTORY"` مع المسار الفعلي إلى الدليل الخاص بك.

## الخطوة 3: تحديد مسار ملف الإدخال

 أعلن أ`InputPath` متغير وقم بتهيئته بالمسار الكامل لملف Excel الذي تريد نسخ جدول البيانات منه. على سبيل المثال :

```csharp
string InputPath = dataDir + "book1.xls";
```

 تأكد من أن لديك ملف Excel`book1.xls` في دليل المستندات الخاص بك أو حدد اسم الملف الصحيح وموقعه.

## الخطوة 4: إنشاء مصنف Excel الأول

 استخدم ال`Workbook` فئة Aspose.Cells لإنشاء مصنف Excel الأول وفتح الملف المحدد:

```csharp
Workbook excelWorkbook0 = new Workbook(InputPath);
```

## الخطوة 5: إنشاء مصنف Excel ثانٍ

قم بإنشاء مصنف Excel ثانيًا:

```csharp
Workbook excelWorkbook1 = new Workbook();
```

## الخطوة 6: انسخ ورقة العمل من المصنف الأول إلى المصنف الثاني

 استخدم ال`Copy`طريقة نسخ ورقة العمل الأولى من المصنف الأول إلى المصنف الثاني:

```csharp
excelWorkbook1.Worksheets[0].Copy(excelWorkbook0.Worksheets[0]);
```

## الخطوة 7: احفظ ملف Excel

احفظ ملف Excel الذي يحتوي على جدول البيانات المنسوخ:

```csharp
excelWorkbook1.Save(dataDir + "Copy WorksheetsBetweenWorkbooks_out.xls");
```

تأكد من تحديد المسار واسم الملف المطلوبين لملف الإخراج.

### نموذج التعليمات البرمجية المصدر لبرنامج Excel نسخ أوراق العمل بين المصنفات باستخدام Aspose.Cells لـ .NET 
```csharp
//المسار إلى دليل المستندات.
string dataDir = "YOUR DOCUMENT DIRECTORY";
string InputPath = dataDir + "book1.xls";
// إنشاء مصنف.
// افتح ملفًا في الكتاب الأول.
Workbook excelWorkbook0 = new Workbook(InputPath);
// إنشاء مصنف آخر.
Workbook excelWorkbook1 = new Workbook();
// انسخ الورقة الأولى من الكتاب الأول إلى الكتاب الثاني.
excelWorkbook1.Worksheets[0].Copy(excelWorkbook0.Worksheets[0]);
// حفظ الملف.
excelWorkbook1.Save(dataDir + "CopyWorksheetsBetweenWorkbooks_out.xls");
```

## خاتمة

تهنئة ! لقد تعلمت الآن كيفية نسخ أوراق العمل بين مصنفات Excel باستخدام Aspose.Cells لـ .NET. لا تتردد في استخدام هذه الطريقة في مشاريعك الخاصة لمعالجة ملفات Excel بكفاءة.

### الأسئلة الشائعة

#### س. ما المكتبات اللازمة لاستخدام Aspose.Cells لـ .NET؟

A. لاستخدام Aspose.Cells لـ .NET، يجب عليك تضمين مكتبة Aspose.Cells في مشروعك. تأكد من أنك قمت بالإشارة إلى هذه المكتبة بشكل صحيح في بيئة التطوير المتكاملة (IDE).

#### س. هل يدعم Aspose.Cells تنسيقات ملفات Excel الأخرى، مثل XLSX؟

A. نعم، يدعم Aspose.Cells العديد من تنسيقات ملفات Excel بما في ذلك XLSX وXLS وCSV وHTML وغيرها الكثير. يمكنك التعامل مع تنسيقات الملفات هذه باستخدام ميزات Aspose.Cells لـ .NET.

#### س: هل يمكنني تخصيص خيارات التخطيط عند نسخ جدول البيانات؟

A.  نعم، يمكنك تخصيص خيارات إعداد الصفحة عند نسخ جدول البيانات باستخدام خصائص`PageSetup` هدف. يمكنك تحديد رؤوس الصفحات وتذييلاتها والهوامش والاتجاهات وما إلى ذلك.