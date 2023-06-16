---
title: تجميد أجزاء من ورقة العمل
linktitle: تجميد أجزاء من ورقة العمل
second_title: Aspose.Cells لمرجع .NET API
description: تلاعب بسهولة بأجزاء التجميد في ورقة عمل Excel باستخدام Aspose.Cells for .NET.
type: docs
weight: 70
url: /ar/net/excel-display-settings-csharp-tutorials/freeze-panes-of-worksheet/
---
في هذا البرنامج التعليمي ، سنوضح لك كيفية قفل الأجزاء في ورقة عمل Excel باستخدام كود المصدر C # مع Aspose.Cells for .NET. اتبع الخطوات أدناه للحصول على النتيجة المرجوة.

## الخطوة 1: استيراد المكتبات الضرورية

تأكد من تثبيت مكتبة Aspose.Cells لـ .NET واستورد المكتبات الضرورية إلى مشروع C # الخاص بك.

```csharp
using Aspose.Cells;
```

## الخطوة 2: قم بتعيين مسار الدليل وافتح ملف Excel

 عيّن المسار إلى الدليل الذي يحتوي على ملف Excel ، ثم افتح الملف عن طريق إنشاء ملف`Workbook` هدف.

```csharp
string dataDir = "YOUR DOCUMENTS DIRECTORY";
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
Workbook workbook = new Workbook(fstream);
```

## الخطوة 3: انتقل إلى جدول البيانات وقم بتطبيق إعدادات قفل الجزء

 انتقل إلى ورقة العمل الأولى في ملف Excel باستخدام ملحق`Worksheet` هدف. ثم استخدم ملف`FreezePanes` طريقة لتطبيق إعدادات تأمين الجزء.

```csharp
Worksheet worksheet = workbook.Worksheets[0];
worksheet. FreezePanes(3, 2, 3, 2);
```

في المثال أعلاه ، تم تأمين الأجزاء بالخلية الموجودة في الصف 3 والعمود 2.

## الخطوة 4: حفظ التغييرات

 بمجرد إجراء التغييرات اللازمة ، احفظ ملف Excel المعدل باستخدام امتداد`Save` طريقة`Workbook` هدف.

```csharp
workbook.Save(dataDir + "output.xls");
```

### نموذج التعليمات البرمجية المصدر لتجميد أجزاء من ورقة العمل باستخدام Aspose.Cells لـ .NET 

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
// تطبيق إعدادات تجميد الأجزاء
worksheet.FreezePanes(3, 2, 3, 2);
// حفظ ملف Excel المعدل
workbook.Save(dataDir + "output.xls");
// إغلاق دفق الملف لتحرير جميع الموارد
fstream.Close();
```

## خاتمة

يوضح لك هذا الدليل التفصيلي كيفية قفل الأجزاء في جدول بيانات Excel باستخدام Aspose.Cells for .NET. باستخدام الكود المصدري C # المقدم ، يمكنك بسهولة تخصيص إعدادات قفل الجزء لتنظيم وتصور بياناتك بشكل أفضل في ملفات Excel.

### أسئلة وأجوبة (FAQ)

#### ما هو Aspose.Cells لـ .NET؟

Aspose.Cells for .NET مكتبة قوية لمعالجة ملفات Excel في تطبيقات .NET.

#### كيف يمكنني تثبيت Aspose.Cells for .NET؟

 لتثبيت Aspose.Cells for .NET ، تحتاج إلى تنزيل الحزمة ذات الصلة من[إصدارات Aspose](https://releases/aspose.com/cells/net/) وإضافته إلى مشروع .NET الخاص بك.

#### كيفية قفل الأجزاء في ورقة عمل Excel باستخدام Aspose.Cells for .NET؟

 يمكنك استخدام ال`FreezePanes` طريقة`Worksheet` كائن لتأمين أجزاء ورقة العمل. حدد الخلايا المراد قفلها من خلال توفير فهارس الصفوف والأعمدة.

#### هل يمكنني تخصيص إعدادات قفل الجزء باستخدام Aspose.Cells for .NET؟

 نعم ، باستخدام ملف`FreezePanes` الطريقة ، يمكنك تحديد الخلايا المطلوب قفلها حسب الحاجة ، مع توفير فهارس الصفوف والأعمدة المناسبة.
