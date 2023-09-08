---
title: حماية خلايا محددة في ورقة عمل Excel
linktitle: حماية خلايا محددة في ورقة عمل Excel
second_title: Aspose.Cells لمرجع .NET API
description: تعرف على كيفية حماية خلايا معينة في Excel باستخدام Aspose.Cells لـ .NET. البرنامج التعليمي خطوة بخطوة في C#.
type: docs
weight: 70
url: /ar/net/protect-excel-file/protect-specific-cells-in-a-excel-worksheet/
---
في هذا البرنامج التعليمي، سنلقي نظرة على الكود المصدري لـ C# الذي يستخدم مكتبة Aspose.Cells لحماية خلايا معينة في جدول بيانات Excel. سنتعرف على كل خطوة من خطوات الكود ونشرح كيفية عمله. اتبعي التعليمات بعناية للحصول على النتائج المرجوة.

## الخطوة 1: المتطلبات الأساسية

قبل البدء، تأكد من تثبيت مكتبة Aspose.Cells لـ .NET. يمكنك الحصول عليه من موقع Aspose الرسمي. تأكد أيضًا من أن لديك إصدارًا حديثًا من Visual Studio أو أي بيئة تطوير أخرى لـ C#.

## الخطوة 2: استيراد مساحات الأسماء المطلوبة

لاستخدام مكتبة Aspose.Cells، نحتاج إلى استيراد مساحات الأسماء الضرورية إلى الكود الخاص بنا. أضف الأسطر التالية إلى أعلى ملف مصدر C# الخاص بك:

```csharp
using Aspose.Cells;
```

## الخطوة 3: إنشاء مصنف Excel

في هذه الخطوة، سنقوم بإنشاء مصنف Excel جديد. استخدم الكود التالي لإنشاء مصنف Excel:

```csharp
// المسار إلى دليل المستندات.
string dataDir = "YOUR_DIRECTORY_OF_DOCUMENTS";

// إنشاء مصنف جديد.
Workbook wb = new Workbook();
```

 تأكد من استبدال`"YOUR_DOCUMENTS_DIR"` بالمسار المناسب إلى دليل المستندات الخاص بك.

## الخطوة 4: إنشاء جدول بيانات

الآن بعد أن أنشأنا مصنف Excel، فلنقم بإنشاء ورقة عمل ونحصل على الورقة الأولى. استخدم الكود التالي:

```csharp
// قم بإنشاء كائن جدول بيانات واحصل على الورقة الأولى.
Worksheet sheet = wb.Worksheets[0];
```

## الخطوة 5: تحديد النمط

في هذه الخطوة، سنحدد النمط الذي سيتم تطبيقه على خلايا معينة. استخدم الكود التالي:

```csharp
// تعريف كائن النمط.
Styling styling;
```

## الخطوة 6: قم بالتكرار لفتح جميع الأعمدة

سنقوم الآن بتمرير كافة الأعمدة الموجودة في ورقة العمل وإلغاء قفلها. استخدم الكود التالي:

```csharp
// قم بالمرور عبر كافة الأعمدة الموجودة في ورقة العمل وقم بإلغاء تأمينها.
for (int i = 0; i <= 255; i++)
{
     style = sheet.Cells.Columns[(byte)i].Style;
     style. IsLocked = false;
     sheet.Cells.Columns[(byte)i].ApplyStyle(style);
}
```

## الخطوة 7: قفل خلايا محددة

في هذه الخطوة، سنقوم بقفل خلايا معينة. استخدم الكود التالي:

