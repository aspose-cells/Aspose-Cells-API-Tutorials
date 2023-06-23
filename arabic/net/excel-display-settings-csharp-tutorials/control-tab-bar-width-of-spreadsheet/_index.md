---
title: عرض شريط علامة تبويب التحكم في جدول البيانات
linktitle: عرض شريط علامة تبويب التحكم في جدول البيانات
second_title: Aspose.Cells لمرجع .NET API
description: تحكم في عرض شريط علامات التبويب في جدول بيانات Excel باستخدام Aspose.Cells for .NET.
type: docs
weight: 10
url: /ar/net/excel-display-settings-csharp-tutorials/control-tab-bar-width-of-spreadsheet/
---
في هذا البرنامج التعليمي ، سنوضح لك كيفية التحكم في عرض شريط علامات التبويب في ورقة عمل Excel باستخدام كود المصدر C # مع Aspose.Cells for .NET. اتبع الخطوات أدناه للحصول على النتيجة المرجوة.

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

## الخطوة 3: إخفاء علامات تبويب ورقة العمل

 لإخفاء علامات تبويب ورقة العمل ، يمكنك استخدام ملحق`ShowTabs` ممتلكات`Settings` كائن`Workbook` فصل. اضبطه على`false` لإخفاء علامات التبويب.

```csharp
workbook.Settings.ShowTabs = false;
```

## الخطوة 4: ضبط عرض شريط الجدولة

 لضبط عرض شريط علامة تبويب ورقة العمل ، يمكنك استخدام ملف`SheetTabBarWidth` ممتلكات`Settings` كائن`Workbook` فصل. اضبطه على القيمة المطلوبة (بالنقاط) لضبط العرض.

```csharp
workbook.Settings.SheetTabBarWidth = 800;
```

## الخطوة 5: حفظ التغييرات

 بمجرد إجراء التغييرات اللازمة ، احفظ ملف Excel المعدل باستخدام امتداد`Save` طريقة`Workbook` هدف.

```csharp
workbook.Save(dataDir + "output.xls");
```

### نموذج التعليمات البرمجية المصدر لـ Control Tab Bar Width Of Spreadsheet باستخدام Aspose.Cells for .NET 
```csharp
// المسار إلى دليل المستندات.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// إنشاء كائن مصنف
// فتح ملف إكسل
Workbook workbook = new Workbook(dataDir + "book1.xls");
// إخفاء علامات تبويب ملف الإكسل
workbook.Settings.ShowTabs = true;
// ضبط عرض شريط علامة تبويب الورقة
workbook.Settings.SheetTabBarWidth = 800;
// حفظ ملف Excel المعدل
workbook.Save(dataDir + "output.xls");
```

## خاتمة

يوضح لك هذا الدليل التفصيلي كيفية التحكم في عرض شريط علامات التبويب في ورقة عمل Excel باستخدام Aspose.Cells for .NET. باستخدام الكود المصدري C # المقدم ، يمكنك بسهولة تخصيص عرض شريط علامات التبويب في ملفات Excel الخاصة بك.

## أسئلة وأجوبة (FAQ)

#### ما هو Aspose.Cells لـ .NET؟

Aspose.Cells for .NET مكتبة قوية لمعالجة ملفات Excel في تطبيقات .NET.

#### كيف يمكنني تثبيت Aspose.Cells for .NET؟

 لتثبيت Aspose.Cells for .NET ، تحتاج إلى تنزيل الحزمة ذات الصلة من[إصدارات Aspose](https://releases/aspose.com/cells/net/) وإضافته إلى مشروع .NET الخاص بك.

#### ما هي الميزات التي تقدمها Aspose.Cells for .NET؟

يوفر Aspose.Cells for .NET العديد من الميزات ، مثل إنشاء ملفات Excel وتعديلها وتحويلها ومعالجتها.

#### كيفية إخفاء علامات التبويب في جدول بيانات Excel باستخدام Aspose.Cells for .NET؟

 يمكنك إخفاء علامات تبويب ورقة العمل باستخدام ملحق`ShowTabs` ممتلكات`Settings` كائن`Workbook` الطبقة وضبطها على`false`.

#### كيفية ضبط عرض شريط علامات التبويب باستخدام Aspose.Cells لـ .NET؟

يمكنك ضبط عرض شريط علامات التبويب باستخدام ملف`SheetTabBarWidth` ممتلكات`Settings` كائن`Workbook` فئة وتعيين قيمة عددية لها بالنقاط.