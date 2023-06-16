---
title: الحصول على عرض الورق وارتفاع ورقة العمل
linktitle: الحصول على عرض الورق وارتفاع ورقة العمل
second_title: Aspose.Cells لمرجع .NET API
description: قم بإنشاء دليل خطوة بخطوة لشرح التعليمات البرمجية المصدر C # التالية للحصول على عرض الورق وارتفاع جدول البيانات باستخدام Aspose.Cells for .NET.
type: docs
weight: 80
url: /ar/net/excel-display-settings-csharp-tutorials/get-paper-width-and-height-of-worksheet/
---
في هذا البرنامج التعليمي ، سوف نأخذك خطوة بخطوة لشرح التعليمات البرمجية المصدر C # التالية للحصول على عرض الورق وارتفاع ورقة العمل باستخدام Aspose.Cells for .NET. اتبع الخطوات التالية:

## الخطوة 1: قم بإنشاء المصنف
 ابدأ بإنشاء مصنف جديد باستخدام ملف`Workbook` فصل:

```csharp
Workbook wb = new Workbook();
```

## الخطوة 2: قم بالوصول إلى ورقة العمل الأولى
 بعد ذلك ، انتقل إلى ورقة العمل الأولى في المصنف باستخدام ملحق`Worksheet` فصل:

```csharp
Worksheet ws = wb.Worksheets[0];
```

## الخطوة 3: اضبط حجم الورق على A2 وأظهر عرض الورق وارتفاعه بالبوصة
 استخدم ال`PaperSize` ممتلكات`PageSetup` لتعيين حجم الورق على A2 ، ثم استخدم`PaperWidth` و`PaperHeight` خصائص للحصول على عرض الورق وارتفاعه على التوالي. اعرض هذه القيم باستخدام`Console.WriteLine` طريقة:

```csharp
ws.PageSetup.PaperSize = PaperSizeType.PaperA2;
Console.WriteLine("PaperA2: " + ws.PageSetup.PaperWidth + "x" + ws.PageSetup.PaperHeight);
```

## الخطوة 4: كرر الخطوات مع أحجام الورق الأخرى
كرر الخطوات السابقة ، وقم بتغيير حجم الورق إلى A3 ، و A4 ، و Letter ، ثم اعرض قيم عرض الورق وارتفاعه لكل حجم:

```csharp
ws.PageSetup.PaperSize = PaperSizeType.PaperA3;
Console.WriteLine("PaperA3: " + ws.PageSetup.PaperWidth + "x" + ws.PageSetup.PaperHeight);

ws.PageSetup.PaperSize = PaperSizeType.PaperA4;
Console.WriteLine("PaperA4: " + ws.PageSetup.PaperWidth + "x" + ws.PageSetup.PaperHeight);

ws.PageSetup.PaperSize = PaperSizeType.PaperLetter;
Console.WriteLine("PaperLetter: " + ws.PageSetup.PaperWidth + "x" + ws.PageSetup.PaperHeight);
```

### نموذج التعليمات البرمجية المصدر للحصول على عرض الورق وارتفاع ورقة العمل باستخدام Aspose.Cells لـ .NET 

```csharp
//إنشاء مصنف
Workbook wb = new Workbook();
//الوصول إلى ورقة العمل الأولى
Worksheet ws = wb.Worksheets[0];
//اضبط حجم الورق على A2 واطبع عرض الورق وارتفاعه بالبوصة
ws.PageSetup.PaperSize = PaperSizeType.PaperA2;
Console.WriteLine("PaperA2: " + ws.PageSetup.PaperWidth + "x" + ws.PageSetup.PaperHeight);
//اضبط حجم الورق على A3 واطبع عرض الورق وارتفاعه بالبوصة
ws.PageSetup.PaperSize = PaperSizeType.PaperA3;
Console.WriteLine("PaperA3: " + ws.PageSetup.PaperWidth + "x" + ws.PageSetup.PaperHeight);
//اضبط حجم الورق على A4 واطبع عرض الورق وارتفاعه بالبوصة
ws.PageSetup.PaperSize = PaperSizeType.PaperA4;
Console.WriteLine("PaperA4: " + ws.PageSetup.PaperWidth + "x" + ws.PageSetup.PaperHeight);
//اضبط حجم الورق على Letter واطبع عرض الورق وارتفاعه بالبوصة
ws.PageSetup.PaperSize = PaperSizeType.PaperLetter;
Console.WriteLine("PaperLetter: " + ws.PageSetup.PaperWidth + "x" + ws.PageSetup.PaperHeight);
```


## خاتمة

لقد تعلمت كيفية استخدام Aspose.Cells لـ .NET للحصول على عرض الورق وارتفاع جدول البيانات. يمكن أن تكون هذه الميزة مفيدة للتكوين والتخطيط الدقيق لمستندات Excel الخاصة بك.

### أسئلة وأجوبة (FAQ)

#### ما هو Aspose.Cells لـ .NET؟

Aspose.Cells for .NET مكتبة قوية لمعالجة ومعالجة ملفات Excel في تطبيقات .NET. يوفر العديد من الميزات لإنشاء وتعديل وتحويل وتحليل ملفات Excel.

#### كيف يمكنني الحصول على حجم ورق جدول البيانات باستخدام Aspose.Cells for .NET؟

 يمكنك استخدام ال`PageSetup` فئة من`Worksheet` كائن للوصول إلى حجم الورق. استخدم ال`PaperSize` لتعيين حجم الورق وملف`PaperWidth` و`PaperHeight` خصائص للحصول على عرض الورق وارتفاعه على التوالي.

#### ما هي أحجام الورق التي يدعمها Aspose.Cells for .NET؟

يدعم Aspose.Cells for .NET نطاقًا واسعًا من أحجام الورق شائعة الاستخدام ، مثل A2 و A3 و A4 و Letter ، بالإضافة إلى العديد من الأحجام المخصصة الأخرى.

#### هل يمكنني تخصيص حجم ورقة جدول بيانات باستخدام Aspose.Cells for .NET؟

نعم ، يمكنك تعيين حجم ورق مخصص عن طريق تحديد أبعاد العرض والارتفاع بدقة باستخدام تنسيق`PaperWidth` و`PaperHeight` خصائص`PageSetup` فصل.