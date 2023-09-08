---
title: حماية صف معين في ورقة عمل Excel
linktitle: حماية صف معين في ورقة عمل Excel
second_title: Aspose.Cells لمرجع .NET API
description: قم بحماية صف معين في Excel باستخدام Aspose.Cells لـ .NET. دليل خطوة بخطوة لتأمين بياناتك السرية.
type: docs
weight: 90
url: /ar/net/protect-excel-file/protect-specific-row-in-excel-worksheet/
---
تعد حماية البيانات السرية في جدول بيانات Excel أمرًا ضروريًا لضمان أمن المعلومات. يقدم Aspose.Cells for .NET حلاً قويًا لحماية صفوف معينة في جدول بيانات Excel. سيرشدك هذا الدليل إلى كيفية حماية صف معين في ورقة عمل Excel باستخدام كود مصدر C# المتوفر. اتبع هذه الخطوات البسيطة لإعداد حماية الصف في ملفات Excel الخاصة بك.

## الخطوة 1: استيراد المكتبات المطلوبة

للبدء، تأكد من تثبيت Aspose.Cells for .NET على نظامك. تحتاج أيضًا إلى إضافة المراجع المناسبة في مشروع C# الخاص بك لتتمكن من استخدام وظيفة Aspose.Cells. إليك الكود لاستيراد المكتبات المطلوبة:

```csharp
// أضف المراجع اللازمة
using Aspose.Cells;
```

## الخطوة 2: إنشاء مصنف Excel وجدول البيانات

بعد استيراد المكتبات المطلوبة، يمكنك إنشاء مصنف Excel جديد وورقة عمل جديدة. هيريس كيفية القيام بذلك:

```csharp
//المسار إلى دليل المستندات.
string dataDir = "YOUR DOCUMENTS DIRECTORY";

// قم بإنشاء دليل إذا لم يكن موجودًا بالفعل.
bool IsExists = System.IO.Directory.Exists(dataDir);
if (!IsExists)
     System.IO.Directory.CreateDirectory(dataDir);

// إنشاء مصنف جديد.
Workbook wb = new Workbook();

// قم بإنشاء كائن جدول بيانات واحصل على الورقة الأولى.
Worksheet sheet = wb.Worksheets[0];
```

## الخطوة 3: تحديد النمط وعلامة النمط

سنقوم الآن بتعيين نمط الخلية وعلامة النمط لفتح جميع الأعمدة في ورقة العمل. هنا هو الكود الضروري:

```csharp
// قم بتعيين كائن النمط.
Styling styling;

// قم بتعيين كائن styleflag.
StyleFlag flag;

// قم بالمرور عبر كافة الأعمدة في ورقة العمل وقم بإلغاء قفلها.
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

الآن سنقوم بحماية الصف المحدد في ورقة العمل. سنقوم بقفل الصف الأول لمنع أي تعديل. إليك الطريقة:

```csharp
// احصل على نمط السطر الأول.
style = sheet.Cells.Rows[0].Style;

// أغلق.
style. IsLocked = true;

//إنشاء مثيل للعلم.
flag = new StyleFlag();

// قم بتعيين معلمة القفل.
flag. Locked = true;

// تطبيق النمط على السطر الأول.
sheet.Cells.ApplyRowStyle(0, style, flag);
```

## الخطوة 5: حماية ورقة العمل

وأخيرًا، سنقوم بحماية ورقة عمل Excel بأكملها لمنع التعديل غير المصرح به. إليك الطريقة:

```csharp
// حماية ورقة العمل.
sheet.Protect(ProtectionType.All);
```

## الخطوة 6: احفظ ملف Excel المحمي

بمجرد الانتهاء من حماية صف معين في ورقة عمل Excel، يمكنك حفظ ملف Excel المحمي على نظامك. إليك الطريقة:

```csharp
// احفظ ملف إكسل.
wb.Save(dataDir + "output.out.xls", SaveFormat.Excel97To2003);
```

بعد اتباع هذه الخطوات، ستكون قد نجحت في حماية صف معين في جدول بيانات Excel الخاص بك باستخدام Aspose.Cells for .NET.

### نموذج التعليمات البرمجية المصدر لحماية صف معين في ورقة عمل Excel باستخدام Aspose.Cells لـ .NET 
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
// تحديد كائن styleflag.
StyleFlag flag;
// قم بالمرور عبر كافة الأعمدة الموجودة في ورقة العمل وقم بإلغاء تأمينها.
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
//إنشاء مثيل للعلم.
flag = new StyleFlag();
// اضبط إعداد القفل.
flag.Locked = true;
// قم بتطبيق النمط على الصف الأول.
sheet.Cells.ApplyRowStyle(0, style, flag);
// حماية الورقة.
sheet.Protect(ProtectionType.All);
// احفظ ملف الاكسل.
wb.Save(dataDir + "output.out.xls", SaveFormat.Excel97To2003);
```

## خاتمة

تعد حماية البيانات في ملفات Excel أمرًا ضروريًا لمنع الوصول غير المصرح به أو التعديل غير المرغوب فيه. باستخدام مكتبة Aspose.Cells لـ .NET، يمكنك بسهولة حماية صفوف معينة في جدول بيانات Excel باستخدام كود مصدر C# المتوفر. اتبع هذا الدليل خطوة بخطوة لإضافة طبقة إضافية من الأمان إلى ملفات Excel الخاصة بك.

### الأسئلة الشائعة

#### هل تعمل حماية صف معين في كافة إصدارات Excel؟

نعم، تعمل حماية صف معين باستخدام Aspose.Cells for .NET في كافة إصدارات Excel المدعومة.

#### هل يمكنني حماية عدة صفوف محددة في جدول بيانات Excel؟

نعم، يمكنك حماية عدة صفوف محددة باستخدام طرق مشابهة موضحة في هذا الدليل.

#### كيف يمكنني فتح صف معين في جدول بيانات Excel؟

 لفتح صف معين، يجب عليك تعديل كود المصدر وفقًا لذلك باستخدام`IsLocked` طريقة`Style` هدف.