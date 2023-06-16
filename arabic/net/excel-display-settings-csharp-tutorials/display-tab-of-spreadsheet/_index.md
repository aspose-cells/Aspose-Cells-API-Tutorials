---
title: عرض علامة تبويب جدول البيانات
linktitle: عرض علامة تبويب جدول البيانات
second_title: Aspose.Cells لمرجع .NET API
description: اعرض علامة تبويب جدول بيانات Excel باستخدام Aspose.Cells for .NET.
type: docs
weight: 60
url: /ar/net/excel-display-settings-csharp-tutorials/display-tab-of-spreadsheet/
---
في هذا البرنامج التعليمي ، سنوضح لك كيفية عرض علامة تبويب ورقة عمل Excel باستخدام كود المصدر C # مع Aspose.Cells for .NET. اتبع الخطوات أدناه للحصول على النتيجة المرجوة.

## الخطوة 1: استيراد المكتبات الضرورية

تأكد من تثبيت مكتبة Aspose.Cells لـ .NET واستورد المكتبات الضرورية إلى مشروع C # الخاص بك.

```csharp
using Aspose.Cells;
```

## الخطوة 2: قم بتعيين مسار الدليل وافتح ملف Excel

 عيّن المسار إلى الدليل الذي يحتوي على ملف Excel ، ثم افتح الملف عن طريق إنشاء ملف`Workbook` هدف.

```csharp
string dataDir = "YOUR DOCUMENTS DIRECTORY";
Workbook workbook = new Workbook(dataDir + "book1.xls");
```

## الخطوة 3: إظهار علامة تبويب ورقة العمل

 استخدم ال`ShowTabs` ممتلكات`Workbook.Settings` لإظهار علامة تبويب ورقة عمل Excel.

```csharp
workbook.Settings.ShowTabs = true;
```

## الخطوة 4: حفظ التغييرات

 بمجرد إجراء التغييرات اللازمة ، احفظ ملف Excel المعدل باستخدام امتداد`Save` طريقة`Workbook` هدف.

```csharp
workbook.Save(dataDir + "output.xls");
```

### نموذج التعليمات البرمجية المصدر لـ Display Tab Of Spreadsheet باستخدام Aspose.Cells for .NET 

```csharp
// المسار إلى دليل المستندات.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// إنشاء كائن مصنف
// فتح ملف إكسل
Workbook workbook = new Workbook(dataDir + "book1.xls");
// إخفاء علامات تبويب ملف الإكسل
workbook.Settings.ShowTabs = true;
// حفظ ملف Excel المعدل
workbook.Save(dataDir + "output.xls");
```

### خاتمة

يوضح لك هذا الدليل التفصيلي كيفية إظهار علامة تبويب جدول بيانات Excel باستخدام Aspose.Cells for .NET. باستخدام الكود المصدري C # المقدم ، يمكنك بسهولة تخصيص عرض علامات التبويب في ملفات Excel الخاصة بك.

### أسئلة وأجوبة (FAQ)

#### ما هو Aspose.Cells لـ .NET؟

Aspose.Cells for .NET مكتبة قوية لمعالجة ملفات Excel في تطبيقات .NET.

#### كيف يمكنني تثبيت Aspose.Cells for .NET؟

 لتثبيت Aspose.Cells for .NET ، تحتاج إلى تنزيل الحزمة ذات الصلة من[إصدارات Aspose](https://releases/aspose.com/cells/net/) وإضافته إلى مشروع .NET الخاص بك.

#### كيفية عرض علامة تبويب جدول بيانات Excel باستخدام Aspose.Cells for .NET؟

 يمكنك استخدام ال`ShowTabs` ممتلكات`Workbook.Settings` كائن وضبطه على`true`لإظهار علامة تبويب ورقة العمل.

#### ما هي تنسيقات ملفات Excel الأخرى التي يدعمها Aspose.Cells لـ .NET؟

يدعم Aspose.Cells for .NET مجموعة متنوعة من تنسيقات ملفات Excel ، مثل XLS و XLSX و CSV و HTML و PDF وما إلى ذلك.
