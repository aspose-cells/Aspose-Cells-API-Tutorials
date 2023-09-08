---
title: حماية الخلايا في ورقة عمل Excel
linktitle: حماية الخلايا في ورقة عمل Excel
second_title: Aspose.Cells لمرجع .NET API
description: تعرف على كيفية حماية خلايا معينة في Excel باستخدام Aspose.Cells لـ .NET. البرنامج التعليمي خطوة بخطوة في C#.
type: docs
weight: 30
url: /ar/net/protect-excel-file/protect-cells-in-excel-worksheet/
---
يعد Microsoft Excel أداة مستخدمة على نطاق واسع لإنشاء جداول البيانات وإدارتها. إحدى ميزات Excel الأساسية هي القدرة على حماية خلايا معينة للحفاظ على سلامة البيانات. في هذا البرنامج التعليمي، سنرشدك خطوة بخطوة لحماية خلايا معينة في جدول بيانات Excel باستخدام Aspose.Cells for .NET. Aspose.Cells for .NET هي مكتبة برمجة قوية تسهل التعامل مع ملفات Excel بمرونة كبيرة وميزات متقدمة. اتبع الخطوات المقدمة لمعرفة كيفية حماية خلاياك المهمة والحفاظ على بياناتك آمنة.

## الخطوة 1: تهيئة البيئة

تأكد من تثبيت Aspose.Cells for .NET في بيئة التطوير الخاصة بك. قم بتنزيل المكتبة من موقع Aspose الرسمي وتحقق من الوثائق للحصول على تعليمات التثبيت.

## الخطوة 2: تهيئة المصنف وورقة العمل

للبدء، نحتاج إلى إنشاء مصنف جديد والحصول على المرجع إلى ورقة العمل حيث نريد حماية الخلايا. استخدم الكود التالي:

```csharp
// المسار إلى دليل المستندات.
string dataDir = "YOUR DOCUMENTS DIRECTORY";
// قم بإنشاء الدليل إذا لم يكن موجودًا بالفعل.
bool exists = System.IO.Directory.Exists(dataDir);
if (! exists)
     System.IO.Directory.CreateDirectory(dataDir);

// إنشاء مصنف جديد
Workbook workbook = new Workbook();

// الحصول على ورقة العمل الأولى
Worksheet sheet = workbook.Worksheets[0];
```

 في مقتطف التعليمات البرمجية هذا، نحدد أولاً المسار إلى الدليل الذي سيتم حفظ ملف Excel فيه. بعد ذلك، نقوم بإنشاء مثيل جديد من`Workbook` class واحصل على المرجع إلى ورقة العمل الأولى باستخدام ملف`Worksheets` ملكية.

## الخطوة 3: تحديد نمط الخلية

الآن نحن بحاجة إلى تحديد نمط الخلايا التي نريد حمايتها. استخدم الكود التالي:

```csharp
// تحديد كائن النمط
Styling styling;

// قم بالمرور عبر كافة الأعمدة في ورقة العمل وقم بإلغاء قفلها
for (int i = 0; i <= 255; i++)
{
     style = sheet.Cells.Columns[(byte)i].Style;
     style. IsLocked = false;
     leaf.Cells.Columns[(byte)i].ApplyStyle(style, new StyleFlag { Locked = true });
}
```

 في هذا الكود، نستخدم حلقة للتنقل عبر جميع الأعمدة في ورقة العمل وإلغاء قفل خلاياها عن طريق ضبط النمط`IsLocked` الملكية ل`false` . نستخدم بعد ذلك`ApplyStyle` طريقة لتطبيق النمط على الأعمدة باستخدام`StyleFlag` العلم لقفل الخلايا.

## الخطوة 4: حماية خلايا محددة

سنقوم الآن بحماية الخلايا المحددة التي نريد قفلها. استخدم الكود التالي:

```csharp
// قفل الخلايا الثلاث: A1، B1، C1
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

 في هذا الكود، نحصل على نمط كل خلية محددة باستخدام`GetStyle` الطريقة، ومن ثم نقوم بتعيين`IsLocked` خاصية الاسلوب ل`true`لقفل الخلية. وأخيرا، نقوم بتطبيق النمط المحدث على كل خلية باستخدام`SetStyle` طريقة.

## الخطوة 5: حماية ورقة العمل

الآن بعد أن قمنا بتعريف الخلايا المراد حمايتها، يمكننا حماية ورقة العمل نفسها. استخدم الكود التالي:

```csharp
// حماية ورقة العمل
leaf.Protect(ProtectionType.All);
```

 يستخدم هذا الرمز`Protect` طريقة لحماية ورقة العمل بنوع الحماية المحدد، في هذه الحالة`ProtectionType.All` الذي يحمي كافة العناصر في ورقة العمل.

## الخطوة 6: احفظ ملف Excel

وأخيرا، نقوم بحفظ ملف Excel مع التغييرات التي تم إجراؤها. استخدم الكود التالي:

```csharp
// احفظ ملف إكسل
workbook.Save(dataDir + "output.xls", SaveFormat.Excel97To2003);
```

 في هذا الكود نستخدم`Save` طريقة لحفظ المصنف في الدليل المحدد بالملحق`Excel97To2003` شكل.

### نموذج التعليمات البرمجية المصدر لحماية الخلايا في ورقة عمل Excel باستخدام Aspose.Cells لـ .NET 
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
wb.Save(dataDir + "output.xls", SaveFormat.Excel97To2003);
```

## خاتمة

تهنئة ! لقد تعلمت كيفية حماية خلايا معينة في جدول بيانات Excel باستخدام Aspose.Cells لـ .NET. يمكنك الآن تطبيق هذه التقنية في مشاريعك الخاصة وتحسين أمان ملفات Excel الخاصة بك.


### الأسئلة الشائعة

#### س: لماذا يجب علي استخدام Aspose.Cells لـ .NET لحماية الخلايا في جدول بيانات Excel؟

ج: Aspose.Cells for .NET هي مكتبة قوية تسهل العمل مع ملفات Excel. يوفر ميزات متقدمة لحماية الخلايا وفتح النطاقات وما إلى ذلك.

#### س: هل من الممكن حماية نطاقات من الخلايا بدلاً من الخلايا الفردية؟

 ج: نعم، يمكنك تحديد نطاقات خلايا معينة لحمايتها باستخدام`ApplyStyle` الطريقة مع المناسبة`StyleFlag`.

#### س: كيف يمكنني فتح ملف Excel المحمي بعد حفظه؟

ج: عند فتح ملف Excel المحمي، ستحتاج إلى توفير كلمة المرور المحددة عند حماية ورقة العمل.

#### س: هل هناك أنواع أخرى من الحماية يمكنني تطبيقها على جدول بيانات Excel؟

ج: نعم، يدعم Aspose.Cells for .NET أنواعًا متعددة من الحماية، مثل حماية البنية وحماية النوافذ وما إلى ذلك. ويمكنك اختيار نوع الحماية المناسب وفقًا لاحتياجاتك.