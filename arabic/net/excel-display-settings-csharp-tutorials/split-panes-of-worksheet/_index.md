---
title: انقسام أجزاء من ورقة العمل
linktitle: انقسام أجزاء من ورقة العمل
second_title: Aspose.Cells لمرجع .NET API
description: دليل خطوة بخطوة لتقسيم الأجزاء في ورقة عمل Excel باستخدام Aspose.Cells for .NET.
type: docs
weight: 130
url: /ar/net/excel-display-settings-csharp-tutorials/split-panes-of-worksheet/
---
في هذا البرنامج التعليمي ، سنشرح كيفية تقسيم الأجزاء في ورقة عمل Excel باستخدام Aspose.Cells for .NET. اتبع هذه الخطوات للحصول على النتيجة المرجوة:

## الخطوة الأولى: تهيئة البيئة

تأكد من تثبيت Aspose.Cells for .NET وإعداد بيئة التطوير الخاصة بك. تأكد أيضًا من أن لديك نسخة من ملف Excel الذي تريد تقسيم الأجزاء عليه.

## الخطوة 2: استيراد التبعيات الضرورية

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

 تجسيد ملف`Workbook` الكائن وافتح ملف Excel باستخدام ملحق`Open` طريقة:

```csharp
Workbook book = new Workbook(dataDir + "Book1.xls");
```

## الخطوة 5: تحديد الخلية النشطة

 قم بتعيين الخلية النشطة لورقة العمل باستخدام امتداد`ActiveCell` ملكية:

```csharp
book.Worksheets[0].ActiveCell = "A20";
```

## الخطوة 6: تقسيم اللوحات

 قم بتقسيم نافذة ورقة العمل باستخدام ملف`Split` طريقة:

```csharp
book.Worksheets[0].Split();
```

## الخطوة 7: حفظ التغييرات

احفظ التغييرات التي تم إجراؤها على ملف Excel:

```csharp
book.Save(dataDir + "output.xls");
```

### نموذج التعليمات البرمجية المصدر لـ Split Panes Of Worksheet باستخدام Aspose.Cells لـ .NET 

```csharp
// المسار إلى دليل المستندات.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// إنشاء مصنف جديد وفتح ملف قالب
Workbook book = new Workbook(dataDir + "Book1.xls");
// قم بتعيين الخلية النشطة
book.Worksheets[0].ActiveCell = "A20";
// انقسام نافذة ورقة العمل
book.Worksheets[0].Split();
// احفظ ملف اكسل
book.Save(dataDir + "output.xls");
```

## خاتمة

في هذا البرنامج التعليمي ، تعلمت كيفية تقسيم الأجزاء في ورقة عمل Excel باستخدام Aspose.Cells for .NET. باتباع الخطوات الموضحة ، يمكنك بسهولة تخصيص مظهر وسلوك ملفات Excel الخاصة بك.

### أسئلة وأجوبة (FAQ)

#### ما هو Aspose.Cells لـ .NET؟

Aspose.Cells for .NET هي مكتبة برامج شائعة لمعالجة ملفات Excel في تطبيقات .NET.

#### كيف يمكنني ضبط الخلية النشطة لورقة العمل في Aspose.Cells؟

 يمكنك ضبط الخلية النشطة باستخدام ملف`ActiveCell`خاصية كائن ورقة العمل.

#### هل يمكنني فقط تقسيم الأجزاء الأفقية أو الرأسية من نافذة ورقة العمل؟

 نعم ، باستخدام Aspose.Cells يمكنك فقط تقسيم الأجزاء الأفقية أو الرأسية باستخدام الطرق المناسبة مثل`SplitColumn` أو`SplitRow`.

#### هل يعمل Aspose.Cells فقط مع ملفات Excel بتنسيق .xls؟

لا ، Aspose.Cells يدعم العديد من تنسيقات ملفات Excel بما في ذلك .xls و .xlsx.