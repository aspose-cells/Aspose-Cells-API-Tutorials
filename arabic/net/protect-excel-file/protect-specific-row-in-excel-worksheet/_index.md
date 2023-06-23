---
title: حماية صف معين في ورقة عمل Excel
linktitle: حماية صف معين في ورقة عمل Excel
second_title: Aspose.Cells لمرجع .NET API
description: حماية صف معين في Excel باستخدام Aspose.Cells for .NET. دليل تفصيلي خطوة بخطوة لتأمين بياناتك السرية.
type: docs
weight: 90
url: /ar/net/protect-excel-file/protect-specific-row-in-excel-worksheet/
---
تعد حماية البيانات السرية في جدول بيانات Excel أمرًا ضروريًا لضمان أمن المعلومات. يوفر Aspose.Cells for .NET حلاً قويًا لحماية صفوف معينة في جدول بيانات Excel. سيرشدك هذا الدليل إلى كيفية حماية صف معين في ورقة عمل Excel باستخدام كود المصدر C # المقدم. اتبع هذه الخطوات البسيطة لإعداد حماية الصفوف في ملفات Excel الخاصة بك.

## الخطوة 1: استيراد المكتبات المطلوبة

للبدء ، تأكد من تثبيت Aspose.Cells for .NET على نظامك. تحتاج أيضًا إلى إضافة المراجع المناسبة في مشروع C # الخاص بك لتتمكن من استخدام وظيفة Aspose.Cells. إليك الكود الخاص باستيراد المكتبات المطلوبة:

```csharp
// أضف المراجع الضرورية
using Aspose.Cells;
```

## الخطوة 2: إنشاء مصنف وجدول بيانات Excel

بعد استيراد المكتبات المطلوبة ، يمكنك إنشاء مصنف Excel جديد وورقة عمل جديدة. هيريس كيفية القيام بذلك:

```csharp
// المسار إلى دليل المستندات.
string dataDir = "YOUR DOCUMENTS DIRECTORY";

// قم بإنشاء دليل إذا لم يكن موجودًا بالفعل.
bool IsExists = System.IO.Directory.Exists(dataDir);
if (!IsExists)
     System.IO.Directory.CreateDirectory(dataDir);

// قم بإنشاء مصنف جديد.
Workbook wb = new Workbook();

// قم بإنشاء كائن جدول بيانات واحصل على الورقة الأولى.
Worksheet sheet = wb.Worksheets[0];
```

## الخطوة 3: إعداد علم النمط والأسلوب

سنقوم الآن بتعيين نمط الخلية وعلم النمط لإلغاء تأمين جميع الأعمدة في ورقة العمل. هذا هو الكود الضروري:

```csharp
// قم بتعيين كائن النمط.
Styling styling;

// قم بتعيين كائن styleflag.
StyleFlag flag;

// قم بالتكرار خلال جميع الأعمدة في ورقة العمل وقم بإلغاء تأمينها.
for (int i = 0; i <= 255; i++)
{
     style = sheet.Cells.Columns[(byte)i].Style;
     style. IsLocked = false;
     flag = new StyleFlag();
     flag. Locked = true;
     sheet.Cells.Columns[(byte)i].ApplyStyle(style, flag);
}
```

## الخطوة 4: حماية الخط المحدد

الآن سنقوم بحماية الصف المحدد في ورقة العمل. سنقوم بإغلاق الصف الأول لمنع أي تعديل. إليك الطريقة:

```csharp
// احصل على نمط الخط الأول.
style = sheet.Cells.Rows[0].Style;

// أغلق.
style. IsLocked = true;

//تجسيد العلم.
flag = new StyleFlag();

// اضبط معلمة القفل.
flag. Locked = true;

// قم بتطبيق النمط على السطر الأول.
sheet.Cells.ApplyRowStyle(0, style, flag);
```

## الخطوة 5: حماية ورقة العمل

أخيرًا ، سنحمي ورقة عمل Excel بأكملها لمنع التعديل غير المصرح به. إليك الطريقة:

```csharp
// حماية ورقة العمل.
sheet.Protect(ProtectionType.All);
```

## الخطوة 6: احفظ ملف Excel المحمي

بمجرد الانتهاء من حماية الصف المحدد في ورقة عمل Excel ، يمكنك حفظ ملف Excel المحمي على نظامك. إليك الطريقة:

```csharp
// احفظ ملف Excel.
wb.Save(dataDir + "output.out.xls", SaveFormat.Excel97To2003);
```

بعد اتباع هذه الخطوات ، ستكون قد نجحت في حماية صف معين في جدول بيانات Excel باستخدام Aspose.Cells for .NET.

### نموذج التعليمات البرمجية المصدر لحماية صف معين في ورقة عمل Excel باستخدام Aspose.Cells for .NET 
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
// تحديد كائن styleflag.
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
//تجسيد العلم.
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

تعد حماية البيانات في ملفات Excel أمرًا بالغ الأهمية لمنع الوصول غير المصرح به أو التعديل غير المرغوب فيه. باستخدام مكتبة Aspose.Cells لـ .NET ، يمكنك بسهولة حماية صفوف معينة في جدول بيانات Excel باستخدام شفرة المصدر C # المتوفرة. اتبع هذا الدليل المفصل خطوة بخطوة لإضافة طبقة أمان إضافية لملفات Excel الخاصة بك.

### أسئلة وأجوبة

#### هل تعمل حماية صف معينة في جميع إصدارات Excel؟

نعم ، تعمل حماية الصفوف المحددة باستخدام Aspose.Cells for .NET في جميع الإصدارات المدعومة من Excel.

#### هل يمكنني حماية عدة صفوف محددة في جدول بيانات Excel؟

نعم ، يمكنك حماية عدة صفوف محددة باستخدام طرق مماثلة موصوفة في هذا الدليل.

#### كيف يمكنني فتح صف معين في جدول بيانات Excel؟

 لإلغاء تأمين صف معين ، يجب عليك تعديل كود المصدر وفقًا لذلك باستخدام ملف`IsLocked` طريقة`Style` هدف.