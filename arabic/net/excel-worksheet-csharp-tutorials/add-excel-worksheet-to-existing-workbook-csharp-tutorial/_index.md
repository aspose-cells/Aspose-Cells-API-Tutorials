---
title: أضف ورقة عمل Excel إلى المصنف الحالي C # البرنامج التعليمي
linktitle: أضف ورقة عمل Excel إلى المصنف الحالي
second_title: Aspose.Cells لمرجع .NET API
description: أضف ورقة جديدة بسهولة إلى مصنف Excel موجود باستخدام Aspose.Cells for .NET. خطوة بخطوة البرنامج التعليمي مع أمثلة التعليمات البرمجية.
type: docs
weight: 10
url: /ar/net/excel-worksheet-csharp-tutorials/add-excel-worksheet-to-existing-workbook-csharp-tutorial/
---
في هذا البرنامج التعليمي ، سوف نأخذك خطوة بخطوة لشرح الكود المصدري C # أدناه ، مما يساعد على إضافة ورقة جديدة إلى مصنف Excel موجود باستخدام Aspose.Cells for .NET. سنقوم بتضمين نموذج التعليمات البرمجية لكل خطوة لمساعدتك على فهم العملية بالتفصيل.

## الخطوة 1: تحديد دليل المستندات

للبدء ، تحتاج إلى تعيين مسار الدليل حيث يوجد ملف Excel الخاص بك. استبدل "دليل المستند" في الكود بالمسار الفعلي لملف Excel.

```csharp
// المسار إلى دليل المستندات.
string dataDir = "YOUR DOCUMENT DIRECTORY";
```

## الخطوة 2: قم بإنشاء دفق ملف وافتح ملف Excel

 بعد ذلك ، تحتاج إلى إنشاء دفق ملف وفتح ملف Excel باستخدام ملحق`FileStream` فصل.

```csharp
// قم بإنشاء دفق ملف يحتوي على ملف Excel لفتحه
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
```

## الخطوة 3: إنشاء كائن مصنف

 بعد فتح ملف Excel ، تحتاج إلى إنشاء ملف`Workbook`هدف. يمثل هذا الكائن مصنف Excel ويقدم أساليب وخصائص متنوعة لمعالجة المصنف.

```csharp
// إنشاء كائن مصنف
// افتح ملف Excel عبر تدفق الملف
Workbook workbook = new Workbook(fstream);
```

## الخطوة 4: أضف ورقة جديدة إلى المصنف

 لإضافة ورقة عمل جديدة إلى المصنف ، يمكنك استخدام ملحق`Worksheets.Add()` طريقة`Workbook` هدف. تقوم هذه الطريقة بإرجاع فهرس الورقة المضافة حديثًا.

```csharp
// أضف ورقة جديدة إلى المصنف
int i = workbook. Worksheets. Add();
```

## الخطوة 5: تعيين اسم ورقة جديد

 يمكنك تعيين اسم الورقة المضافة حديثًا باستخدام ملف`Name` ممتلكات`Worksheet` هدف.

```csharp
// احصل على مرجع الورقة الجديدة المضافة عن طريق تمرير فهرس الورقة الخاص بها
Worksheet worksheet = workbook.Worksheets[i];
// حدد اسم الورقة الجديدة
worksheet.Name = "My Worksheet";
```

## الخطوة 6: احفظ ملف Excel

 بمجرد إضافة الورقة الجديدة وتعيين اسمها ، يمكنك حفظ ملف Excel المعدل باستخدام الامتداد`Save()` طريقة`Workbook` هدف.

```csharp
// احفظ ملف Excel
workbook.Save(dataDir + "output.out.xls");
```

## الخطوة 7: أغلق دفق الملفات وإصدار الموارد

أخيرًا ، من المهم إغلاق تدفق الملفات لتحرير جميع الموارد المرتبطة به.

```csharp
// أغلق دفق الملف لتحرير جميع الموارد
fstream.Close();
```

