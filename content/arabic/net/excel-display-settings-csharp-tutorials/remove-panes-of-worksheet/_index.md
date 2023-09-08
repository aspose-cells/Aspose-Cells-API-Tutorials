---
title: إزالة أجزاء من ورقة العمل
linktitle: إزالة أجزاء من ورقة العمل
second_title: Aspose.Cells لمرجع .NET API
description: دليل خطوة بخطوة لإزالة الأجزاء من ورقة عمل Excel باستخدام Aspose.Cells لـ .NET.
type: docs
weight: 120
url: /ar/net/excel-display-settings-csharp-tutorials/remove-panes-of-worksheet/
---
سنشرح في هذا البرنامج التعليمي كيفية إزالة الأجزاء من ورقة عمل Excel باستخدام Aspose.Cells for .NET. اتبعي الخطوات التالية للحصول على النتيجة المرجوة:

## الخطوة 1: تهيئة البيئة

تأكد من تثبيت Aspose.Cells لـ .NET وإعداد بيئة التطوير الخاصة بك. تأكد أيضًا من أن لديك نسخة من ملف Excel الذي تريد إزالة الأجزاء منه.

## الخطوة 2: استيراد التبعيات اللازمة

أضف التوجيهات اللازمة لاستخدام الفئات من Aspose.Cells:

```csharp
using Aspose.Cells;
```

## الخطوة 3: تهيئة الكود

ابدأ بتهيئة المسار إلى الدليل الذي يحتوي على مستندات Excel الخاصة بك:

```csharp
string dataDir = "YOUR DOCUMENTS DIRECTORY";
```

## الخطوة 4: فتح ملف Excel

 إنشاء مثيل جديد`Workbook` الكائن وافتح ملف Excel باستخدام الملف`Open` طريقة:

```csharp
Workbook book = new Workbook(dataDir + "Book1.xls");
```

## الخطوة 5: تحديد الخلية النشطة

 قم بتعيين الخلية النشطة لورقة العمل باستخدام`ActiveCell` ملكية:

```csharp
book.Worksheets[0].ActiveCell = "A20";
```

## الخطوة 6: حذف الأجزاء

 قم بإزالة الأجزاء من نافذة ورقة العمل باستخدام`RemoveSplit` طريقة:

```csharp
book.Worksheets[0].RemoveSplit();
```

## الخطوة 7: حفظ التغييرات

احفظ التغييرات التي تم إجراؤها على ملف Excel:

```csharp
book.Save(dataDir + "output.xls");
```

### نموذج التعليمات البرمجية المصدر لإزالة أجزاء من ورقة العمل باستخدام Aspose.Cells لـ .NET 
```csharp
//المسار إلى دليل المستندات.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// إنشاء مثيل لمصنف جديد وفتح ملف قالب
Workbook book = new Workbook(dataDir + "Book1.xls");
// قم بتعيين الخلية النشطة
book.Worksheets[0].ActiveCell = "A20";
// تقسيم نافذة ورقة العمل
book.Worksheets[0].RemoveSplit();
// احفظ ملف الاكسل
book.Save(dataDir + "output.xls");
```

## خاتمة

في هذا البرنامج التعليمي، تعلمت كيفية إزالة الأجزاء من ورقة عمل Excel باستخدام Aspose.Cells لـ .NET. باتباع الخطوات الموضحة، يمكنك بسهولة تخصيص مظهر وسلوك ملفات Excel الخاصة بك.

### أسئلة وأجوبة (FAQ)

#### ما هو Aspose.Cells لـ .NET؟

Aspose.Cells for .NET هي مكتبة برامج شائعة لمعالجة ملفات Excel في تطبيقات .NET.

#### كيف يمكنني ضبط الخلية النشطة لورقة العمل في Aspose.Cells؟

 يمكنك ضبط الخلية النشطة باستخدام`ActiveCell`خاصية كائن ورقة العمل.

#### هل يمكنني إزالة الأجزاء الأفقية أو الرأسية فقط من نافذة ورقة العمل؟

 نعم، باستخدام Aspose.Cells، يمكنك إزالة الأجزاء الأفقية أو الرأسية فقط باستخدام الطرق المناسبة مثل`RemoveHorizontalSplit` أو`RemoveVerticalSplit`.

#### هل يعمل Aspose.Cells فقط مع ملفات Excel بتنسيق .xls؟

لا، يدعم Aspose.Cells العديد من تنسيقات ملفات Excel بما في ذلك .xls و.xlsx.
	