```csharp
//قفل الخلايا الثلاث... أي A1، B1، C1.
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

وأخيرًا، سنقوم بحماية ورقة العمل لمنع تعديل خلايا معينة. استخدم الكود التالي:

```csharp
// حماية ورقة العمل.
sheet.Protect(ProtectionType.All);
```

## الخطوة 9: حفظ ملف Excel

سنقوم الآن بحفظ ملف Excel المعدل. استخدم الكود التالي:

```csharp
// احفظ ملف إكسل.
wb.Save(dataDir + "output.out.xls", SaveFormat.Excel97To2003);
```

تأكد من تحديد المسار الصحيح لحفظ ملف Excel المعدل.

### نموذج التعليمات البرمجية المصدر لحماية خلايا محددة في ورقة عمل Excel باستخدام Aspose.Cells لـ .NET 
```csharp
//المسار إلى دليل المستندات.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// قم بإنشاء الدليل إذا لم يكن موجودًا بالفعل.
bool IsExists = System.IO.Directory.Exists(dataDir);
if (!IsExists)
    System.IO.Directory.CreateDirectory(dataDir);
// إنشاء مصنف جديد.
Workbook wb = new Workbook();
// قم بإنشاء كائن ورقة عمل واحصل على الورقة الأولى.
Worksheet sheet = wb.Worksheets[0];
// تحديد كائن النمط.
Style style;
// تحديد كائن styleflag
StyleFlag styleflag;
// قم بالمرور عبر كافة الأعمدة الموجودة في ورقة العمل وقم بإلغاء تأمينها.
for (int i = 0; i <= 255; i++)
{
    style = sheet.Cells.Columns[(byte)i].Style;
    style.IsLocked = false;
    styleflag = new StyleFlag();
    styleflag.Locked = true;
    sheet.Cells.Columns[(byte)i].ApplyStyle(style, styleflag);
}
// قفل الخلايا الثلاث...أي A1، B1، C1.
style = sheet.Cells["A1"].GetStyle();
style.IsLocked = true;
sheet.Cells["A1"].SetStyle(style);
style = sheet.Cells["B1"].GetStyle();
style.IsLocked = true;
sheet.Cells["B1"].SetStyle(style);
style = sheet.Cells["C1"].GetStyle();
style.IsLocked = true;
sheet.Cells["C1"].SetStyle(style);
// أخيرًا، قم بحماية الورقة الآن.
sheet.Protect(ProtectionType.All);
// احفظ ملف الاكسل.
wb.Save(dataDir + "output.out.xls", SaveFormat.Excel97To2003);
```


## خاتمة

تهنئة ! لديك الآن كود مصدر C# الذي يسمح لك بحماية خلايا معينة في ورقة عمل Excel باستخدام مكتبة Aspose.Cells لـ .NET. لا تتردد في تخصيص الكود ليناسب احتياجاتك الخاصة.

### الأسئلة الشائعة (الأسئلة المتداولة)

#### هل يعمل هذا الرمز مع الإصدارات الأخيرة من Excel؟

نعم، يعمل هذا الرمز مع الإصدارات الحديثة من Excel، بما في ذلك الملفات بتنسيق Excel 2010 والإصدارات الأحدث.

#### هل يمكنني حماية الخلايا الأخرى إلى جانب الخلايا A1 وB1 وC1؟

نعم، يمكنك تعديل التعليمات البرمجية لقفل خلايا محددة أخرى عن طريق ضبط مراجع الخلايا في سطور التعليمات البرمجية المقابلة.

#### كيف يمكنني فتح الخلايا المقفلة مرة أخرى؟

 يمكنك استخدام`SetStyle` طريقة مع`IsLocked` ضبط ل`false` لفتح الخلايا.

#### هل يمكنني إضافة المزيد من أوراق العمل إلى المصنف؟

 نعم، يمكنك إضافة أوراق عمل أخرى إلى المصنف باستخدام الملف`Worksheets.Add()`الطريقة وكرر خطوات حماية الخلية لكل ورقة عمل.

#### كيف يمكنني تغيير تنسيق الحفظ لملف Excel؟

 يمكنك تغيير تنسيق الحفظ باستخدام`SaveFormat` الطريقة بالتنسيق المطلوب، على سبيل المثال`SaveFormat.Xlsx` لبرنامج Excel 2007 والإصدارات الأحدث.