### نموذج التعليمات البرمجية المصدر لإضافة ورقة عمل Excel إلى البرنامج التعليمي الموجود في المصنف C # باستخدام Aspose.Cells for .NET 
```csharp
// المسار إلى دليل المستندات.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// إنشاء دفق ملف يحتوي على ملف Excel ليتم فتحه
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
// إنشاء كائن مصنف
// فتح ملف Excel من خلال تدفق الملفات
Workbook workbook = new Workbook(fstream);
// إضافة ورقة عمل جديدة إلى كائن المصنف
int i = workbook.Worksheets.Add();
// الحصول على مرجع ورقة العمل المضافة حديثًا عن طريق تمرير فهرس الورقة الخاص بها
Worksheet worksheet = workbook.Worksheets[i];
// تعيين اسم ورقة العمل المضافة حديثًا
worksheet.Name = "My Worksheet";
// حفظ ملف Excel
workbook.Save(dataDir + "output.out.xls");
// إغلاق دفق الملف لتحرير جميع الموارد
fstream.Close();
```

## خاتمة

في هذا البرنامج التعليمي ، قمنا بتغطية العملية خطوة بخطوة لإضافة Fire Connect جديد إلى مصنف Excel موجود باستخدام Aspose.Cells for .NET. باتباع أمثلة الشفرات والتوضيحات المقدمة ، يجب أن يكون لديك الآن فهم جيد لكيفية تنفيذ هذه المهمة في تطبيقات C # الخاصة بك. يوفر Aspose.Cells for .NET مجموعة شاملة من الميزات للعمل مع ملفات Excel ، مما يسمح لك بأتمتة المهام المختلفة المتعلقة بـ Excel بكفاءة.

### أسئلة وأجوبة (FAQ)

#### ما هو Aspose.Cells لـ .NET؟

Aspose.Cells for .NET هي مكتبة .NET قوية تتيح للمطورين إنشاء ومعالجة وتحويل ملفات Excel في تطبيقاتهم. يوفر مجموعة كبيرة من الميزات للعمل مع جداول البيانات والخلايا والصيغ والأنماط والمزيد.

#### كيف يمكنني تثبيت Aspose.Cells for .NET؟

لتثبيت Aspose.Cells for .NET ، يمكنك تنزيل حزمة التثبيت من إصدارات Aspose (https://releases.aspose.com/cells/net) واتبع تعليمات التثبيت المتوفرة. ستحتاج أيضًا إلى ترخيص صالح لاستخدام المكتبة في تطبيقاتك.

#### هل يمكنني إضافة جداول بيانات متعددة باستخدام Aspose.Cells لـ .NET؟

 نعم ، يمكنك إضافة أوراق عمل متعددة إلى ملف Excel واحد باستخدام Aspose.Cells for .NET. يمكنك استخدام ال`Worksheets.Add()` طريقة`Workbook` كائن لإضافة أوراق عمل جديدة في مواضع مختلفة في المصنف.

#### كيف يمكنني تنسيق الخلايا في ملف Excel؟

يوفر Aspose.Cells for .NET طرقًا وخصائص مختلفة لتنسيق الخلايا في ملف Excel. يمكنك تعيين قيم الخلية وتطبيق خيارات التنسيق مثل نمط الخط واللون والمحاذاة والحدود والمزيد. راجع الوثائق وعينة التعليمات البرمجية المقدمة من Aspose.Cells لمزيد من المعلومات التفصيلية حول تنسيق الخلية.

#### هل Aspose.Cells for .NET متوافق مع إصدارات Excel المختلفة؟

نعم ، Aspose.Cells for .NET متوافق مع إصدارات مختلفة من Excel بما في ذلك Excel 2003 و Excel 2007 و Excel 2010 و Excel 2013 و Excel 2016 و Excel 2019 و Excel لـ Office 365. وهو يدعم كل من التنسيق .xls والإصدارات الأحدث. xlsx.