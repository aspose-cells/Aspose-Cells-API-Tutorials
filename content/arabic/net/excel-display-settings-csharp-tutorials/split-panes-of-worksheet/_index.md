---
title: تقسيم أجزاء ورقة العمل
linktitle: تقسيم أجزاء ورقة العمل
second_title: Aspose.Cells لمرجع .NET API
description: دليل خطوة بخطوة لتقسيم الأجزاء في ورقة عمل Excel باستخدام Aspose.Cells لـ .NET.
type: docs
weight: 130
url: /ar/net/excel-display-settings-csharp-tutorials/split-panes-of-worksheet/
---
سنشرح في هذا البرنامج التعليمي كيفية تقسيم الأجزاء في ورقة عمل Excel باستخدام Aspose.Cells for .NET. اتبعي الخطوات التالية للحصول على النتيجة المرجوة:

## الخطوة 1: تهيئة البيئة

تأكد من تثبيت Aspose.Cells لـ .NET وإعداد بيئة التطوير الخاصة بك. تأكد أيضًا من أن لديك نسخة من ملف Excel الذي تريد تقسيم الأجزاء عليه.

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

## الخطوة 6: تقسيم اللوحات

 قم بتقسيم نافذة ورقة العمل باستخدام`Split` طريقة:

```csharp
book.Worksheets[0].Split();
```

## الخطوة 7: حفظ التغييرات

احفظ التغييرات التي تم إجراؤها على ملف Excel:

```csharp
book.Save(dataDir + "output.xls");
```

### نموذج التعليمات البرمجية المصدر لتقسيم أجزاء ورقة العمل باستخدام Aspose.Cells لـ .NET 

```csharp
//المسار إلى دليل المستندات.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// إنشاء مثيل لمصنف جديد وفتح ملف قالب
Workbook book = new Workbook(dataDir + "Book1.xls");
// قم بتعيين الخلية النشطة
book.Worksheets[0].ActiveCell = "A20";
// تقسيم نافذة ورقة العمل
book.Worksheets[0].Split();
// احفظ ملف الاكسل
book.Save(dataDir + "output.xls");
```

## خاتمة

في هذا البرنامج التعليمي، تعلمت كيفية تقسيم الأجزاء في ورقة عمل Excel باستخدام Aspose.Cells لـ .NET. باتباع الخطوات الموضحة، يمكنك بسهولة تخصيص مظهر وسلوك ملفات Excel الخاصة بك.

### أسئلة وأجوبة (FAQ)

#### ما هو Aspose.Cells لـ .NET؟

Aspose.Cells for .NET هي مكتبة برامج شائعة لمعالجة ملفات Excel في تطبيقات .NET.

#### كيف يمكنني ضبط الخلية النشطة لورقة العمل في Aspose.Cells؟

 يمكنك ضبط الخلية النشطة باستخدام`ActiveCell`خاصية كائن ورقة العمل.

#### هل يمكنني فقط تقسيم الأجزاء الأفقية أو الرأسية لنافذة ورقة العمل؟

 نعم، باستخدام Aspose.Cells، يمكنك فقط تقسيم الأجزاء الأفقية أو الرأسية باستخدام الطرق المناسبة مثل`SplitColumn` أو`SplitRow`.

#### هل يعمل Aspose.Cells فقط مع ملفات Excel بتنسيق .xls؟

لا، يدعم Aspose.Cells العديد من تنسيقات ملفات Excel بما في ذلك .xls و.xlsx.