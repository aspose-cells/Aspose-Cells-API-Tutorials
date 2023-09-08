---
title: انسخ إعدادات إعداد الصفحة من ورقة عمل أخرى
linktitle: انسخ إعدادات إعداد الصفحة من ورقة عمل أخرى
second_title: Aspose.Cells لمرجع .NET API
description: تعرف على كيفية نسخ إعدادات تكوين الصفحة من جدول بيانات إلى آخر باستخدام Aspose.Cells لـ .NET. دليل خطوة بخطوة لتحسين استخدام هذه المكتبة.
type: docs
weight: 10
url: /ar/net/excel-page-setup/copy-page-setup-settings-from-other-worksheet/
---
في هذه المقالة، سنأخذك خطوة بخطوة لشرح التعليمات البرمجية المصدر لـ C# التالية: انسخ إعدادات تكوين الصفحة من جدول بيانات آخر باستخدام Aspose.Cells لـ .NET. سوف نستخدم مكتبة Aspose.Cells لـ .NET لإجراء هذه العملية. إذا كنت تريد نسخ إعدادات إعداد الصفحة من ورقة عمل إلى أخرى، فاتبع الخطوات أدناه.

## الخطوة 1: إنشاء المصنف
الخطوة الأولى هي إنشاء مصنف. في حالتنا، سوف نستخدم فئة Workbook التي توفرها مكتبة Aspose.Cells. إليك الكود لإنشاء مصنف:

```csharp
Workbook wb = new Workbook();
```

## الخطوة 2: إضافة أوراق عمل الاختبار
بعد إنشاء المصنف، نحتاج إلى إضافة أوراق عمل الاختبار. في هذا المثال، سوف نقوم بإضافة ورقتي عمل. إليك الكود لإضافة ورقتي عمل:

```csharp
wb.Worksheets.Add("TestSheet1");
wb.Worksheets.Add("TestSheet2");
```

## الخطوة 3: الوصول إلى أوراق العمل
الآن بعد أن أضفنا أوراق العمل، نحتاج إلى الوصول إليها حتى نتمكن من تغيير إعداداتها. سنصل إلى ورقتي العمل "TestSheet1" و"TestSheet2" باستخدام أسمائهما. إليك الرمز للوصول إليه:

```csharp
Worksheet TestSheet1 = wb. Worksheets["TestSheet1"];
Worksheet TestSheet2 = wb. Worksheets["TestSheet2"];
```

## الخطوة 4: تحديد حجم الورق
 في هذه الخطوة، سنقوم بتعيين حجم ورق ورقة العمل "TestSheet1". سوف نستخدم`PageSetup.PaperSize` خاصية ضبط حجم الورق على سبيل المثال، سوف نقوم بتعيين حجم الورق إلى "PaperA3ExtraTransverse". هنا هو الرمز لذلك:

```csharp
TestSheet1.PageSetup.PaperSize = PaperSizeType.PaperA3ExtraTransverse;
```

## الخطوة 5: نسخ إعدادات إعداد الصفحة
سنقوم الآن بنسخ إعدادات تكوين الصفحة من ورقة العمل "TestSheet1" إلى "TestSheet2". سوف نستخدم`PageSetup.Copy` طريقة تنفيذ هذه العملية. هنا هو الرمز لذلك:

```csharp
TestSheet2.PageSetup.Copy(TestSheet1.PageSetup, new CopyOptions());
```

## الخطوة 6: طباعة أحجام الورق
 بعد نسخ إعدادات إعداد الصفحة، سنقوم بطباعة أحجام الورق لورقتي العمل. سوف نستخدم`Console.WriteLine` لعرض أحجام الورق. هنا هو الرمز لذلك:

```csharp
Console.WriteLine("Before Paper Size: " + TestSheet1.PageSetup.PaperSize);
Console.WriteLine("Before Paper Size: " + TestSheet2.PageSetup.PaperSize);
```

