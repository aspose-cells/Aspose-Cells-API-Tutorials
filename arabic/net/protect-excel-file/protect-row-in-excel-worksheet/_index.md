---
title: حماية الصف في ورقة عمل Excel
linktitle: حماية الصف في ورقة عمل Excel
second_title: Aspose.Cells لمرجع .NET API
description: اكتشف في هذا البرنامج التعليمي كيفية حماية صفوف جدول بيانات Excel باستخدام Aspose.Cells for .NET. تعليمي خطوة بخطوة في C #.
type: docs
weight: 60
url: /ar/net/protect-excel-file/protect-row-in-excel-worksheet/
---
في هذا البرنامج التعليمي ، سنلقي نظرة على بعض التعليمات البرمجية المصدر لـ C # التي تستخدم مكتبة Aspose.Cells لحماية الصفوف في جدول بيانات Excel. سنستعرض كل خطوة في الكود ونوضح كيف يعمل. اتبع التعليمات بعناية للحصول على النتائج المرجوة.

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

في هذه الخطوة ، سنحدد النمط الذي سيتم تطبيقه على صفوف جدول البيانات. استخدم الكود التالي:

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

## الخطوة 7: قفل الخط الأول

في هذه الخطوة ، سنغلق الصف الأول من ورقة العمل. استخدم الكود التالي:

```csharp
// احصل على نمط الخط الأول.
style = sheet.Cells.Rows[0].Style;
// قفل النمط.
style. IsLocked = true;
// قم بتطبيق النمط على السطر الأول.
sheet.Cells.ApplyRowStyle(0, style);
```

## الخطوة 8: حماية ورقة العمل

الآن بعد أن قمنا بتعيين الأنماط وأغلقنا الصفوف ، دعنا نحمي جدول البيانات. استخدم الكود التالي:

```csharp
// حماية ورقة العمل.
sheet.Protect(ProtectionType.All);
```

## الخطوة 9: حفظ ملف Excel

أخيرًا ، سنقوم بحفظ ملف Excel المعدل. استخدم الكود التالي:

```csharp
// احفظ ملف Excel.
wb.Save(dataDir + "output.out.xls", SaveFormat.Excel97To2003);
```

تأكد من تحديد المسار الصحيح لحفظ ملف Excel المعدل.

### نموذج التعليمات البرمجية المصدر لـ Protect Row In Excel Worksheet باستخدام Aspose.Cells for .NET 
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
//تحديد كائن styleflag.
StyleFlag flag;
// قم بالتكرار خلال جميع الأعمدة في ورقة العمل وقم بإلغاء تأمينها.
for (int i = 0; i <= 255; i++)
{
    style = sheet.Cells.Columns[(byte)i].Style;
    style.IsLocked = false;
    flag = new StyleFlag();
    flag.Locked = true;
    sheet.Cells.Columns[(byte)i].ApplyStyle(style, flag);
}
// احصل على نمط الصف الأول.
style = sheet.Cells.Rows[0].Style;
// أغلق.
style.IsLocked = true;
// تجسيد العلم.
flag = new StyleFlag();
// اضبط إعداد القفل.
flag.Locked = true;
// قم بتطبيق النمط على الصف الأول.
sheet.Cells.ApplyRowStyle(0, style, flag);
// احمِ الورقة.
sheet.Protect(ProtectionType.All);
// احفظ ملف اكسل.
wb.Save(dataDir + "output.out.xls", SaveFormat.Excel97To2003);
```

## خاتمة

تهنئة ! لديك الآن كود مصدر C # يسمح لك بحماية الصفوف في جدول بيانات Excel باستخدام مكتبة Aspose.Cells لـ .NET. تأكد من اتباع الخطوات بعناية وتخصيص الكود وفقًا لاحتياجاتك الخاصة.

### أسئلة وأجوبة (أسئلة متكررة)

#### هل يعمل هذا الرمز مع الإصدارات الأخيرة من Excel؟
نعم ، يعمل هذا الرمز مع الإصدارات الحديثة من Excel ، بما في ذلك الملفات بتنسيق Excel 2010 وما فوق.

#### هل يمكنني حماية صفوف معينة فقط بدلاً من كافة الصفوف في ورقة العمل؟
نعم ، يمكنك تعديل الكود لتحديد الصفوف المحددة التي تريد حمايتها. ستحتاج إلى ضبط الحلقة والمؤشرات وفقًا لذلك.

#### كيف يمكنني فتح الخطوط المقفلة مرة أخرى؟
 يمكنك استخدام ال`IsLocked` طريقة`Style` كائن لتعيين القيمة إليه`false` وافتح الصفوف.

#### هل من الممكن حماية أوراق عمل متعددة في نفس مصنف Excel؟
نعم ، يمكنك تكرار خطوات إنشاء ورقة عمل ، وتعيين النمط والحماية لكل ورقة عمل في المصنف.

#### كيف يمكنني تغيير كلمة مرور حماية جدول البيانات؟
 يمكنك تغيير كلمة المرور باستخدام ملف`Protect` طريقة وتحديد كلمة مرور جديدة كوسيطة.