---
title: نسخ إعدادات إعداد الصفحة من ورقة عمل أخرى
linktitle: نسخ إعدادات إعداد الصفحة من ورقة عمل أخرى
second_title: Aspose.Cells لمرجع .NET API
description: تعرف على كيفية نسخ إعدادات تكوين الصفحة من جدول بيانات إلى آخر باستخدام Aspose.Cells for .NET. دليل خطوة بخطوة لتحسين استخدام هذه المكتبة.
type: docs
weight: 10
url: /ar/net/excel-page-setup/copy-page-setup-settings-from-other-worksheet/
---
في هذه المقالة ، سوف نأخذك خطوة بخطوة لشرح التعليمات البرمجية المصدر C # التالية: نسخ إعدادات تكوين الصفحة من جدول بيانات آخر باستخدام Aspose.Cells for .NET. سنستخدم مكتبة Aspose.Cells لـ .NET لإجراء هذه العملية. إذا كنت تريد نسخ إعدادات إعداد الصفحة من ورقة عمل إلى أخرى ، فاتبع الخطوات أدناه.

## الخطوة 1: إنشاء المصنف
الخطوة الأولى هي إنشاء مصنف. في حالتنا ، سوف نستخدم فئة Workbook التي توفرها مكتبة Aspose.Cells. إليك التعليمات البرمجية لإنشاء مصنف:

```csharp
Workbook wb = new Workbook();
```

## الخطوة 2: إضافة أوراق عمل الاختبار
بعد إنشاء المصنف ، نحتاج إلى إضافة أوراق عمل الاختبار. في هذا المثال ، سنضيف ورقتي عمل. إليك الكود لإضافة ورقتي عمل:

```csharp
wb.Worksheets.Add("TestSheet1");
wb.Worksheets.Add("TestSheet2");
```

## الخطوة 3: الوصول إلى أوراق العمل
الآن بعد أن أضفنا أوراق العمل ، نحتاج إلى الوصول إليها حتى نتمكن من تغيير إعداداتها. سنصل إلى أوراق العمل "TestSheet1" و "TestSheet2" باستخدام أسمائهم. ها هو الكود للوصول إليه:

```csharp
Worksheet TestSheet1 = wb. Worksheets["TestSheet1"];
Worksheet TestSheet2 = wb. Worksheets["TestSheet2"];
```

## الخطوة 4: ضبط حجم الورق
 في هذه الخطوة ، سنقوم بتعيين حجم الورق لورقة العمل "TestSheet1". سوف نستخدم ملف`PageSetup.PaperSize` خاصية لتعيين حجم الورق. على سبيل المثال ، سنقوم بتعيين حجم الورق على "PaperA3ExtraTransverse". هذا هو الكود الخاص بذلك:

```csharp
TestSheet1.PageSetup.PaperSize = PaperSizeType.PaperA3ExtraTransverse;
```

## الخطوة 5: نسخ إعدادات إعداد الصفحة
سنقوم الآن بنسخ إعدادات تكوين الصفحة من ورقة العمل "TestSheet1" إلى "TestSheet2". سوف نستخدم ملف`PageSetup.Copy` طريقة إجراء هذه العملية. هذا هو الكود الخاص بذلك:

```csharp
TestSheet2.PageSetup.Copy(TestSheet1.PageSetup, new CopyOptions());
```

## الخطوة 6: أحجام ورق الطباعة
 بعد نسخ إعدادات إعداد الصفحة ، سنقوم بطباعة أحجام ورق ورقتي العمل. سوف نستخدم`Console.WriteLine` لعرض أحجام الورق. هذا هو الكود الخاص بذلك:

```csharp
Console.WriteLine("Before Paper Size: " + TestSheet1.PageSetup.PaperSize);
Console.WriteLine("Before Paper Size: " + TestSheet2.PageSetup.PaperSize);
```

