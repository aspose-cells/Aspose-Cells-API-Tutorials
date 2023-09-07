---
title: نسخ ورقة عمل Excel
linktitle: نسخ ورقة عمل Excel
second_title: Aspose.Cells لمرجع .NET API
description: انسخ ورقة عمل Excel إلى أخرى باستخدام Aspose.Cells for .NET.
type: docs
weight: 20
url: /ar/net/excel-copy-worksheet/excel-copy-worksheet/
---

في هذا الدليل ، سنشرح كيفية نسخ ورقة عمل Excel باستخدام مكتبة Aspose.Cells لـ .NET. سنزودك بكود مصدر C # وسنرشدك خلال الخطوات اللازمة لإكمال هذه المهمة. في النهاية ، سوف نعرض لك النتيجة المتوقعة. اتبع التعليمات أدناه لتبدأ.

## الخطوة الأولى: التحضير

قبل أن تبدأ ، تأكد من تثبيت Aspose.Cells لـ .NET وإنشاء مشروع C # في بيئة التطوير المتكاملة المفضلة لديك (IDE). تأكد أيضًا من أن لديك نسخة من ملف Excel الذي تريد معالجته.

## الخطوة 2: استيراد المكتبات المطلوبة

 في ملف المصدر C # الخاص بك ، قم باستيراد المكتبات الضرورية من Aspose.Cells باستخدام امتداد`using` التوجيه:

```csharp
using Aspose.Cells;
```

## الخطوة 3: حدد مسار الملف

 تعلن أ`dataDir` متغير وتهيئته بالدليل الذي يحتوي على ملف Excel الخاص بك. على سبيل المثال :

```csharp
string dataDir = "PATH_TO_YOUR_DOCUMENT_DIRECTORY";
```

 تأكد من استبدال`"PATH_TO_YOUR_DOCUMENT_DIRECTORY"` مع المسار الفعلي للدليل الخاص بك.

## الخطوة 4: تحميل ملف Excel الحالي

 استخدم ال`Workbook`فئة من Aspose.Cells لفتح ملف Excel الحالي. استخدم ال`InputPath` متغير لتحديد مسار الملف:

```csharp
string InputPath = dataDir + "book1.xls";
Workbook wb = new Workbook(InputPath);
```

 تأكد من أنك استبدلت`"book1.xls"` بالاسم الفعلي لملف Excel الخاص بك.

## الخطوة 5: انسخ ورقة العمل

 الآن سنقوم بنسخ ورقة العمل الحالية إلى ورقة عمل جديدة. استخدم ال`Worksheets` ممتلكات`Workbook` كائن للوصول إلى مجموعة أوراق العمل:

```csharp
WorksheetCollection sheets = wb.Worksheets;
```

 ثم استخدم ملف`AddCopy` طريقة لنسخ ورقة العمل المحددة. على سبيل المثال ، لنسخ "الورقة 1":

```csharp
sheets.AddCopy("Sheet1");
```

## الخطوة 6: احفظ ملف Excel

 استخدم ال`Save` طريقة`Workbook` كائن لحفظ التغييرات في ملف جديد:

```csharp
wb.Save(dataDir + "CopyWithinWorkbook_out.xls");
```

تأكد من تحديد المسار المطلوب واسم الملف لملف الإخراج.

### نموذج التعليمات البرمجية المصدر لـ Excel Copy Worksheet باستخدام Aspose.Cells for .NET 

```csharp
// المسار إلى دليل المستندات.
string dataDir = "YOUR DOCUMENT DIRECTORY";
string InputPath = dataDir + "book1.xls";
// افتح ملف Excel موجود.
Workbook wb = new Workbook(InputPath);
// قم بإنشاء كائن أوراق عمل بالإشارة إلى
// أوراق المصنف.
WorksheetCollection sheets = wb.Worksheets;
// انسخ البيانات إلى ورقة جديدة من ملف
// ورقة داخل المصنف.
sheets.AddCopy("Sheet1");
// احفظ ملف Excel.
wb.Save(dataDir + "CopyWithinWorkbook_out.xls");
```

## خاتمة

تهنئة ! لقد تعلمت الآن كيفية نسخ ورقة عمل Excel باستخدام Aspose.Cells for .NET. يوضح هذا الدليل التفصيلي كيفية استيراد المكتبات الضرورية ، وتحميل ملف Excel موجود ، ونسخ ورقة العمل وحفظ الملف المعدل. لا تتردد في استخدام هذه الطريقة في مشاريعك الخاصة لمعالجة ملفات Excel بكفاءة.

### أسئلة وأجوبة

#### س: هل Aspose.Cells متوافق مع لغات البرمجة الأخرى؟

A. نعم ، تدعم Aspose.Cells لغات برمجة متعددة بما في ذلك C # و Java و Python وغيرها الكثير.

#### س هل يمكنني نسخ ورقة عمل إلى مصنف Excel آخر؟

A.  نعم ، يمكنك استخدام ملف`AddCopy` طريقة لنسخ ورقة عمل إلى مصنف Excel آخر.

#### س: هل يحتفظ Aspose.Cells بالصيغ والتنسيقات عند نسخ ورقة العمل؟

A. نعم ، Aspose.Cells يحافظ على الصيغ والتنسيقات والخصائص الأخرى عند نسخ ورقة العمل.

#### س: هل تتطلب Aspose.Cells ترخيصًا للاستخدام التجاري؟

A. نعم ، Aspose.Cells منتج تجاري ويتطلب شراء ترخيص للاستخدام التجاري. يمكنك العثور على مزيد من معلومات الترخيص على موقع Aspose الرسمي.