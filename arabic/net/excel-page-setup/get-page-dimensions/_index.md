---
title: احصل على أبعاد الصفحة
linktitle: احصل على أبعاد الصفحة
second_title: Aspose.Cells لمرجع .NET API
description: تعرف على كيفية استرداد أبعاد الصفحة في Excel باستخدام Aspose.Cells for .NET. دليل خطوة بخطوة مع شفرة المصدر في C #.
type: docs
weight: 40
url: /ar/net/excel-page-setup/get-page-dimensions/
---
Aspose.Cells for .NET مكتبة قوية تسمح للمطورين بالعمل مع ملفات Microsoft Excel برمجيًا. يوفر مجموعة واسعة من الميزات لمعالجة مستندات Excel ، بما في ذلك القدرة على الحصول على أبعاد الصفحة. في هذا البرنامج التعليمي ، سنرشدك عبر خطوات استرداد أبعاد الصفحة باستخدام Aspose.Cells for .NET.

## الخطوة 1: إنشاء مثيل لفئة المصنف

للبدء ، نحتاج إلى إنشاء مثيل لفئة المصنف ، والتي تمثل مصنف Excel. يمكن تحقيق ذلك باستخدام الكود التالي:

```csharp
Workbook book = new Workbook();
```

## الخطوة 2: الوصول إلى جدول البيانات

بعد ذلك ، نحتاج إلى الانتقال إلى ورقة العمل في المصنف حيث نريد تعيين أبعاد الصفحة. في هذا المثال ، افترض أننا نريد العمل بورقة العمل الأولى. يمكننا الوصول إليه باستخدام الكود التالي:

```csharp
Worksheet sheet = book.Worksheets[0];
```

## الخطوة 3: قم بتعيين حجم الورق على A2 وعرض الطباعة والارتفاع بالبوصة

الآن سنقوم بتعيين حجم الورق على A2 وطباعة عرض الصفحة وارتفاعها بالبوصة. يمكن تحقيق ذلك باستخدام الكود التالي:

```csharp
sheet.PageSetup.PaperSize = PaperSizeType.PaperA2;
Console.WriteLine("A2: " + sheet.PageSetup.PaperWidth + "x" + sheet.PageSetup.PaperHeight);
```

## الخطوة 4: اضبط حجم الورق على A3 وعرض الطباعة والارتفاع بالبوصة

بعد ذلك ، سنقوم بتعيين حجم الورق على A3 ونطبع عرض الصفحة وارتفاعها بالبوصة. هذا هو الكود المقابل:

```csharp
sheet.PageSetup.PaperSize = PaperSizeType.PaperA3;
Console.WriteLine("A3: " + sheet.PageSetup.PaperWidth + "x" + sheet.PageSetup.PaperHeight);
```

## الخطوة 5: قم بتعيين حجم الورق على A4 وطباعة العرض والارتفاع بالبوصة

سنقوم الآن بتعيين حجم الورق على A4 وطباعة عرض الصفحة وارتفاعها بالبوصة. ها هو الكود:

```csharp
sheet.PageSetup.PaperSize = PaperSizeType.PaperA4;
Console.WriteLine("A4: " + sheet.PageSetup.PaperWidth + "x" + sheet.PageSetup.PaperHeight);
```

## الخطوة 6: اضبط حجم الورق على Letter واطبع العرض والارتفاع بالبوصة

أخيرًا ، سنقوم بتعيين حجم الورق على Letter وطباعة عرض الصفحة وارتفاعها بالبوصة. ها هو الكود:

```csharp
sheet.PageSetup.PaperSize = PaperSizeType.PaperLetter;
Console.WriteLine("Letter: " + sheet.PageSetup.PaperWidth + "x" + sheet.PageSetup.PaperHeight);
```

### نموذج التعليمات البرمجية المصدر للحصول على أبعاد الصفحة باستخدام Aspose.Cells for .NET 
```csharp
// قم بإنشاء مثيل لفئة المصنف
Workbook book = new Workbook();
// الوصول إلى ورقة العمل الأولى
Worksheet sheet = book.Worksheets[0];
// اضبط حجم الورق على A2 واطبع عرض الورق وارتفاعه بالبوصة
sheet.PageSetup.PaperSize = PaperSizeType.PaperA2;
Console.WriteLine("PaperA2: " + sheet.PageSetup.PaperWidth + "x" + sheet.PageSetup.PaperHeight);
// اضبط حجم الورق على A3 واطبع عرض الورق وارتفاعه بالبوصة
sheet.PageSetup.PaperSize = PaperSizeType.PaperA3;
Console.WriteLine("PaperA3: " + sheet.PageSetup.PaperWidth + "x" + sheet.PageSetup.PaperHeight);
// اضبط حجم الورق على A4 واطبع عرض الورق وارتفاعه بالبوصة
sheet.PageSetup.PaperSize = PaperSizeType.PaperA4;
Console.WriteLine("PaperA4: " + sheet.PageSetup.PaperWidth + "x" + sheet.PageSetup.PaperHeight);
// اضبط حجم الورق على Letter واطبع عرض الورق وارتفاعه بالبوصة
sheet.PageSetup.PaperSize = PaperSizeType.PaperLetter;
Console.WriteLine("PaperLetter: " + sheet.PageSetup.PaperWidth + "x" + sheet.PageSetup.PaperHeight);
Console.WriteLine("GetPageDimensions executed successfully.\r\n");
```

## خاتمة

تهنئة ! لقد تعلمت كيفية استرداد أبعاد الصفحة باستخدام Aspose.Cells لـ .NET. يمكن أن تكون هذه الميزة مفيدة عندما تحتاج إلى إجراء عمليات محددة بناءً على أبعاد الصفحة في ملفات Excel الخاصة بك.

لا تنسَ مواصلة استكشاف توثيق Aspose.Cells لاكتشاف كل الميزات القوية التي تقدمها.

### التعليمات

#### 1. ما هي أحجام الورق الأخرى التي يدعمها Aspose.Cells لـ .NET؟

يدعم Aspose.Cells for .NET مجموعة متنوعة من أحجام الورق بما في ذلك A1 و A5 و B4 و B5 و Executive و Legal و Letter وغيرها الكثير. يمكنك التحقق من الوثائق للحصول على القائمة الكاملة لأحجام الورق المدعومة.

#### 2. هل يمكنني تعيين أبعاد الصفحة المخصصة باستخدام Aspose.Cells لـ .NET؟

نعم ، يمكنك تعيين أبعاد الصفحة المخصصة عن طريق تحديد العرض والارتفاع المطلوبين. يوفر Aspose.Cells مرونة كاملة لتخصيص أبعاد الصفحة حسب احتياجاتك.

#### 3. هل يمكنني الحصول على أبعاد الصفحة بوحدات غير البوصة؟

نعم ، يسمح لك Aspose.Cells for .NET بالحصول على أبعاد الصفحة بوحدات مختلفة ، بما في ذلك البوصات والسنتيمترات والملليمترات والنقاط.

#### 4. هل يدعم Aspose.Cells for .NET ميزات تحرير إعدادات الصفحة الأخرى؟

نعم ، Aspose.Cells تقدم مجموعة كاملة من الميزات لتحرير إعدادات الصفحة ، بما في ذلك ضبط الهوامش ، والاتجاه ، والرؤوس والتذييلات ، إلخ.