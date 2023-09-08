---
title: تجميد أجزاء من ورقة العمل
linktitle: تجميد أجزاء من ورقة العمل
second_title: Aspose.Cells لمرجع .NET API
description: يمكنك التعامل بسهولة مع أجزاء التجميد في ورقة عمل Excel باستخدام Aspose.Cells لـ .NET.
type: docs
weight: 70
url: /ar/net/excel-display-settings-csharp-tutorials/freeze-panes-of-worksheet/
---
سنوضح لك في هذا البرنامج التعليمي كيفية قفل الأجزاء في ورقة عمل Excel باستخدام كود مصدر C# مع Aspose.Cells for .NET. اتبع الخطوات أدناه للحصول على النتيجة المرجوة.

## الخطوة 1: استيراد المكتبات اللازمة

تأكد من تثبيت مكتبة Aspose.Cells لـ .NET واستيراد المكتبات الضرورية إلى مشروع C# الخاص بك.

```csharp
using Aspose.Cells;
```

## الخطوة 2: قم بتعيين مسار الدليل وافتح ملف Excel

 قم بتعيين المسار إلى الدليل الذي يحتوي على ملف Excel الخاص بك، ثم افتح الملف عن طريق إنشاء مثيل لـ`Workbook` هدف.

```csharp
string dataDir = "YOUR DOCUMENTS DIRECTORY";
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
Workbook workbook = new Workbook(fstream);
```

## الخطوة 3: انتقل إلى جدول البيانات وقم بتطبيق إعدادات قفل الجزء

 انتقل إلى ورقة العمل الأولى في ملف Excel باستخدام الملف`Worksheet` هدف. ثم استخدم`FreezePanes` طريقة لتطبيق إعدادات قفل الجزء.

```csharp
Worksheet worksheet = workbook.Worksheets[0];
worksheet. FreezePanes(3, 2, 3, 2);
```

في المثال أعلاه، يتم قفل الأجزاء بالخلية الموجودة في الصف 3 والعمود 2.

## الخطوة 4: حفظ التغييرات

 بمجرد إجراء التغييرات اللازمة، احفظ ملف Excel المعدل باستخدام الملف`Save` طريقة`Workbook` هدف.

```csharp
workbook.Save(dataDir + "output.xls");
```

### نموذج التعليمات البرمجية المصدر لتجميد أجزاء ورقة العمل باستخدام Aspose.Cells لـ .NET 

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
// تطبيق إعدادات أجزاء التجميد
worksheet.FreezePanes(3, 2, 3, 2);
// حفظ ملف Excel المعدل
workbook.Save(dataDir + "output.xls");
// إغلاق دفق الملف لتحرير كافة الموارد
fstream.Close();
```

## خاتمة

يوضح لك هذا الدليل خطوة بخطوة كيفية قفل الأجزاء في جدول بيانات Excel باستخدام Aspose.Cells for .NET. باستخدام كود مصدر C# المقدم، يمكنك بسهولة تخصيص إعدادات قفل اللوحة لتنظيم بياناتك وتصورها بشكل أفضل في ملفات Excel.

### أسئلة وأجوبة (FAQ)

#### ما هو Aspose.Cells لـ .NET؟

Aspose.Cells for .NET هي مكتبة قوية لمعالجة ملفات Excel في تطبيقات .NET.

#### كيف يمكنني تثبيت Aspose.Cells لـ .NET؟

 لتثبيت Aspose.Cells لـ .NET، يتعين عليك تنزيل الحزمة ذات الصلة من[إصدارات Aspose](https://releases/aspose.com/cells/net/) وإضافته إلى مشروع .NET الخاص بك.

#### كيفية قفل الأجزاء في ورقة عمل Excel باستخدام Aspose.Cells لـ .NET؟

 يمكنك استخدام ال`FreezePanes` طريقة`Worksheet` كائن لتأمين أجزاء ورقة العمل. حدد الخلايا المراد قفلها من خلال توفير فهارس الصفوف والأعمدة.

#### هل يمكنني تخصيص إعدادات قفل الجزء باستخدام Aspose.Cells لـ .NET؟

 نعم باستخدام`FreezePanes` الطريقة، يمكنك تحديد الخلايا التي سيتم قفلها حسب الحاجة، مع توفير فهارس الصفوف والأعمدة المناسبة.
