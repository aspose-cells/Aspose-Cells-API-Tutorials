---
title: إعدادات الحماية المتقدمة لورقة عمل Excel
linktitle: إعدادات الحماية المتقدمة لورقة عمل Excel
second_title: Aspose.Cells لمرجع .NET API
description: قم بحماية ملفات Excel الخاصة بك عن طريق تعيين إعدادات الحماية المتقدمة باستخدام Aspose.Cells for .NET.
type: docs
weight: 10
url: /ar/net/excel-security/advanced-protection-settings-for-excel-worksheet/
---
في هذا البرنامج التعليمي ، سنرشدك خلال الخطوات لتعيين إعدادات الحماية المتقدمة لجدول بيانات Excel باستخدام مكتبة Aspose.Cells لـ .NET. اتبع التعليمات أدناه لإكمال هذه المهمة.

## الخطوة الأولى: التحضير

تأكد من تثبيت Aspose.Cells لـ .NET وإنشاء مشروع C # في بيئة التطوير المتكاملة المفضلة لديك (IDE).

## الخطوة 2: قم بتعيين مسار دليل المستند

 تعلن أ`dataDir` متغير وتهيئته بالمسار إلى دليل المستندات. على سبيل المثال :

```csharp
string dataDir = "YOUR_DIRECTORY_OF_DOCUMENTS";
```

 تأكد من استبدال`"YOUR_DOCUMENTS_DIRECTORY"` مع المسار الفعلي للدليل الخاص بك.

## الخطوة 3: قم بإنشاء دفق ملف لفتح ملف Excel

 إنشاء`FileStream` كائن يحتوي على ملف Excel لفتحه:

```csharp
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
```

 تأكد من أن لديك ملف Excel`book1.xls` في دليل المستندات الخاص بك أو تحديد اسم الملف الصحيح والموقع.

## الخطوة 4: إنشاء كائن مصنف وافتح ملف Excel

 استخدم ال`Workbook`class من Aspose.Cells لإنشاء كائن مصنف وفتح ملف Excel المحدد عبر تدفق الملف:

```csharp
Workbook excel = new Workbook(fstream);
```

## الخطوة 5: قم بالوصول إلى ورقة العمل الأولى

انتقل إلى ورقة العمل الأولى لملف Excel:

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
// ... اضبط إعدادات الحماية الأخرى حسب الحاجة ...
```

## الخطوة 7: احفظ ملف Excel المعدل

 احفظ ملف Excel المعدل باستخدام امتداد`Save` طريقة كائن المصنف:

```csharp
excel.Save(dataDir + "output.xls", SaveFormat.Excel97To2003);
```

تأكد من تحديد المسار المطلوب واسم الملف لملف الإخراج.

## الخطوة 8: أغلق تدفق الملفات

بمجرد الحفظ ، أغلق دفق الملف لتحرير جميع الموارد المرتبطة:

```csharp
fstream.Close();
```
	
### نموذج التعليمات البرمجية المصدر لإعدادات الحماية المتقدمة لورقة عمل Excel باستخدام Aspose.Cells for .NET 
```csharp
// المسار إلى دليل المستندات.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// إنشاء دفق ملف يحتوي على ملف Excel ليتم فتحه
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
// إنشاء كائن مصنف
// فتح ملف Excel من خلال تدفق الملفات
Workbook excel = new Workbook(fstream);
// الوصول إلى ورقة العمل الأولى في ملف Excel
Worksheet worksheet = excel.Worksheets[0];
// تقييد المستخدمين لحذف أعمدة من ورقة العمل
worksheet.Protection.AllowDeletingColumn = false;
// تقييد المستخدمين لحذف صف من ورقة العمل
worksheet.Protection.AllowDeletingRow = false;
// تقييد المستخدمين لتحرير محتويات ورقة العمل
worksheet.Protection.AllowEditingContent = false;
// تقييد المستخدمين لتحرير كائنات ورقة العمل
worksheet.Protection.AllowEditingObject = false;
// تقييد المستخدمين لتحرير سيناريوهات ورقة العمل
worksheet.Protection.AllowEditingScenario = false;
//تقييد المستخدمين على التصفية
worksheet.Protection.AllowFiltering = false;
// السماح للمستخدمين بتنسيق خلايا ورقة العمل
worksheet.Protection.AllowFormattingCell = true;
// السماح للمستخدمين بتنسيق صفوف ورقة العمل
worksheet.Protection.AllowFormattingRow = true;
// السماح للمستخدمين بإدراج أعمدة في ورقة العمل
worksheet.Protection.AllowFormattingColumn = true;
// السماح للمستخدمين بإدراج ارتباطات تشعبية في ورقة العمل
worksheet.Protection.AllowInsertingHyperlink = true;
// السماح للمستخدمين بإدراج صفوف في ورقة العمل
worksheet.Protection.AllowInsertingRow = true;
// السماح للمستخدمين بتحديد الخلايا المؤمنة من ورقة العمل
worksheet.Protection.AllowSelectingLockedCell = true;
// السماح للمستخدمين بتحديد الخلايا غير المؤمنة من ورقة العمل
worksheet.Protection.AllowSelectingUnlockedCell = true;
// السماح للمستخدمين بالفرز
worksheet.Protection.AllowSorting = true;
// السماح للمستخدمين باستخدام الجداول المحورية في ورقة العمل
worksheet.Protection.AllowUsingPivotTable = true;
// حفظ ملف Excel المعدل
excel.Save(dataDir + "output.xls", SaveFormat.Excel97To2003);
// إغلاق دفق الملف لتحرير جميع الموارد
fstream.Close();
```

## خاتمة

تهنئة ! لقد تعلمت الآن كيفية تعيين إعدادات الحماية المتقدمة لجدول بيانات Excel باستخدام Aspose.Cells for .NET. استخدم هذه المعرفة لتأمين ملفات Excel الخاصة بك وتقييد إجراءات المستخدم.

### أسئلة وأجوبة

#### س: كيف يمكنني إنشاء مشروع C # جديد في IDE الخاص بي؟

ج: قد تختلف خطوات إنشاء مشروع C # جديد اعتمادًا على IDE الذي تستخدمه. راجع وثائق IDE الخاصة بك للحصول على إرشادات مفصلة.

#### س: هل من الممكن تعيين إعدادات حماية مخصصة بخلاف تلك المذكورة في البرنامج التعليمي؟

ج: نعم ، تقدم Aspose.Cells مجموعة واسعة من إعدادات الحماية التي يمكنك تخصيصها وفقًا لاحتياجاتك الخاصة. راجع وثائق Aspose.Cells لمزيد من التفاصيل.

#### س: ما هو تنسيق الملف المستخدم لحفظ ملف Excel المعدل في نموذج التعليمات البرمجية؟

ج: في نموذج التعليمات البرمجية ، يتم حفظ ملف Excel المعدل بتنسيق Excel 97-2003 (.xls). يمكنك اختيار التنسيقات الأخرى التي يدعمها Aspose.Cells إذا لزم الأمر.

#### س: كيف يمكنني الوصول إلى أوراق عمل أخرى في ملف Excel؟

 ج: يمكنك الوصول إلى أوراق عمل أخرى باستخدام اسم الفهرس أو الورقة ، على سبيل المثال:`Worksheet worksheet = excel.Worksheets[1];` أو`Worksheet worksheet = excel.Worksheets[" SheetName"];`.