### نموذج التعليمات البرمجية المصدر لنسخ إعدادات إعداد الصفحة من ورقة عمل أخرى باستخدام Aspose.Cells for .NET 
```csharp
//إنشاء مصنف
Workbook wb = new Workbook();
//أضف ورقتي عمل اختبار
wb.Worksheets.Add("TestSheet1");
wb.Worksheets.Add("TestSheet2");
//قم بالوصول إلى ورقتي العمل TestSheet1 و TestSheet2
Worksheet TestSheet1 = wb.Worksheets["TestSheet1"];
Worksheet TestSheet2 = wb.Worksheets["TestSheet2"];
//اضبط حجم الورق في TestSheet1 على PaperA3ExtraTransverse
TestSheet1.PageSetup.PaperSize = PaperSizeType.PaperA3ExtraTransverse;
//اطبع حجم الورق لكلتا ورقتي العمل
Console.WriteLine("Before Paper Size: " + TestSheet1.PageSetup.PaperSize);
Console.WriteLine("Before Paper Size: " + TestSheet2.PageSetup.PaperSize);
Console.WriteLine();
//انسخ PageSetup من TestSheet1 إلى TestSheet2
TestSheet2.PageSetup.Copy(TestSheet1.PageSetup, new CopyOptions());
//اطبع حجم الورق لكلتا ورقتي العمل
Console.WriteLine("After Paper Size: " + TestSheet1.PageSetup.PaperSize);
Console.WriteLine("After Paper Size: " + TestSheet2.PageSetup.PaperSize);
Console.WriteLine();
Console.WriteLine("CopyPageSetupSettingsFromSourceWorksheetToDestinationWorksheet executed successfully.\r\n");
```

## خاتمة
في هذه المقالة ، تعلمنا كيفية نسخ إعدادات تكوين الصفحة من ورقة عمل إلى أخرى باستخدام Aspose.Cells for .NET. لقد ذهبنا من خلال الخطوات التالية: إنشاء المصنف ، وإضافة أوراق عمل الاختبار ، والوصول إلى أوراق العمل ، وتعيين حجم الورق ، ونسخ إعدادات إعداد الصفحة ، وطباعة أحجام الورق. يمكنك الآن استخدام هذه المعرفة لنسخ إعدادات تكوين الصفحة إلى مشاريعك الخاصة.

### أسئلة وأجوبة

#### س: هل يمكنني نسخ إعدادات تكوين الصفحة بين مثيلات المصنف المختلفة؟

 ج: نعم ، يمكنك نسخ إعدادات إعداد الصفحة بين مثيلات المصنف المختلفة باستخدام ملف`PageSetup.Copy` طريقة مكتبة Aspose.Cells.

#### س: هل يمكنني نسخ إعدادات إعداد الصفحة الأخرى ، مثل الاتجاه أو الهوامش؟

 ج: نعم ، يمكنك نسخ إعدادات إعداد الصفحة الأخرى باستخدام ملف`PageSetup.Copy` الطريقة مع الخيارات المناسبة. على سبيل المثال ، يمكنك نسخ الاتجاه باستخدام`CopyOptions.Orientation` والهوامش باستخدام`CopyOptions.Margins`.

#### س: كيف أعرف الخيارات المتوفرة لحجم الورق؟

ج: يمكنك التحقق من مرجع واجهة برمجة تطبيقات مكتبة Aspose.Cells لمعرفة الخيارات المتاحة لحجم الورق. هناك تعداد يسمى`PaperSizeType` الذي يسرد أحجام الورق المختلفة المدعومة.

#### س: كيف يمكنني تنزيل مكتبة Aspose.Cells لـ .NET؟

 ج: يمكنك تنزيل مكتبة Aspose.Cells لـ .NET من[إصدارات Aspose](https://releases.aspose.com/cells/net). تتوفر إصدارات تجريبية مجانية ، بالإضافة إلى تراخيص مدفوعة للاستخدام التجاري.

#### س: هل تدعم مكتبة Aspose.Cells لغات البرمجة الأخرى؟

ج: نعم ، تدعم مكتبة Aspose.Cells لغات برمجة متعددة بما في ذلك C # و Java و Python وغيرها الكثير.