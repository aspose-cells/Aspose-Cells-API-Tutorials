---
title: حماية خلايا معينة في ورقة عمل Excel
linktitle: حماية خلايا معينة في ورقة عمل Excel
second_title: Aspose.Cells لمرجع .NET API
description: تعرف على كيفية حماية خلايا معينة في Excel باستخدام Aspose.Cells for .NET. تعليمي خطوة بخطوة في C #.
type: docs
weight: 70
url: /ar/net/protect-excel-file/protect-specific-cells-in-a-excel-worksheet/
---
في هذا البرنامج التعليمي ، سنلقي نظرة على التعليمات البرمجية المصدر C # التي تستخدم مكتبة Aspose.Cells لحماية خلايا معينة في جدول بيانات Excel. سنستعرض كل خطوة في الكود ونوضح كيف يعمل. اتبع التعليمات بعناية للحصول على النتائج المرجوة.

## الخطوة 1: المتطلبات الأساسية

قبل أن تبدأ ، تأكد من تثبيت مكتبة Aspose.Cells لـ .NET. يمكنك الحصول عليه من موقع Aspose الرسمي. تأكد أيضًا من أن لديك إصدارًا حديثًا من Visual Studio أو أي بيئة تطوير أخرى لـ C #.

## الخطوة 2: استيراد مساحات الأسماء المطلوبة

لاستخدام مكتبة Aspose.Cells ، نحتاج إلى استيراد مساحات الأسماء الضرورية إلى الكود الخاص بنا. أضف الأسطر التالية إلى أعلى ملف المصدر C #:

```csharp
using Aspose.Cells;
```

## الخطوة 3: إنشاء مصنف Excel

في هذه الخطوة ، سننشئ مصنف Excel جديدًا. استخدم التعليمات البرمجية التالية لإنشاء مصنف Excel:

```csharp
// المسار إلى دليل المستندات.
string dataDir = "YOUR_DIRECTORY_OF_DOCUMENTS";

// قم بإنشاء مصنف جديد.
Workbook wb = new Workbook();
```

 تأكد من استبدال`"YOUR_DOCUMENTS_DIR"` مع المسار المناسب إلى دليل المستندات الخاص بك.

## الخطوة 4: إنشاء جدول بيانات

الآن وقد أنشأنا مصنف Excel ، فلنقم بإنشاء ورقة عمل والحصول على الورقة الأولى. استخدم الكود التالي:

```csharp
// قم بإنشاء كائن جدول بيانات واحصل على الورقة الأولى.
Worksheet sheet = wb.Worksheets[0];
```

## الخطوة 5: تحديد النمط

في هذه الخطوة ، سنحدد النمط الذي سيتم تطبيقه على خلايا معينة. استخدم الكود التالي:

```csharp
// تعريف كائن النمط.
Styling styling;
```

## الخطوة 6: التكرار لفتح جميع الأعمدة

سنقوم الآن بالمرور عبر جميع الأعمدة في ورقة العمل وفتحها. استخدم الكود التالي:

```csharp
// قم بالتكرار خلال جميع الأعمدة في ورقة العمل وقم بإلغاء تأمينها.
for (int i = 0; i <= 255; i++)
{
     style = sheet.Cells.Columns[(byte)i].Style;
     style. IsLocked = false;
     sheet.Cells.Columns[(byte)i].ApplyStyle(style);
}
```

## الخطوة 7: قفل خلايا معينة

في هذه الخطوة ، سنغلق خلايا معينة. استخدم الكود التالي:

```csharp
//قفل جميع الخلايا الثلاث ... أي A1 ، B1 ، C1.
style = sheet.Cells["A1"].GetStyle();
style. IsLocked = true;
sheet.Cells["A1"].SetStyle(style);

style = sheet.Cells["B1"].GetStyle();
style. IsLocked = true;
sheet.Cells["B1"].SetStyle(style);

style = sheet.Cells["C1"].GetStyle();
style. IsLocked = true;
sheet.Cells["C1"].SetStyle(style);
```

## الخطوة 8: حماية ورقة العمل

أخيرًا ، سنحمي ورقة العمل لمنع تعديل خلايا معينة. استخدم الكود التالي:

```csharp
// حماية ورقة العمل.
sheet.Protect(ProtectionType.All);
```

## الخطوة 9: حفظ ملف Excel

سنقوم الآن بحفظ ملف Excel المعدل. استخدم الكود التالي:

```csharp
// احفظ ملف Excel.
wb.Save(dataDir + "output.out.xls", SaveFormat.Excel97To2003);
```

تأكد من تحديد المسار الصحيح لحفظ ملف Excel المعدل.

### نموذج التعليمات البرمجية المصدر لحماية خلايا معينة في ورقة عمل Excel باستخدام Aspose.Cells for .NET 
```csharp
// المسار إلى دليل المستندات.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// قم بإنشاء دليل إذا لم يكن موجودًا بالفعل.
bool IsExists = System.IO.Directory.Exists(dataDir);
if (!IsExists)
    System.IO.Directory.CreateDirectory(dataDir);
// قم بإنشاء مصنف جديد.
Workbook wb = new Workbook();
// قم بإنشاء كائن ورقة عمل والحصول على الورقة الأولى.
Worksheet sheet = wb.Worksheets[0];
// تحديد كائن النمط.
Style style;
// تحديد كائن styleflag
StyleFlag styleflag;
// قم بالتكرار خلال جميع الأعمدة في ورقة العمل وقم بإلغاء تأمينها.
for (int i = 0; i <= 255; i++)
{
    style = sheet.Cells.Columns[(byte)i].Style;
    style.IsLocked = false;
    styleflag = new StyleFlag();
    styleflag.Locked = true;
    sheet.Cells.Columns[(byte)i].ApplyStyle(style, styleflag);
}
// قفل الخلايا الثلاث ... أي A1 ، B1 ، C1.
style = sheet.Cells["A1"].GetStyle();
style.IsLocked = true;
sheet.Cells["A1"].SetStyle(style);
style = sheet.Cells["B1"].GetStyle();
style.IsLocked = true;
sheet.Cells["B1"].SetStyle(style);
style = sheet.Cells["C1"].GetStyle();
style.IsLocked = true;
sheet.Cells["C1"].SetStyle(style);
//أخيرًا ، قم بحماية الورقة الآن.
sheet.Protect(ProtectionType.All);
// احفظ ملف اكسل.
wb.Save(dataDir + "output.out.xls", SaveFormat.Excel97To2003);
```


## خاتمة

تهنئة ! لديك الآن كود مصدر C # يسمح لك بحماية خلايا معينة في ورقة عمل Excel باستخدام مكتبة Aspose.Cells لـ .NET. لا تتردد في تخصيص الكود ليناسب احتياجاتك الخاصة.

### أسئلة وأجوبة (أسئلة متكررة)

#### هل يعمل هذا الرمز مع الإصدارات الأخيرة من Excel؟

نعم ، يعمل هذا الرمز مع الإصدارات الحديثة من Excel ، بما في ذلك الملفات بتنسيق Excel 2010 وما فوق.

#### هل يمكنني حماية الخلايا الأخرى إلى جانب A1 و B1 و C1؟

نعم ، يمكنك تعديل التعليمات البرمجية لقفل خلايا محددة أخرى عن طريق ضبط مراجع الخلية في سطور التعليمات البرمجية المقابلة.

#### كيف يمكنني فتح الخلايا المقفلة مرة أخرى؟

 يمكنك استخدام`SetStyle` طريقة مع`IsLocked` ضبط ل`false` لفتح الخلايا.

#### هل يمكنني إضافة المزيد من أوراق العمل إلى المصنف؟

 نعم ، يمكنك إضافة أوراق عمل أخرى إلى المصنف باستخدام ملحق`Worksheets.Add()`الطريقة وكرر خطوات حماية الخلية لكل ورقة عمل.

#### كيف يمكنني تغيير تنسيق الحفظ لملف Excel؟

 يمكنك تغيير تنسيق الحفظ باستخدام ملف`SaveFormat` الطريقة بالتنسيق المطلوب ، على سبيل المثال`SaveFormat.Xlsx` لبرنامج Excel 2007 والإصدارات الأحدث.