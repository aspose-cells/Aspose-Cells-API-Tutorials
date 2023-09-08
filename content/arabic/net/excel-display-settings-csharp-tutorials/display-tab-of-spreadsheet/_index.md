---
title: عرض علامة التبويب لجدول البيانات
linktitle: عرض علامة التبويب لجدول البيانات
second_title: Aspose.Cells لمرجع .NET API
description: عرض علامة تبويب جدول بيانات Excel باستخدام Aspose.Cells لـ .NET.
type: docs
weight: 60
url: /ar/net/excel-display-settings-csharp-tutorials/display-tab-of-spreadsheet/
---
سنوضح لك في هذا البرنامج التعليمي كيفية عرض علامة تبويب ورقة عمل Excel باستخدام كود مصدر C# مع Aspose.Cells for .NET. اتبع الخطوات أدناه للحصول على النتيجة المرجوة.

## الخطوة 1: استيراد المكتبات اللازمة

تأكد من تثبيت مكتبة Aspose.Cells لـ .NET واستيراد المكتبات الضرورية إلى مشروع C# الخاص بك.

```csharp
using Aspose.Cells;
```

## الخطوة 2: قم بتعيين مسار الدليل وافتح ملف Excel

 قم بتعيين المسار إلى الدليل الذي يحتوي على ملف Excel الخاص بك، ثم افتح الملف عن طريق إنشاء مثيل لـ`Workbook` هدف.

```csharp
string dataDir = "YOUR DOCUMENTS DIRECTORY";
Workbook workbook = new Workbook(dataDir + "book1.xls");
```

## الخطوة 3: إظهار علامة تبويب ورقة العمل

 استخدم ال`ShowTabs` ملكية`Workbook.Settings` كائن لإظهار علامة تبويب ورقة عمل Excel.

```csharp
workbook.Settings.ShowTabs = true;
```

## الخطوة 4: حفظ التغييرات

 بمجرد إجراء التغييرات اللازمة، احفظ ملف Excel المعدل باستخدام الملف`Save` طريقة`Workbook` هدف.

```csharp
workbook.Save(dataDir + "output.xls");
```

### نموذج التعليمات البرمجية المصدر لعرض علامة تبويب جدول البيانات باستخدام Aspose.Cells لـ .NET 

```csharp
//المسار إلى دليل المستندات.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// إنشاء مثيل لكائن المصنف
// فتح ملف إكسل
Workbook workbook = new Workbook(dataDir + "book1.xls");
// إخفاء علامات التبويب في ملف Excel
workbook.Settings.ShowTabs = true;
// حفظ ملف Excel المعدل
workbook.Save(dataDir + "output.xls");
```

### خاتمة

يوضح لك هذا الدليل خطوة بخطوة كيفية إظهار علامة تبويب جدول بيانات Excel باستخدام Aspose.Cells لـ .NET. باستخدام كود مصدر C# المقدم، يمكنك بسهولة تخصيص عرض علامات التبويب في ملفات Excel الخاصة بك.

### أسئلة وأجوبة (FAQ)

#### ما هو Aspose.Cells لـ .NET؟

Aspose.Cells for .NET هي مكتبة قوية لمعالجة ملفات Excel في تطبيقات .NET.

#### كيف يمكنني تثبيت Aspose.Cells لـ .NET؟

 لتثبيت Aspose.Cells لـ .NET، يتعين عليك تنزيل الحزمة ذات الصلة من[إصدارات Aspose](https://releases/aspose.com/cells/net/) وإضافته إلى مشروع .NET الخاص بك.

#### كيفية عرض علامة تبويب جدول بيانات Excel باستخدام Aspose.Cells لـ .NET؟

 يمكنك استخدام ال`ShowTabs` ملكية`Workbook.Settings` الكائن وتعيينه على`true` لإظهار علامة تبويب ورقة العمل.

#### ما هي تنسيقات ملفات Excel الأخرى التي يدعمها Aspose.Cells لـ .NET؟

يدعم Aspose.Cells for .NET مجموعة متنوعة من تنسيقات ملفات Excel، مثل XLS، وXLSX، وCSV، وHTML، وPDF، وما إلى ذلك.
