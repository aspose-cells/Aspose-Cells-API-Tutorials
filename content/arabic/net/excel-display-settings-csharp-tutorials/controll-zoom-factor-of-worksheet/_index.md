---
title: التحكم في عامل التكبير لورقة العمل
linktitle: التحكم في عامل التكبير لورقة العمل
second_title: Aspose.Cells لمرجع .NET API
description: تحكم في عامل تكبير ورقة عمل Excel باستخدام Aspose.Cells for .NET.
type: docs
weight: 20
url: /ar/net/excel-display-settings-csharp-tutorials/controll-zoom-factor-of-worksheet/
---
يعد التحكم في عامل التكبير / التصغير الخاص بورقة العمل ميزة أساسية عند العمل مع ملفات Excel باستخدام مكتبة Aspose.Cells لـ .NET. في هذا الدليل ، سنوضح لك كيفية استخدام Aspose.Cells للتحكم في عامل التكبير / التصغير الخاص بورقة العمل باستخدام شفرة المصدر C # خطوة بخطوة.

## الخطوة 1: استيراد المكتبات المطلوبة

قبل أن تبدأ ، تأكد من تثبيت مكتبة Aspose.Cells لـ .NET واستورد المكتبات الضرورية إلى مشروع C # الخاص بك.

```csharp
using System;
using System.IO;
using Aspose.Cells;
```

## الخطوة 2: تعيين مسار الدليل وفتح ملف Excel

 للبدء ، قم بتعيين المسار إلى الدليل الذي يحتوي على ملف Excel الخاص بك ، ثم افتحه باستخدام ملف`FileStream` الكائن وإنشاء مثيل أ`Workbook` كائن لتمثيل مصنف Excel.

```csharp
string dataDir = "YOUR DOCUMENTS DIRECTORY";
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
Workbook workbook = new Workbook(fstream);
```

## الخطوة 3: الوصول إلى جدول البيانات وتغيير عامل التكبير / التصغير

في هذه الخطوة ، نصل إلى ورقة العمل الأولى من مصنف Excel باستخدام الفهرس`0` وقم بتعيين عامل تكبير ورقة العمل على`75`.

```csharp
Worksheet worksheet = workbook.Worksheets[0];
worksheet. Zoom = 75;
```

## الخطوة 4: احفظ التغييرات وأغلق الملف

 بمجرد تغيير عامل تكبير ورقة العمل ، نقوم بحفظ التغييرات في ملف Excel باستخدام امتداد`Save` طريقة`Workbook` هدف. ثم نقوم بإغلاق دفق الملفات لتحرير جميع الموارد المستخدمة.

```csharp
workbook.Save(dataDir + "output.xls");
fstream.Close();
```

### عينة من التعليمات البرمجية المصدر للتحكم في عامل التكبير لورقة العمل باستخدام Aspose.Cells for .NET 

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
// ضبط عامل التكبير / التصغير لورقة العمل على 75
worksheet.Zoom = 75;
// حفظ ملف Excel المعدل
workbook.Save(dataDir + "output.xls");
// إغلاق دفق الملف لتحرير جميع الموارد
fstream.Close();
```

## خاتمة

يوضح لك هذا الدليل التفصيلي كيفية التحكم في عامل التكبير / التصغير الخاص بورقة العمل باستخدام Aspose.Cells for .NET. باستخدام الكود المصدري C # المقدم ، يمكنك بسهولة ضبط عامل التكبير / التصغير الخاص بورقة العمل في تطبيقات .NET الخاصة بك.

### أسئلة وأجوبة (FAQ)

#### ما هو Aspose.Cells لـ .NET؟

Aspose.Cells for .NET هي مكتبة ملفات غنية بالمميزات لمعالجة ملفات Excel في تطبيقات .NET.

#### كيف يمكنني تثبيت Aspose.Cells for .NET؟

 لتثبيت Aspose.Cells for .NET ، تحتاج إلى تنزيل حزمة NuGet المقابلة من[إصدارات Aspose](https://releases/aspose.com/cells/net/) وإضافته إلى مشروع .NET الخاص بك.

#### ما هي الميزات التي تقدمها Aspose.Cells for .NET؟

يوفر Aspose.Cells for .NET ميزات مثل إنشاء ملفات Excel وتحريرها وتحويلها ومعالجتها بشكل متقدم.

#### ما هي تنسيقات الملفات التي يدعمها Aspose.Cells لـ .NET؟

يدعم Aspose.Cells for .NET تنسيقات ملفات متعددة بما في ذلك XLSX و XLSM و CSV و HTML و PDF وغيرها الكثير.