### نموذج التعليمات البرمجية المصدر لنسخ إعدادات إعداد الصفحة من ورقة عمل أخرى باستخدام Aspose.Cells لـ .NET 
```csharp
//إنشاء المصنف
Workbook wb = new Workbook();
//إضافة ورقتي عمل للاختبار
wb.Worksheets.Add("TestSheet1");
wb.Worksheets.Add("TestSheet2");
//قم بالوصول إلى ورقتي العمل كـ TestSheet1 وTestSheet2
Worksheet TestSheet1 = wb.Worksheets["TestSheet1"];
Worksheet TestSheet2 = wb.Worksheets["TestSheet2"];
//اضبط حجم ورق ورقة الاختبار1 على PaperA3ExtraTransverse
TestSheet1.PageSetup.PaperSize = PaperSizeType.PaperA3ExtraTransverse;
//اطبع حجم الورق لكلا ورقتي العمل
Console.WriteLine("Before Paper Size: " + TestSheet1.PageSetup.PaperSize);
Console.WriteLine("Before Paper Size: " + TestSheet2.PageSetup.PaperSize);
Console.WriteLine();
//انسخ PageSetup من TestSheet1 إلى TestSheet2
TestSheet2.PageSetup.Copy(TestSheet1.PageSetup, new CopyOptions());
//اطبع حجم الورق لكلا ورقتي العمل
Console.WriteLine("After Paper Size: " + TestSheet1.PageSetup.PaperSize);
Console.WriteLine("After Paper Size: " + TestSheet2.PageSetup.PaperSize);
Console.WriteLine();
Console.WriteLine("CopyPageSetupSettingsFromSourceWorksheetToDestinationWorksheet executed successfully.\r\n");
```

## خاتمة
تعلمنا في هذه المقالة كيفية نسخ إعدادات تكوين الصفحة من ورقة عمل إلى أخرى باستخدام Aspose.Cells لـ .NET. لقد مررنا بالخطوات التالية: إنشاء المصنف، وإضافة أوراق عمل الاختبار، والوصول إلى أوراق العمل، وتعيين حجم الورق، ونسخ إعدادات إعداد الصفحة، وطباعة أحجام الورق. يمكنك الآن استخدام هذه المعرفة لنسخ إعدادات تكوين الصفحة إلى مشاريعك الخاصة.

### الأسئلة الشائعة

#### س: هل يمكنني نسخ إعدادات تكوين الصفحة بين مثيلات المصنف المختلفة؟

 ج: نعم، يمكنك نسخ إعدادات إعداد الصفحة بين مثيلات المصنف المختلفة باستخدام`PageSetup.Copy` طريقة مكتبة Aspose.Cells.

#### س: هل يمكنني نسخ إعدادات إعداد الصفحة الأخرى، مثل الاتجاه أو الهوامش؟

 ج: نعم، يمكنك نسخ إعدادات إعداد الصفحة الأخرى باستخدام`PageSetup.Copy` الطريقة مع الخيارات المناسبة على سبيل المثال، يمكنك نسخ الاتجاه باستخدام`CopyOptions.Orientation` والهوامش باستخدام`CopyOptions.Margins`.

#### س: كيف أعرف ما هي الخيارات المتاحة لحجم الورق؟

ج: يمكنك التحقق من مرجع واجهة برمجة تطبيقات مكتبة Aspose.Cells للتعرف على الخيارات المتاحة لحجم الورق. هناك تعداد يسمى`PaperSizeType` الذي يسرد أحجام الورق المدعومة المختلفة.

#### س: كيف يمكنني تنزيل مكتبة Aspose.Cells لـ .NET؟

 ج: يمكنك تنزيل مكتبة Aspose.Cells لـ .NET من[إصدارات Aspose](https://releases.aspose.com/cells/net). هناك إصدارات تجريبية مجانية متاحة، بالإضافة إلى تراخيص مدفوعة للاستخدام التجاري.

#### س: هل تدعم مكتبة Aspose.Cells لغات البرمجة الأخرى؟

ج: نعم، تدعم مكتبة Aspose.Cells لغات برمجة متعددة بما في ذلك C# وJava وPython وغيرها الكثير.