---
title: الحصول على أبعاد الصفحة
linktitle: الحصول على أبعاد الصفحة
second_title: Aspose.Cells لمرجع .NET API
description: تعرف على كيفية استرداد أبعاد الصفحة في Excel باستخدام Aspose.Cells لـ .NET. دليل خطوة بخطوة مع الكود المصدري في C#.
type: docs
weight: 40
url: /ar/net/excel-page-setup/get-page-dimensions/
---
Aspose.Cells for .NET هي مكتبة قوية تتيح للمطورين العمل مع ملفات Microsoft Excel برمجياً. وهو يقدم مجموعة واسعة من الميزات لمعالجة مستندات Excel، بما في ذلك القدرة على الحصول على أبعاد الصفحة. في هذا البرنامج التعليمي، سنرشدك خلال خطوات استرداد أبعاد الصفحة باستخدام Aspose.Cells لـ .NET.

## الخطوة 1: إنشاء مثيل لفئة المصنف

للبدء، نحتاج إلى إنشاء مثيل لفئة Workbook، التي تمثل مصنف Excel. ويمكن تحقيق ذلك باستخدام الكود التالي:

```csharp
Workbook book = new Workbook();
```

## الخطوة 2: الوصول إلى جدول البيانات

بعد ذلك، نحتاج إلى الانتقال إلى ورقة العمل في المصنف حيث نريد تعيين أبعاد الصفحة. في هذا المثال، لنفترض أننا نريد العمل مع ورقة العمل الأولى. يمكننا الوصول إليه باستخدام الكود التالي:

```csharp
Worksheet sheet = book.Worksheets[0];
```

## الخطوة 3: اضبط حجم الورق على A2 وعرض الطباعة وارتفاعها بالبوصة

الآن سنقوم بتعيين حجم الورق على A2 وطباعة عرض الصفحة وارتفاعها بالبوصة. ويمكن تحقيق ذلك باستخدام الكود التالي:

```csharp
sheet.PageSetup.PaperSize = PaperSizeType.PaperA2;
Console.WriteLine("A2: " + sheet.PageSetup.PaperWidth + "x" + sheet.PageSetup.PaperHeight);
```

## الخطوة 4: اضبط حجم الورق على A3 وعرض الطباعة وارتفاعها بالبوصة

بعد ذلك، سنقوم بتعيين حجم الورق على A3 وطباعة عرض الصفحة وارتفاعها بالبوصة. هنا هو الكود المقابل:

```csharp
sheet.PageSetup.PaperSize = PaperSizeType.PaperA3;
Console.WriteLine("A3: " + sheet.PageSetup.PaperWidth + "x" + sheet.PageSetup.PaperHeight);
```

## الخطوة 5: اضبط حجم الورق على A4 وعرض الطباعة وارتفاعها بالبوصة

سنقوم الآن بتعيين حجم الورق على A4 وطباعة عرض الصفحة وارتفاعها بالبوصة. هنا هو الرمز:

```csharp
sheet.PageSetup.PaperSize = PaperSizeType.PaperA4;
Console.WriteLine("A4: " + sheet.PageSetup.PaperWidth + "x" + sheet.PageSetup.PaperHeight);
```

## الخطوة 6: اضبط حجم الورق على Letter واطبع العرض والارتفاع بالبوصة

أخيرًا، سنقوم بتعيين حجم الورق على Letter وطباعة عرض الصفحة وارتفاعها بالبوصة. هنا هو الرمز:

```csharp
sheet.PageSetup.PaperSize = PaperSizeType.PaperLetter;
Console.WriteLine("Letter: " + sheet.PageSetup.PaperWidth + "x" + sheet.PageSetup.PaperHeight);
```

### نموذج التعليمات البرمجية المصدر للحصول على أبعاد الصفحة باستخدام Aspose.Cells لـ .NET 
```csharp
// إنشاء مثيل لفئة المصنف
Workbook book = new Workbook();
// الوصول إلى ورقة العمل الأولى
Worksheet sheet = book.Worksheets[0];
// اضبط حجم الورق على A2 واطبع عرض الورق وارتفاعه بالبوصة
sheet.PageSetup.PaperSize = PaperSizeType.PaperA2;
Console.WriteLine("PaperA2: " + sheet.PageSetup.PaperWidth + "x" + sheet.PageSetup.PaperHeight);
// اضبط حجم الورق على A3 وقم بطباعة عرض الورق وارتفاعه بالبوصة
sheet.PageSetup.PaperSize = PaperSizeType.PaperA3;
Console.WriteLine("PaperA3: " + sheet.PageSetup.PaperWidth + "x" + sheet.PageSetup.PaperHeight);
// اضبط حجم الورق على A4 وطباعة عرض الورق وارتفاعه بالبوصة
sheet.PageSetup.PaperSize = PaperSizeType.PaperA4;
Console.WriteLine("PaperA4: " + sheet.PageSetup.PaperWidth + "x" + sheet.PageSetup.PaperHeight);
// اضبط حجم الورق على Letter وقم بطباعة عرض الورق وارتفاعه بالبوصة
sheet.PageSetup.PaperSize = PaperSizeType.PaperLetter;
Console.WriteLine("PaperLetter: " + sheet.PageSetup.PaperWidth + "x" + sheet.PageSetup.PaperHeight);
Console.WriteLine("GetPageDimensions executed successfully.\r\n");
```

## خاتمة

تهنئة ! لقد تعلمت كيفية استرداد أبعاد الصفحة باستخدام Aspose.Cells لـ .NET. يمكن أن تكون هذه الميزة مفيدة عندما تحتاج إلى تنفيذ عمليات محددة بناءً على أبعاد الصفحة في ملفات Excel الخاصة بك.

لا تنسَ مواصلة استكشاف وثائق Aspose.Cells لاكتشاف جميع الميزات القوية التي تقدمها.

### الأسئلة الشائعة

#### 1. ما هي أحجام الورق الأخرى التي يدعمها Aspose.Cells لـ .NET؟

يدعم Aspose.Cells for .NET مجموعة متنوعة من أحجام الورق بما في ذلك A1 وA5 وB4 وB5 وExecutive وLegal وLetter وغيرها الكثير. يمكنك التحقق من الوثائق للحصول على القائمة الكاملة لأحجام الورق المدعومة.

#### 2. هل يمكنني تعيين أبعاد صفحة مخصصة باستخدام Aspose.Cells لـ .NET؟

نعم، يمكنك تعيين أبعاد الصفحة المخصصة عن طريق تحديد العرض والارتفاع المطلوبين. يوفر Aspose.Cells المرونة الكاملة لتخصيص أبعاد الصفحة وفقًا لاحتياجاتك.

#### 3. هل يمكنني الحصول على أبعاد الصفحة بوحدات غير البوصة؟

نعم، يتيح لك Aspose.Cells for .NET الحصول على أبعاد الصفحة بوحدات مختلفة، بما في ذلك البوصة والسنتيمتر والمليمتر والنقاط.

#### 4. هل يدعم Aspose.Cells for .NET ميزات تحرير إعدادات الصفحة الأخرى؟

نعم، تقدم Aspose.Cells مجموعة كاملة من الميزات لتحرير إعدادات الصفحة، بما في ذلك ضبط الهوامش والاتجاه والرؤوس والتذييلات وما إلى ذلك.