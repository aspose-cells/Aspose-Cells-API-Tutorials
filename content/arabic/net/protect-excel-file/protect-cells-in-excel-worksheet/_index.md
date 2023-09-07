---
title: حماية الخلايا في ورقة عمل Excel
linktitle: حماية الخلايا في ورقة عمل Excel
second_title: Aspose.Cells لمرجع .NET API
description: تعرف على كيفية حماية خلايا معينة في Excel باستخدام Aspose.Cells for .NET. تعليمي خطوة بخطوة في C #.
type: docs
weight: 30
url: /ar/net/protect-excel-file/protect-cells-in-excel-worksheet/
---
يعد Microsoft Excel أداة مستخدمة على نطاق واسع لإنشاء جداول البيانات وإدارتها. تتمثل إحدى ميزات Excel الأساسية في القدرة على حماية خلايا معينة للحفاظ على تكامل البيانات. في هذا البرنامج التعليمي ، سنوجهك خطوة بخطوة لحماية خلايا معينة في جدول بيانات Excel باستخدام Aspose.Cells for .NET. Aspose.Cells for .NET مكتبة برمجة قوية تجعل من السهل التعامل مع ملفات Excel بمرونة كبيرة وميزات متقدمة. اتبع الخطوات المقدمة لمعرفة كيفية حماية خلاياك المهمة والحفاظ على أمان بياناتك.

## الخطوة الأولى: تهيئة البيئة

تأكد من تثبيت Aspose.Cells for .NET في بيئة التطوير لديك. قم بتنزيل المكتبة من موقع Aspose الرسمي وتحقق من الوثائق للحصول على تعليمات التثبيت.

## الخطوة 2: تهيئة المصنف وورقة العمل

للبدء ، نحتاج إلى إنشاء مصنف جديد والحصول على المرجع إلى ورقة العمل حيث نريد حماية الخلايا. استخدم الكود التالي:

```csharp
// المسار إلى دليل المستندات.
string dataDir = "YOUR DOCUMENTS DIRECTORY";
// قم بإنشاء الدليل إذا لم يكن موجودًا بالفعل.
bool exists = System.IO.Directory.Exists(dataDir);
if (! exists)
     System.IO.Directory.CreateDirectory(dataDir);

//قم بإنشاء مصنف جديد
Workbook workbook = new Workbook();

// احصل على ورقة العمل الأولى
Worksheet sheet = workbook.Worksheets[0];
```

 في مقتطف الشفرة هذا ، نحدد أولاً المسار إلى الدليل حيث سيتم حفظ ملف Excel. بعد ذلك ، نقوم بإنشاء مثيل جديد من`Workbook` class واحصل على المرجع إلى ورقة العمل الأولى باستخدام`Worksheets` ملكية.

## الخطوة 3: تحديد نمط الخلية

نحتاج الآن إلى تحديد نمط الخلايا التي نريد حمايتها. استخدم الكود التالي:

```csharp
// تحديد كائن النمط
Styling styling;

// قم بالتكرار خلال جميع الأعمدة في ورقة العمل وقم بإلغاء تأمينها
for (int i = 0; i <= 255; i++)
{
     style = sheet.Cells.Columns[(byte)i].Style;
     style. IsLocked = false;
     leaf.Cells.Columns[(byte)i].ApplyStyle(style, new StyleFlag { Locked = true });
}
```

 في هذا الكود ، نستخدم حلقة للتكرار عبر جميع الأعمدة في ورقة العمل وفتح خلاياها عن طريق تعيين النمط`IsLocked` الملكية ل`false` . ثم نستخدم ملف`ApplyStyle` طريقة لتطبيق النمط على الأعمدة ذات الامتداد`StyleFlag` علم لقفل الخلايا.

## الخطوة 4: حماية خلايا معينة

الآن سنقوم بحماية الخلايا المحددة التي نريد قفلها. استخدم الكود التالي:

```csharp
// قفل الخلايا الثلاث: A1 ، B1 ، C1
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

 في هذا الكود ، نحصل على نمط كل خلية محددة باستخدام`GetStyle` الطريقة ، ثم قمنا بتعيين ملف`IsLocked` ملكية النمط ل`true`لقفل الخلية. أخيرًا ، نطبق النمط المحدث على كل خلية باستخدام`SetStyle` طريقة.

## الخطوة 5: حماية ورقة العمل

الآن بعد أن حددنا الخلايا المطلوب حمايتها ، يمكننا حماية ورقة العمل نفسها. استخدم الكود التالي:

```csharp
// حماية ورقة العمل
leaf.Protect(ProtectionType.All);
```

 يستخدم هذا الرمز الامتداد`Protect` طريقة لحماية ورقة العمل بنوع الحماية المحدد ، في هذه الحالة`ProtectionType.All` الذي يحمي كافة العناصر الموجودة في ورقة العمل.

## الخطوة 6: احفظ ملف Excel

أخيرًا ، نحفظ ملف Excel بالتغييرات التي تم إجراؤها. استخدم الكود التالي:

```csharp
// احفظ ملف Excel
workbook.Save(dataDir + "output.xls", SaveFormat.Excel97To2003);
```

 في هذا الكود ، نستخدم الامتداد`Save` طريقة لحفظ المصنف في الدليل المحدد بامتداد`Excel97To2003` شكل.

### نموذج التعليمات البرمجية المصدر لحماية الخلايا في ورقة عمل Excel باستخدام Aspose.Cells for .NET 
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
// أخيرًا ، قم بحماية الورقة الآن.
sheet.Protect(ProtectionType.All);
// احفظ ملف اكسل.
wb.Save(dataDir + "output.xls", SaveFormat.Excel97To2003);
```

## خاتمة

تهنئة ! لقد تعلمت كيفية حماية خلايا معينة في جدول بيانات Excel باستخدام Aspose.Cells for .NET. يمكنك الآن تطبيق هذه التقنية في مشاريعك الخاصة وتحسين أمان ملفات Excel الخاصة بك.


### أسئلة وأجوبة

#### س: لماذا يجب علي استخدام Aspose.Cells لـ .NET لحماية الخلايا في جدول بيانات Excel؟

ج: Aspose.Cells for .NET مكتبة قوية تسهل العمل مع ملفات Excel. يوفر ميزات متقدمة لحماية الخلايا وفتح النطاقات وما إلى ذلك.

#### س: هل من الممكن حماية نطاقات من الخلايا بدلاً من الخلايا الفردية؟

 ج: نعم ، يمكنك تحديد نطاقات خلايا معينة للحماية باستخدام`ApplyStyle` بطريقة مناسبة`StyleFlag`.

#### س: كيف يمكنني فتح ملف اكسل المحمي بعد حفظه؟

ج: عند فتح ملف Excel المحمي ، ستحتاج إلى توفير كلمة المرور المحددة عند حماية ورقة العمل.

#### س: هل هناك أنواع أخرى من الحماية يمكنني تطبيقها على جدول بيانات Excel؟

ج: نعم ، يدعم Aspose.Cells for .NET أنواعًا متعددة من الحماية ، مثل حماية الهيكل وحماية النوافذ وما إلى ذلك. يمكنك اختيار نوع الحماية المناسب وفقًا لاحتياجاتك.