---
title: التحكم في عامل التكبير من ورقة العمل
linktitle: التحكم في عامل التكبير من ورقة العمل
second_title: Aspose.Cells لمرجع .NET API
description: تحكم في عامل التكبير/التصغير لورقة عمل Excel باستخدام Aspose.Cells لـ .NET.
type: docs
weight: 20
url: /ar/net/excel-display-settings-csharp-tutorials/controll-zoom-factor-of-worksheet/
---
يعد التحكم في عامل التكبير/التصغير لورقة العمل ميزة أساسية عند العمل مع ملفات Excel باستخدام مكتبة Aspose.Cells لـ .NET. سنوضح لك في هذا الدليل كيفية استخدام Aspose.Cells للتحكم في عامل التكبير/التصغير لورقة العمل باستخدام كود مصدر C# خطوة بخطوة.

## الخطوة 1: استيراد المكتبات المطلوبة

قبل البدء، تأكد من تثبيت مكتبة Aspose.Cells لـ .NET واستيراد المكتبات الضرورية إلى مشروع C# الخاص بك.

```csharp
using System;
using System.IO;
using Aspose.Cells;
```

## الخطوة 2: قم بتعيين مسار الدليل وفتح ملف Excel

 للبدء، قم بتعيين المسار إلى الدليل الذي يحتوي على ملف Excel الخاص بك، ثم افتحه باستخدام ملف`FileStream` كائن وإنشاء مثيل أ`Workbook` كائن لتمثيل مصنف Excel.

```csharp
string dataDir = "YOUR DOCUMENTS DIRECTORY";
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
Workbook workbook = new Workbook(fstream);
```

## الخطوة 3: الوصول إلى جدول البيانات وتغيير عامل التكبير/التصغير

في هذه الخطوة، نقوم بالوصول إلى ورقة العمل الأولى من مصنف Excel باستخدام الفهرس`0` وقم بتعيين عامل تكبير ورقة العمل على`75`.

```csharp
Worksheet worksheet = workbook.Worksheets[0];
worksheet. Zoom = 75;
```

## الخطوة 4: احفظ التغييرات وأغلق الملف

 بمجرد تغيير عامل تكبير ورقة العمل، نقوم بحفظ التغييرات في ملف Excel باستخدام الملف`Save` طريقة`Workbook` هدف. ثم نغلق دفق الملفات لتحرير جميع الموارد المستخدمة.

```csharp
workbook.Save(dataDir + "output.xls");
fstream.Close();
```

### نموذج التعليمات البرمجية المصدر لـ Controll Zoom Factor Of Worksheet باستخدام Aspose.Cells لـ .NET 

```csharp
//المسار إلى دليل المستندات.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// إنشاء دفق ملف يحتوي على ملف Excel المراد فتحه
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
// إنشاء مثيل لكائن المصنف
// فتح ملف Excel من خلال دفق الملف
Workbook workbook = new Workbook(fstream);
// الوصول إلى ورقة العمل الأولى في ملف Excel
Worksheet worksheet = workbook.Worksheets[0];
// ضبط عامل التكبير لورقة العمل على 75
worksheet.Zoom = 75;
// حفظ ملف Excel المعدل
workbook.Save(dataDir + "output.xls");
// إغلاق دفق الملف لتحرير كافة الموارد
fstream.Close();
```

## خاتمة

يوضح لك هذا الدليل خطوة بخطوة كيفية التحكم في عامل التكبير/التصغير لورقة العمل باستخدام Aspose.Cells for .NET. باستخدام كود مصدر C# المتوفر، يمكنك بسهولة ضبط عامل التكبير/التصغير لورقة العمل في تطبيقات .NET الخاصة بك.

### أسئلة وأجوبة (FAQ)

#### ما هو Aspose.Cells لـ .NET؟

Aspose.Cells for .NET عبارة عن مكتبة ملفات غنية بالميزات لمعالجة ملفات Excel في تطبيقات .NET.

#### كيف يمكنني تثبيت Aspose.Cells لـ .NET؟

 لتثبيت Aspose.Cells لـ .NET، تحتاج إلى تنزيل حزمة NuGet المقابلة من[إصدارات Aspose](https://releases/aspose.com/cells/net/) وإضافته إلى مشروع .NET الخاص بك.

#### ما هي الميزات التي يقدمها Aspose.Cells لـ .NET؟

يوفر Aspose.Cells for .NET ميزات مثل إنشاء ملفات Excel وتحريرها وتحويلها ومعالجتها المتقدمة.

#### ما تنسيقات الملفات التي يدعمها Aspose.Cells لـ .NET؟

يدعم Aspose.Cells for .NET تنسيقات ملفات متعددة بما في ذلك XLSX وXLSM وCSV وHTML وPDF وغيرها الكثير.
