---
title: إعدادات الحماية المتقدمة لورقة عمل Excel
linktitle: إعدادات الحماية المتقدمة لورقة عمل Excel
second_title: Aspose.Cells لمرجع .NET API
description: قم بحماية ملفات Excel الخاصة بك عن طريق ضبط إعدادات الحماية المتقدمة باستخدام Aspose.Cells لـ .NET.
type: docs
weight: 10
url: /ar/net/excel-security/advanced-protection-settings-for-excel-worksheet/
---
في هذا البرنامج التعليمي، سنرشدك خلال الخطوات اللازمة لتعيين إعدادات الحماية المتقدمة لجدول بيانات Excel باستخدام مكتبة Aspose.Cells لـ .NET. اتبع الإرشادات أدناه لإكمال هذه المهمة.

## الخطوة 1: التحضير

تأكد من تثبيت Aspose.Cells لـ .NET وإنشاء مشروع C# في بيئة التطوير المتكاملة المفضلة لديك (IDE).

## الخطوة 2: قم بتعيين مسار دليل المستند

 أعلن أ`dataDir` متغير وقم بتهيئته بالمسار إلى دليل المستندات الخاص بك. على سبيل المثال :

```csharp
string dataDir = "YOUR_DIRECTORY_OF_DOCUMENTS";
```

 تأكد من استبدال`"YOUR_DOCUMENTS_DIRECTORY"` مع المسار الفعلي إلى الدليل الخاص بك.

## الخطوة 3: إنشاء دفق ملف لفتح ملف Excel

 إنشاء`FileStream` كائن يحتوي على ملف Excel المراد فتحه:

```csharp
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
```

 تأكد من أن لديك ملف Excel`book1.xls` في دليل المستندات الخاص بك أو حدد اسم الملف الصحيح وموقعه.

## الخطوة 4: إنشاء مثيل لكائن مصنف وفتح ملف Excel

 استخدم ال`Workbook`فئة من Aspose.Cells لإنشاء كائن Workbook وفتح ملف Excel المحدد عبر دفق الملف:

```csharp
Workbook excel = new Workbook(fstream);
```

## الخطوة 5: الوصول إلى ورقة العمل الأولى

انتقل إلى ورقة العمل الأولى من ملف Excel:

```csharp
Worksheet worksheet = excel.Worksheets[0];
```

## الخطوة 6: ضبط إعدادات حماية ورقة العمل

استخدم خصائص كائن ورقة العمل لتعيين إعدادات حماية ورقة العمل حسب الحاجة. على سبيل المثال :

```csharp
worksheet.Protection.AllowDeletingColumn = false;
worksheet.Protection.AllowDeletingRow = false;
worksheet.Protection.AllowEditingContent = false;
worksheet.Protection.AllowEditingObject = false;
// ... قم بضبط إعدادات الحماية الأخرى حسب الحاجة...
```

## الخطوة 7: احفظ ملف Excel المعدل

 احفظ ملف Excel المعدل باستخدام ملف`Save` طريقة كائن المصنف:

```csharp
excel.Save(dataDir + "output.xls", SaveFormat.Excel97To2003);
```

تأكد من تحديد المسار واسم الملف المطلوبين لملف الإخراج.

## الخطوة 8: أغلق دفق الملف

بمجرد الحفظ، أغلق دفق الملف لتحرير جميع الموارد المرتبطة:

```csharp
fstream.Close();
```
	
