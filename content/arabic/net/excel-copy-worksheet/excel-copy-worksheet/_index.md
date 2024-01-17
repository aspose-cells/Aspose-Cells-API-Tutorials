---
title: ورقة عمل نسخ إكسل
linktitle: ورقة عمل نسخ إكسل
second_title: Aspose.Cells لمرجع .NET API
description: انسخ ورقة عمل Excel إلى أخرى باستخدام Aspose.Cells لـ .NET.
type: docs
weight: 20
url: /ar/net/excel-copy-worksheet/excel-copy-worksheet/
---

سنشرح في هذا الدليل كيفية نسخ ورقة عمل Excel باستخدام مكتبة Aspose.Cells لـ .NET. سنزودك بكود مصدر C# وسنرشدك خلال الخطوات اللازمة لإكمال هذه المهمة. وفي النهاية سنعرض لك النتيجة المتوقعة. اتبع الإرشادات أدناه للبدء.

## الخطوة 1: التحضير

قبل البدء، تأكد من تثبيت Aspose.Cells لـ .NET وإنشاء مشروع C# في بيئة التطوير المتكاملة (IDE) المفضلة لديك. تأكد أيضًا من أن لديك نسخة من ملف Excel الذي تريد معالجته.

## الخطوة 2: استيراد المكتبات المطلوبة

 في ملف مصدر C#، قم باستيراد المكتبات الضرورية من Aspose.Cells باستخدام ملف`using` التوجيه:

```csharp
using Aspose.Cells;
```

## الخطوة 3: تعيين مسار الملف

 أعلن أ`dataDir` متغير وقم بتهيئته بالدليل الذي يحتوي على ملف Excel الخاص بك. على سبيل المثال :

```csharp
string dataDir = "PATH_TO_YOUR_DOCUMENT_DIRECTORY";
```

 تأكد من استبدال`"PATH_TO_YOUR_DOCUMENT_DIRECTORY"` مع المسار الفعلي إلى الدليل الخاص بك.

## الخطوة 4: تحميل ملف Excel الموجود

 استخدم ال`Workbook` فئة من Aspose.Cells لفتح ملف Excel الموجود. استخدم ال`InputPath` متغير لتحديد مسار الملف:

```csharp
string InputPath = dataDir + "book1.xls";
Workbook wb = new Workbook(InputPath);
```

 تأكد من أنك قد استبدلت`"book1.xls"` بالاسم الفعلي لملف Excel الخاص بك.

## الخطوة 5: انسخ ورقة العمل

 الآن سنقوم بنسخ ورقة العمل الموجودة إلى ورقة عمل جديدة. استخدم ال`Worksheets` ملكية`Workbook` كائن للوصول إلى مجموعة أوراق العمل:

```csharp
WorksheetCollection sheets = wb.Worksheets;
```

 ثم استخدم`AddCopy` طريقة لنسخ ورقة العمل المحددة. على سبيل المثال، لنسخ "الورقة1":

```csharp
sheets.AddCopy("Sheet1");
```

## الخطوة 6: احفظ ملف Excel

 استخدم ال`Save` طريقة`Workbook` كائن لحفظ التغييرات في ملف جديد:

```csharp
wb.Save(dataDir + "CopyWithinWorkbook_out.xls");
```

تأكد من تحديد المسار واسم الملف المطلوبين لملف الإخراج.

### نموذج التعليمات البرمجية المصدر لبرنامج Excel Copy Worksheet باستخدام Aspose.Cells لـ .NET 

```csharp
//المسار إلى دليل المستندات.
string dataDir = "YOUR DOCUMENT DIRECTORY";
string InputPath = dataDir + "book1.xls";
// افتح ملف Excel موجود.
Workbook wb = new Workbook(InputPath);
// قم بإنشاء كائن أوراق العمل بالإشارة إلى
// أوراق كتاب العمل.
WorksheetCollection sheets = wb.Worksheets;
// انسخ البيانات إلى ورقة جديدة من ورقة موجودة
// ورقة داخل المصنف.
sheets.AddCopy("Sheet1");
// احفظ ملف إكسل.
wb.Save(dataDir + "CopyWithinWorkbook_out.xls");
```

## خاتمة

تهنئة ! لقد تعلمت الآن كيفية نسخ ورقة عمل Excel باستخدام Aspose.Cells لـ .NET. يوضح هذا الدليل خطوة بخطوة كيفية استيراد المكتبات الضرورية وتحميل ملف Excel موجود ونسخ ورقة العمل وحفظ الملف المعدل. لا تتردد في استخدام هذه الطريقة في مشاريعك الخاصة لمعالجة ملفات Excel بكفاءة.

### الأسئلة الشائعة

#### س: هل Aspose.Cells متوافق مع لغات البرمجة الأخرى؟

A. نعم، يدعم Aspose.Cells لغات برمجة متعددة بما في ذلك C# وJava وPython وغيرها الكثير.

#### س: هل يمكنني نسخ ورقة عمل إلى مصنف Excel آخر؟

A.  نعم يمكنك استخدام`AddCopy` طريقة لنسخ ورقة عمل إلى مصنف Excel آخر.

#### س. هل يحتفظ Aspose.Cells بالصيغ والتنسيقات عند نسخ ورقة العمل؟

A. نعم، يحتفظ Aspose.Cells بالصيغ والتنسيقات والخصائص الأخرى عند نسخ ورقة العمل.

#### س. هل يتطلب Aspose.Cells ترخيصًا للاستخدام التجاري؟

A. نعم، Aspose.Cells هو منتج تجاري ويتطلب شراء ترخيص للاستخدام التجاري. يمكنك العثور على مزيد من معلومات الترخيص على موقع Aspose الرسمي.