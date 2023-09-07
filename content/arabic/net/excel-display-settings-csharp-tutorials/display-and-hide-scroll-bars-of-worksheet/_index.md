---
title: عرض وإخفاء أشرطة التمرير لورقة العمل
linktitle: عرض وإخفاء أشرطة التمرير لورقة العمل
second_title: Aspose.Cells لمرجع .NET API
description: عرض أو إخفاء أشرطة التمرير في ورقة عمل Excel باستخدام Aspose.Cells for .NET.
type: docs
weight: 50
url: /ar/net/excel-display-settings-csharp-tutorials/display-and-hide-scroll-bars-of-worksheet/
---
في هذا البرنامج التعليمي ، سنوضح لك كيفية عرض أو إخفاء أشرطة التمرير الرأسية والأفقية في ورقة عمل Excel باستخدام كود المصدر C # مع Aspose.Cells for .NET. اتبع الخطوات أدناه للحصول على النتيجة المرجوة.

## الخطوة 1: استيراد المكتبات الضرورية

تأكد من تثبيت مكتبة Aspose.Cells لـ .NET واستورد المكتبات الضرورية إلى مشروع C # الخاص بك.

```csharp
using Aspose.Cells;
using System.IO;
```

## الخطوة 2: قم بتعيين مسار الدليل وافتح ملف Excel

 عيّن المسار إلى الدليل الذي يحتوي على ملف Excel الخاص بك ، ثم افتح الملف عن طريق إنشاء دفق ملف وإنشاء ملف`Workbook` هدف.

```csharp
string dataDir = "YOUR DOCUMENTS DIRECTORY";
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
Workbook workbook = new Workbook(fstream);
```

## الخطوة 3: إخفاء أشرطة التمرير

 استخدم ال`IsVScrollBarVisible` و`IsHScrollBarVisible` خصائص`Workbook.Settings` كائن لإخفاء أشرطة التمرير الرأسية والأفقية لورقة العمل.

```csharp
workbook.Settings.IsVScrollBarVisible = false;
workbook.Settings.IsHScrollBarVisible = false;
```

## الخطوة 4: حفظ التغييرات

 بمجرد إجراء التغييرات اللازمة ، احفظ ملف Excel المعدل باستخدام امتداد`Save` طريقة`Workbook` هدف.

```csharp
workbook.Save(dataDir + "output.xls");
```

### عينة من التعليمات البرمجية المصدر لعرض وإخفاء أشرطة التمرير لورقة العمل باستخدام Aspose.Cells for .NET 

```csharp
// المسار إلى دليل المستندات.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// إنشاء دفق ملف يحتوي على ملف Excel ليتم فتحه
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
// إنشاء كائن مصنف
// فتح ملف Excel من خلال تدفق الملفات
Workbook workbook = new Workbook(fstream);
// إخفاء شريط التمرير العمودي لملف Excel
workbook.Settings.IsVScrollBarVisible = false;
// إخفاء شريط التمرير الأفقي لملف Excel
workbook.Settings.IsHScrollBarVisible = false;
// حفظ ملف Excel المعدل
workbook.Save(dataDir + "output.xls");
// إغلاق دفق الملف لتحرير جميع الموارد
fstream.Close();
```

### خاتمة

يوضح لك هذا الدليل التفصيلي كيفية عرض أو إخفاء أشرطة التمرير الرأسية والأفقية في جدول بيانات Excel باستخدام Aspose.Cells for .NET. باستخدام الكود المصدري C # المقدم ، يمكنك بسهولة تخصيص عرض أشرطة التمرير في ملفات Excel.

### أسئلة وأجوبة (FAQ)

#### ما هو Aspose.Cells لـ .NET؟

Aspose.Cells for .NET مكتبة قوية لمعالجة ملفات Excel في تطبيقات .NET.

#### كيف يمكنني تثبيت Aspose.Cells for .NET؟

 لتثبيت Aspose.Cells for .NET ، تحتاج إلى تنزيل الحزمة ذات الصلة من[إصدارات Aspose](https://releases/aspose.com/cells/net/) وإضافته إلى مشروع .NET الخاص بك.

#### كيف يمكنني عرض أو إخفاء أشرطة التمرير في جدول بيانات Excel باستخدام Aspose.Cells for .NET؟

 يمكنك استخدام ال`IsVScrollBarVisible` و`IsHScrollBarVisible` خصائص`Workbook.Settings` لعرض أو إخفاء شريط التمرير العمودي والأفقي على التوالي في ورقة عمل Excel.

#### ما هي تنسيقات ملفات Excel الأخرى التي يدعمها Aspose.Cells لـ .NET؟

يدعم Aspose.Cells for .NET مجموعة متنوعة من تنسيقات ملفات Excel ، مثل XLS و XLSX و CSV و HTML و PDF وما إلى ذلك.