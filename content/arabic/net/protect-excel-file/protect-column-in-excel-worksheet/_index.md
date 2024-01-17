---
title: حماية العمود في ورقة عمل Excel
linktitle: حماية العمود في ورقة عمل Excel
second_title: Aspose.Cells لمرجع .NET API
description: تعرف على كيفية حماية عمود معين في Excel باستخدام Aspose.Cells لـ .NET. تم تضمين الخطوات التفصيلية وكود المصدر.
type: docs
weight: 40
url: /ar/net/protect-excel-file/protect-column-in-excel-worksheet/
---
يعد Microsoft Excel تطبيقًا شائعًا لإدارة وتحليل البيانات في شكل جداول بيانات. تعد حماية البيانات الحساسة أمرًا ضروريًا لضمان سلامة المعلومات وسريتها. في هذا البرنامج التعليمي، سنرشدك خطوة بخطوة لحماية عمود معين في جدول بيانات Excel باستخدام مكتبة Aspose.Cells for .NET. يوفر Aspose.Cells for .NET ميزات قوية للتعامل مع ملفات Excel وحمايتها. اتبع الخطوات المقدمة لمعرفة كيفية حماية بياناتك في عمود معين وتأمين جدول بيانات Excel الخاص بك.
## الخطوة 1: إعداد الدليل

ابدأ بتحديد الدليل الذي تريد حفظ ملف Excel فيه. استخدم الكود التالي:

```csharp
//المسار إلى دليل المستندات.
string dataDir = "YOUR DOCUMENTS DIRECTORY";
// قم بإنشاء الدليل إذا لم يكن موجودا.
bool exists = System.IO.Directory.Exists(dataDir);
if (! exists)
     System.IO.Directory.CreateDirectory(dataDir);
```

يتحقق هذا الرمز مما إذا كان الدليل موجودًا بالفعل ويقوم بإنشائه إذا لم يكن كذلك.

## الخطوة 2: إنشاء مصنف جديد

بعد ذلك، سنقوم بإنشاء مصنف Excel جديد والحصول على ورقة العمل الأولى. استخدم الكود التالي:

```csharp
// إنشاء مصنف جديد.
Workbook workbook = new Workbook();
// قم بإنشاء كائن جدول بيانات واحصل على الورقة الأولى.
Worksheet sheet = workbook.Worksheets[0];
```

 يقوم هذا الرمز بإنشاء ملف جديد`Workbook` كائن ويحصل على ورقة العمل الأولى باستخدام`Worksheets[0]`.

## الخطوة 3: فتح الأعمدة

لإلغاء قفل جميع الأعمدة في ورقة العمل، سنستخدم حلقة للتنقل عبر جميع الأعمدة وتطبيق نمط إلغاء القفل. استخدم الكود التالي:

```csharp
// تعيين كائن النمط.
Styling styling;
// قم بتعيين كائن styleflag.
StyleFlag flag;
// قم بالمرور عبر كافة الأعمدة في ورقة العمل وقم بإلغاء تأمينها.
for (int i = 0; i <= 255; i++)
{
     style = sheet.Cells.Columns[(byte)i].Style;
     style. IsLocked = false;
     flag = new StyleFlag();
     flag. Locked = true;
     leaf.Cells.Columns[(byte)i].ApplyStyle(style, flag);
}
```

 يتكرر هذا الرمز خلال كل عمود في ورقة العمل ويفتح النمط عن طريق الإعداد`IsLocked` ل`false`.

## الخطوة 4: قفل عمود معين

سنقوم الآن بقفل عمود معين من خلال تطبيق نمط مقفل. استخدم الكود التالي:

```csharp
// احصل على نمط العمود الأول.
style = sheet.Cells.Columns[0].Style;
// أغلق.
style. IsLocked = true;
// إنشاء مثيل لكائن العلم.
flag = new StyleFlag();
// قم بتعيين معلمة القفل.
flag. Locked = true;
// تطبيق النمط على العمود الأول.
sheet.Cells.Columns[0].ApplyStyle(style, flag);
```

 يحدد هذا الرمز العمود الأول باستخدام`Columns[0]` ، ثم يقوم بتعيين النمط`IsLocked` ل`true` لقفل العمود. وأخيرا، نقوم بتطبيق النمط على العمود الأول باستخدام`ApplyStyle` طريقة.

