---
title: عرض وإخفاء رؤوس أعمدة الصفوف في ورقة العمل
linktitle: عرض وإخفاء رؤوس أعمدة الصفوف في ورقة العمل
second_title: Aspose.Cells لمرجع .NET API
description: عرض أو إخفاء رؤوس الصفوف والأعمدة في ورقة عمل Excel باستخدام Aspose.Cells لـ .NET.
type: docs
weight: 40
url: /ar/net/excel-display-settings-csharp-tutorials/display-and-hide-row-column-headers-of-worksheet/
---
سنوضح لك في هذا البرنامج التعليمي كيفية عرض أو إخفاء رؤوس الصفوف والأعمدة في ورقة عمل Excel باستخدام كود مصدر C# مع Aspose.Cells for .NET. اتبع الخطوات أدناه للحصول على النتيجة المرجوة.

## الخطوة 1: استيراد المكتبات اللازمة

تأكد من تثبيت مكتبة Aspose.Cells لـ .NET واستيراد المكتبات الضرورية إلى مشروع C# الخاص بك.

```csharp
using Aspose.Cells;
using System.IO;
```

## الخطوة 2: قم بتعيين مسار الدليل وافتح ملف Excel

 قم بتعيين المسار إلى الدليل الذي يحتوي على ملف Excel الخاص بك، ثم افتح الملف عن طريق إنشاء دفق ملف وإنشاء مثيل له`Workbook` هدف.

```csharp
string dataDir = "YOUR DOCUMENTS DIRECTORY";
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
Workbook workbook = new Workbook(fstream);
```

## الخطوة 3: انتقل إلى ورقة العمل الأولى وقم بإخفاء رؤوس الصفوف والأعمدة

 قم بالوصول إلى ورقة العمل الأولى في ملف Excel باستخدام الملف`Worksheets` ملكية`Workbook` هدف. ثم استخدم`IsRowColumnHeadersVisible` ملكية`Worksheet` كائن لإخفاء رؤوس الصفوف والأعمدة.

```csharp
Worksheet worksheet = workbook.Worksheets[0];
worksheet. IsRowColumnHeadersVisible = false;
```

## الخطوة 4: حفظ التغييرات

 بمجرد إجراء التغييرات اللازمة، احفظ ملف Excel المعدل باستخدام الملف`Save` طريقة`Workbook` هدف.

```csharp
workbook.Save(dataDir + "output.xls");
```

### نموذج التعليمات البرمجية المصدر لعرض وإخفاء رؤوس أعمدة الصفوف في ورقة العمل باستخدام Aspose.Cells لـ .NET 
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
// إخفاء رؤوس الصفوف والأعمدة
worksheet.IsRowColumnHeadersVisible = false;
// حفظ ملف Excel المعدل
workbook.Save(dataDir + "output.xls");
// إغلاق دفق الملف لتحرير كافة الموارد
fstream.Close(); 
```

## خاتمة

يوضح لك هذا الدليل خطوة بخطوة كيفية عرض أو إخفاء رؤوس الصفوف والأعمدة في جدول بيانات Excel باستخدام Aspose.Cells for .NET. باستخدام كود مصدر C# المقدم، يمكنك بسهولة تخصيص عرض الرؤوس في ملفات Excel الخاصة بك.

### أسئلة وأجوبة (FAQ)

#### ما هو Aspose.Cells لـ .NET؟

Aspose.Cells for .NET هي مكتبة قوية لمعالجة ملفات Excel في تطبيقات .NET.

#### كيف يمكنني تثبيت Aspose.Cells لـ .NET؟

 لتثبيت Aspose.Cells لـ .NET، يتعين عليك تنزيل الحزمة ذات الصلة من[إصدارات Aspose](https://releases/aspose.com/cells/net/) وإضافته إلى مشروع .NET الخاص بك.

#### كيف يمكنني إظهار أو إخفاء رؤوس الصفوف والأعمدة في جدول بيانات Excel باستخدام Aspose.Cells لـ .NET؟

 يمكنك استخدام ال`IsRowColumnHeadersVisible` ملكية`Worksheet`كائن لعرض أو إخفاء رؤوس الصفوف والأعمدة. اضبطه على`true` لتظهر لهم و`false` لإخفائهم.

#### ما هي تنسيقات ملفات Excel الأخرى التي يدعمها Aspose.Cells لـ .NET؟

يدعم Aspose.Cells for .NET تنسيقات ملفات Excel المختلفة، مثل XLS وXLSX وCSV وHTML وPDF وغيرها الكثير.
