---
title: حماية العمود في ورقة عمل Excel
linktitle: حماية العمود في ورقة عمل Excel
second_title: Aspose.Cells لمرجع .NET API
description: تعرف على كيفية حماية عمود معين في Excel باستخدام Aspose.Cells for .NET. وشملت خطوات مفصلة وكود المصدر.
type: docs
weight: 40
url: /ar/net/protect-excel-file/protect-column-in-excel-worksheet/
---
يعد Microsoft Excel تطبيقًا شائعًا لإدارة البيانات وتحليلها في شكل جداول بيانات. حماية البيانات الحساسة أمر ضروري لضمان سلامة وسرية المعلومات. في هذا البرنامج التعليمي ، سنوجهك خطوة بخطوة لحماية عمود معين في جدول بيانات Excel باستخدام مكتبة Aspose.Cells for .NET. يوفر Aspose.Cells for .NET ميزات قوية للتعامل مع ملفات Excel وحمايتها. اتبع الخطوات المقدمة لمعرفة كيفية حماية بياناتك في عمود معين وتأمين جدول بيانات Excel الخاص بك.
## الخطوة 1: إعداد الدليل

ابدأ بتحديد الدليل الذي تريد حفظ ملف Excel فيه. استخدم الكود التالي:

```csharp
// المسار إلى دليل المستندات.
string dataDir = "YOUR DOCUMENTS DIRECTORY";
// قم بإنشاء الدليل إذا لم يكن موجودًا.
bool exists = System.IO.Directory.Exists(dataDir);
if (! exists)
     System.IO.Directory.CreateDirectory(dataDir);
```

يتحقق هذا الرمز مما إذا كان الدليل موجودًا بالفعل ويقوم بإنشائه إذا لم يكن كذلك.

## الخطوة 2: إنشاء مصنف جديد

بعد ذلك ، سننشئ مصنف Excel جديدًا ونحصل على ورقة العمل الأولى. استخدم الكود التالي:

```csharp
// قم بإنشاء مصنف جديد.
Workbook workbook = new Workbook();
// قم بإنشاء كائن جدول بيانات واحصل على الورقة الأولى.
Worksheet sheet = workbook.Worksheets[0];
```

 هذا الرمز يخلق ملف`Workbook` كائن ويحصل على ورقة العمل الأولى باستخدام`Worksheets[0]`.

## الخطوة 3: فتح الأعمدة

لإلغاء تأمين جميع الأعمدة في ورقة العمل ، سنستخدم حلقة للتكرار عبر جميع الأعمدة وتطبيق نمط إلغاء القفل. استخدم الكود التالي:

```csharp
// تعيين كائن النمط.
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
     leaf.Cells.Columns[(byte)i].ApplyStyle(style, flag);
}
```

 يتكرر هذا الرمز عبر كل عمود في ورقة العمل ويفتح النمط عن طريق الإعداد`IsLocked` ل`false`.

## الخطوة 4: قفل عمود معين

سنقوم الآن بقفل عمود معين من خلال تطبيق نمط مغلق. استخدم الكود التالي:

```csharp
// احصل على نمط العمود الأول.
style = sheet.Cells.Columns[0].Style;
// أغلق.
style. IsLocked = true;
// إنشاء كائن العلم.
flag = new StyleFlag();
// اضبط معلمة القفل.
flag. Locked = true;
// قم بتطبيق النمط على العمود الأول.
sheet.Cells.Columns[0].ApplyStyle(style, flag);
```

 هذا الرمز يختار العمود الأول باستخدام`Columns[0]` ، ثم يحدد النمط`IsLocked` ل`true` لقفل العمود. أخيرًا ، نطبق النمط على العمود الأول باستخدام`ApplyStyle` طريقة.

## الخطوة 5: حماية ورقة العمل

الآن وقد أغلقنا العمود المحدد ، يمكننا حماية ورقة العمل نفسها. استخدم الكود التالي:



```csharp
// حماية ورقة العمل.
leaf.Protect(ProtectionType.All);
```

 يستخدم هذا الرمز الامتداد`Protect` طريقة لحماية ورقة العمل من خلال تحديد نوع الحماية.

## الخطوة 6: حفظ ملف Excel

أخيرًا ، نحفظ ملف Excel باستخدام مسار الدليل المطلوب واسم الملف. استخدم الكود التالي:

```csharp
// احفظ ملف Excel.
workbook.Save(dataDir + "output.out.xls", SaveFormat.Excel97To2003);
```

 يستخدم هذا الرمز الامتداد`Save` طريقة`Workbook` كائن لحفظ ملف Excel بالاسم وتنسيق الملف المحددين.

### نموذج التعليمات البرمجية المصدر لـ Protect Column In Excel Worksheet باستخدام Aspose.Cells for .NET 
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
// احصل على نمط العمود الأول.
style = sheet.Cells.Columns[0].Style;
// أغلق.
style.IsLocked = true;
//تجسيد العلم.
flag = new StyleFlag();
// اضبط إعداد القفل.
flag.Locked = true;
// قم بتطبيق النمط على العمود الأول.
sheet.Cells.Columns[0].ApplyStyle(style, flag);
// احمِ الورقة.
sheet.Protect(ProtectionType.All);
// احفظ ملف اكسل.
wb.Save(dataDir + "output.out.xls", SaveFormat.Excel97To2003);
```

## خاتمة

لقد اتبعت للتو درسًا تعليميًا خطوة بخطوة لحماية عمود في جدول بيانات Excel باستخدام Aspose.Cells for .NET. لقد تعلمت كيفية فتح جميع الأعمدة وتأمين عمود معين وحماية ورقة العمل نفسها. يمكنك الآن تطبيق هذه المفاهيم على مشاريعك الخاصة وتأمين بيانات Excel الخاصة بك.

## أسئلة مكررة

#### س: ما سبب أهمية حماية أعمدة معينة في جدول بيانات Excel؟

ج: تساعد حماية أعمدة معينة في جدول بيانات Excel في تقييد الوصول إلى البيانات الحساسة وتعديلها ، وبالتالي ضمان سلامة المعلومات وسريتها.

#### س: هل يدعم Aspose.Cells for .NET ميزات أخرى للتعامل مع ملفات Excel؟

ج: نعم ، تقدم Aspose.Cells for .NET مجموعة كبيرة من الميزات بما في ذلك إنشاء ملفات Excel وتحريرها وتحويلها والإبلاغ عنها.

#### س: كيف يمكنني فتح جميع الأعمدة في جدول بيانات Excel؟

ج: في Aspose.Cells for .NET ، يمكنك استخدام حلقة للتكرار خلال جميع الأعمدة وتعيين نمط القفل على "false" لفتح جميع الأعمدة.

#### س: كيف يمكنني حماية جدول بيانات Excel باستخدام Aspose.Cells for .NET؟

 ج: يمكنك استخدام ملف`Protect` طريقة كائن ورقة العمل لحماية الورقة بمستويات مختلفة من الحماية مثل حماية الهيكل وحماية الخلية وما إلى ذلك.

#### س: هل يمكنني تطبيق مفاهيم حماية الأعمدة هذه في أنواع أخرى من ملفات Excel؟

ج: نعم ، تنطبق مفاهيم حماية العمود في Aspose.Cells for .NET على جميع أنواع ملفات Excel ، مثل ملفات Excel 97-2003 (.xls) وملفات Excel الأحدث (.xlsx).