---
title: معاينة فاصل الصفحة لورقة العمل
linktitle: معاينة فاصل الصفحة لورقة العمل
second_title: Aspose.Cells لمرجع .NET API
description: دليل خطوة بخطوة لإظهار معاينة فاصل الصفحات لورقة العمل باستخدام Aspose.Cells for .NET.
type: docs
weight: 110
url: /ar/net/excel-display-settings-csharp-tutorials/page-break-preview-of-worksheet/
---
في هذا البرنامج التعليمي ، سنشرح كيفية إظهار معاينة فاصل الصفحات لورقة العمل باستخدام Aspose.Cells for .NET. اتبع هذه الخطوات للحصول على النتيجة المرجوة:

## الخطوة الأولى: تهيئة البيئة

تأكد من تثبيت Aspose.Cells for .NET وإعداد بيئة التطوير الخاصة بك. تأكد أيضًا من أن لديك نسخة من ملف Excel الذي تريد عرض معاينة فاصل الصفحة عليه.

## الخطوة 2: استيراد التبعيات الضرورية

أضف التوجيهات اللازمة لاستخدام الفئات من Aspose.Cells:

```csharp
using Aspose.Cells;
using System.IO;
```

## الخطوة 3: تهيئة الكود

ابدأ بتهيئة المسار إلى الدليل الذي يحتوي على مستندات Excel الخاصة بك:

```csharp
string dataDir = "YOUR DOCUMENTS DIRECTORY";
```

## الخطوة 4: فتح ملف Excel

 إنشاء`FileStream` كائن يحتوي على ملف Excel لفتحه:

```csharp
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
```

 تجسيد أ`Workbook` الكائن وافتح ملف Excel باستخدام تدفق الملفات:

```csharp
Workbook workbook = new Workbook(fstream);
```

## الخطوة 5: الوصول إلى جدول البيانات

انتقل إلى ورقة العمل الأولى في ملف Excel:

```csharp
Worksheet worksheet = workbook.Worksheets[0];
```

## الخطوة 6: عرض معاينة الصفحة

تمكين معاينة الصفحة حسب لجدول البيانات:

```csharp
worksheet. IsPageBreakPreview = true;
```

## الخطوة 7: حفظ التغييرات

احفظ التغييرات التي تم إجراؤها على ملف Excel:

```csharp
workbook.Save(dataDir + "output.xls");
```

## الخطوة 8: إغلاق دفق الملف

أغلق تدفق الملفات لتحرير جميع الموارد:

```csharp
fstream.Close();
```

### نموذج التعليمات البرمجية المصدر لـ Page Break Preview Of Worksheet باستخدام Aspose.Cells for .NET 
```csharp
// المسار إلى دليل المستندات.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// إنشاء دفق ملف يحتوي على ملف Excel ليتم فتحه
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
// إنشاء كائن مصنف
// فتح ملف Excel من خلال تدفق الملفات
Workbook workbook = new Workbook(fstream);
// الوصول إلى ورقة العمل الأولى في ملف Excel
Worksheet worksheet = workbook.Worksheets[0];
// عرض ورقة العمل في معاينة فاصل الصفحة
worksheet.IsPageBreakPreview = true;
// حفظ ملف Excel المعدل
workbook.Save(dataDir + "output.xls");
// إغلاق دفق الملف لتحرير جميع الموارد
fstream.Close();
```

## خاتمة

في هذا البرنامج التعليمي ، تعلمت كيفية عرض معاينة فاصل الصفحات لورقة عمل باستخدام Aspose.Cells for .NET. باتباع الخطوات الموضحة ، يمكنك التحكم بسهولة في مظهر وتخطيط ملفات Excel.

### أسئلة وأجوبة (FAQ)

#### ما هو Aspose.Cells لـ .NET؟

Aspose.Cells for .NET هي مكتبة برامج شائعة لمعالجة ملفات Excel في تطبيقات .NET.

#### هل يمكنني إظهار معاينة الصفحة حسب لورقة عمل معينة بدلاً من ورقة العمل بأكملها؟

نعم ، باستخدام Aspose.Cells ، يمكنك تمكين معاينة فاصل الصفحة لورقة عمل محددة عن طريق الوصول إلى كائن ورقة العمل المقابل.

#### هل يدعم Aspose.Cells ميزات تحرير ملفات Excel الأخرى؟

نعم ، Aspose.Cells تقدم مجموعة واسعة من الميزات لتحرير ملفات Excel ومعالجتها ، مثل إضافة البيانات ، والتنسيق ، وإنشاء الرسوم البيانية ، وما إلى ذلك.

#### هل يعمل Aspose.Cells فقط مع ملفات Excel بتنسيق .xls؟

لا ، Aspose.Cells يدعم العديد من تنسيقات ملفات Excel بما في ذلك .xls و .xlsx.
	