## الخطوة 5: حماية ورقة العمل

الآن بعد أن قمنا بتأمين العمود المحدد، يمكننا حماية ورقة العمل نفسها. استخدم الكود التالي:



```csharp
// حماية ورقة العمل.
leaf.Protect(ProtectionType.All);
```

 يستخدم هذا الرمز`Protect` طريقة لحماية ورقة العمل من خلال تحديد نوع الحماية.

## الخطوة 6: حفظ ملف Excel

وأخيرًا، نقوم بحفظ ملف Excel باستخدام مسار الدليل واسم الملف المطلوبين. استخدم الكود التالي:

```csharp
// احفظ ملف إكسل.
workbook.Save(dataDir + "output.out.xls", SaveFormat.Excel97To2003);
```

 يستخدم هذا الرمز`Save` طريقة`Workbook` كائن لحفظ ملف Excel بالاسم وتنسيق الملف المحددين.

### نموذج التعليمات البرمجية المصدر لحماية العمود في ورقة عمل Excel باستخدام Aspose.Cells لـ .NET 
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
// قم بالمرور عبر كافة الأعمدة الموجودة في ورقة العمل وقم بإلغاء قفلها.
for (int i = 0; i <= 255; i++)
{
    style = sheet.Cells.Columns[(byte)i].Style;
    style.IsLocked = false;
    flag = new StyleFlag();
    flag.Locked = true;
    sheet.Cells.Columns[(byte)i].ApplyStyle(style, flag);
}
// احصل على نمط العمود الأول.
style = sheet.Cells.Columns[0].Style;
// أغلق.
style.IsLocked = true;
//إنشاء مثيل للعلم.
flag = new StyleFlag();
// اضبط إعداد القفل.
flag.Locked = true;
// تطبيق النمط على العمود الأول.
sheet.Cells.Columns[0].ApplyStyle(style, flag);
// حماية الورقة.
sheet.Protect(ProtectionType.All);
// احفظ ملف الاكسل.
wb.Save(dataDir + "output.out.xls", SaveFormat.Excel97To2003);
```

## خاتمة

لقد اتبعت للتو برنامجًا تعليميًا خطوة بخطوة لحماية عمود في جدول بيانات Excel باستخدام Aspose.Cells for .NET. لقد تعلمت كيفية إلغاء تأمين كافة الأعمدة، وتأمين عمود معين، وحماية ورقة العمل نفسها. يمكنك الآن تطبيق هذه المفاهيم على مشاريعك الخاصة وتأمين بيانات Excel الخاصة بك.

## أسئلة مكررة

#### س: لماذا من المهم حماية أعمدة معينة في جدول بيانات Excel؟

ج: تساعد حماية أعمدة محددة في جدول بيانات Excel على تقييد الوصول إلى البيانات الحساسة وتعديلها، وبالتالي ضمان سلامة المعلومات وسريتها.

#### س: هل يدعم Aspose.Cells for .NET ميزات أخرى للتعامل مع ملفات Excel؟

ج: نعم، يقدم Aspose.Cells for .NET نطاقًا واسعًا من الميزات بما في ذلك إنشاء ملفات Excel وتحريرها وتحويلها وإعداد التقارير عنها.

#### س: كيف يمكنني فتح جميع الأعمدة في جدول بيانات Excel؟

ج: في Aspose.Cells for .NET، يمكنك استخدام حلقة للتكرار عبر كافة الأعمدة وتعيين نمط القفل على "خطأ" لإلغاء تأمين كافة الأعمدة.

#### س: كيف يمكنني حماية جدول بيانات Excel باستخدام Aspose.Cells لـ .NET؟

 ج: يمكنك استخدام`Protect` طريقة كائن ورقة العمل لحماية الورقة بمستويات مختلفة من الحماية مثل حماية البنية، وحماية الخلية، وما إلى ذلك.

#### س: هل يمكنني تطبيق مفاهيم حماية الأعمدة هذه في أنواع أخرى من ملفات Excel؟

ج: نعم، تنطبق مفاهيم حماية الأعمدة في Aspose.Cells لـ .NET على كافة أنواع ملفات Excel، مثل ملفات Excel 97-2003 (.xls) وملفات Excel الأحدث (.xlsx).