### نموذج التعليمات البرمجية المصدر لإعدادات الحماية المتقدمة لورقة عمل Excel باستخدام Aspose.Cells لـ .NET 
```csharp
//المسار إلى دليل المستندات.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// إنشاء دفق ملف يحتوي على ملف Excel المراد فتحه
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
// إنشاء مثيل لكائن المصنف
// فتح ملف Excel من خلال دفق الملف
Workbook excel = new Workbook(fstream);
// الوصول إلى ورقة العمل الأولى في ملف Excel
Worksheet worksheet = excel.Worksheets[0];
// تقييد المستخدمين لحذف أعمدة ورقة العمل
worksheet.Protection.AllowDeletingColumn = false;
// تقييد المستخدمين لحذف صف من ورقة العمل
worksheet.Protection.AllowDeletingRow = false;
// تقييد المستخدمين لتحرير محتويات ورقة العمل
worksheet.Protection.AllowEditingContent = false;
// تقييد المستخدمين لتحرير كائنات ورقة العمل
worksheet.Protection.AllowEditingObject = false;
// تقييد المستخدمين لتحرير سيناريوهات ورقة العمل
worksheet.Protection.AllowEditingScenario = false;
//تقييد المستخدمين للتصفية
worksheet.Protection.AllowFiltering = false;
// السماح للمستخدمين بتنسيق خلايا ورقة العمل
worksheet.Protection.AllowFormattingCell = true;
// السماح للمستخدمين بتنسيق صفوف ورقة العمل
worksheet.Protection.AllowFormattingRow = true;
// السماح للمستخدمين بإدراج أعمدة في ورقة العمل
worksheet.Protection.AllowFormattingColumn = true;
// السماح للمستخدمين بإدراج الارتباطات التشعبية في ورقة العمل
worksheet.Protection.AllowInsertingHyperlink = true;
// السماح للمستخدمين بإدراج صفوف في ورقة العمل
worksheet.Protection.AllowInsertingRow = true;
// السماح للمستخدمين بتحديد الخلايا المقفلة في ورقة العمل
worksheet.Protection.AllowSelectingLockedCell = true;
// السماح للمستخدمين بتحديد الخلايا غير المؤمّنة في ورقة العمل
worksheet.Protection.AllowSelectingUnlockedCell = true;
// السماح للمستخدمين بالفرز
worksheet.Protection.AllowSorting = true;
// السماح للمستخدمين باستخدام الجداول المحورية في ورقة العمل
worksheet.Protection.AllowUsingPivotTable = true;
// حفظ ملف Excel المعدل
excel.Save(dataDir + "output.xls", SaveFormat.Excel97To2003);
// إغلاق دفق الملف لتحرير كافة الموارد
fstream.Close();
```

## خاتمة

تهنئة ! لقد تعلمت الآن كيفية تعيين إعدادات الحماية المتقدمة لجدول بيانات Excel باستخدام Aspose.Cells لـ .NET. استخدم هذه المعرفة لتأمين ملفات Excel الخاصة بك وتقييد إجراءات المستخدم.

### الأسئلة الشائعة

#### س: كيف يمكنني إنشاء مشروع C# جديد في IDE الخاص بي؟

ج: قد تختلف خطوات إنشاء مشروع C# جديد وفقًا لـ IDE الذي تستخدمه. راجع وثائق IDE الخاصة بك للحصول على تعليمات مفصلة.

#### س: هل من الممكن ضبط إعدادات حماية مخصصة غير تلك المذكورة في البرنامج التعليمي؟

ج: نعم، تقدم Aspose.Cells نطاقًا واسعًا من إعدادات الحماية التي يمكنك تخصيصها وفقًا لاحتياجاتك الخاصة. راجع وثائق Aspose.Cells لمزيد من التفاصيل.

#### س: ما هو تنسيق الملف المستخدم لحفظ ملف Excel المعدل في نموذج التعليمات البرمجية؟

ج: في نموذج التعليمات البرمجية، يتم حفظ ملف Excel المعدل بتنسيق Excel 97-2003 (.xls). يمكنك اختيار التنسيقات الأخرى التي يدعمها Aspose.Cells إذا لزم الأمر.

#### س: كيف يمكنني الوصول إلى أوراق العمل الأخرى في ملف Excel؟

 ج: يمكنك الوصول إلى أوراق العمل الأخرى باستخدام الفهرس أو اسم الورقة، على سبيل المثال:`Worksheet worksheet = excel.Worksheets[1];` أو`Worksheet worksheet = excel.Worksheets[" SheetName"];`.