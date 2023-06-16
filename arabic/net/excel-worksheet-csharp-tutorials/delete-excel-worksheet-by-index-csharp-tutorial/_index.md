---
title: احذف ورقة عمل Excel حسب البرنامج التعليمي للفهرس C #
linktitle: احذف ورقة عمل Excel حسب الفهرس
second_title: Aspose.Cells لمرجع .NET API
description: احذف بسهولة ورقة عمل Excel معينة باستخدام Aspose.Cells for .NET. برنامج تعليمي مفصل مع أمثلة التعليمات البرمجية.
type: docs
weight: 30
url: /ar/net/excel-worksheet-csharp-tutorials/delete-excel-worksheet-by-index-csharp-tutorial/
---
في هذا البرنامج التعليمي ، سوف نأخذك خطوة بخطوة لشرح كود المصدر C # أدناه والذي هو حذف ورقة عمل Excel باستخدام Aspose.Cells for .NET. سنقوم بتضمين نموذج التعليمات البرمجية لكل خطوة لمساعدتك على فهم العملية بالتفصيل.

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

 بعد فتح ملف Excel ، تحتاج إلى إنشاء ملف`Workbook` هدف. يمثل هذا الكائن مصنف Excel ويقدم أساليب وخصائص متنوعة لمعالجة المصنف.

```csharp
// إنشاء كائن مصنف
// افتح ملف Excel عبر تدفق الملف
Workbook workbook = new Workbook(fstream);
```

## الخطوة 4: احذف ورقة عمل حسب الفهرس

 لإزالة ورقة عمل من فهرسها ، يمكنك استخدام ملحق`RemoveAt()` طريقة`Worksheets` كائن`Workbook` هدف. يجب أن يتم تمرير فهرس ورقة العمل التي تريد حذفها كمعامل.

```csharp
// احذف ورقة عمل باستخدام فهرس الورقة الخاص بها
workbook.Worksheets.RemoveAt(0);
```

## الخطوة 5: احفظ المصنف

 بمجرد حذف ورقة العمل ، يمكنك حفظ مصنف Excel المعدل باستخدام ملف`Save()` طريقة`Workbook` هدف.

```csharp
//احفظ مصنف Excel
workbook.Save(dataDir + "output.out.xls");
```


### نموذج التعليمات البرمجية المصدر لحذف ورقة عمل Excel حسب الفهرس C # البرنامج التعليمي باستخدام Aspose.Cells for .NET 
```csharp
// المسار إلى دليل المستندات.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// إنشاء دفق ملف يحتوي على ملف Excel ليتم فتحه
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
// إنشاء كائن مصنف
// فتح ملف Excel من خلال تدفق الملفات
Workbook workbook = new Workbook(fstream);
// إزالة ورقة عمل باستخدام فهرس الورقة الخاص بها
workbook.Worksheets.RemoveAt(0);
// حفظ المصنف
workbook.Save(dataDir + "output.out.xls");
```

## خاتمة

في هذا البرنامج التعليمي ، قمنا بتغطية العملية خطوة بخطوة لحذف ورقة عمل Excel بالفهرس باستخدام Aspose.Cells for .NET. باتباع أمثلة الشفرات والتوضيحات المقدمة ، يجب أن يكون لديك الآن فهم جيد لكيفية تنفيذ هذه المهمة في تطبيقات C # الخاصة بك. يوفر Aspose.Cells for .NET مجموعة شاملة من الميزات للعمل مع ملفات Excel ، مما يتيح لك معالجة أوراق العمل والبيانات ذات الصلة بسهولة.

### أسئلة وأجوبة (FAQ)

#### ما هو Aspose.Cells لـ .NET؟

Aspose.Cells for .NET مكتبة قوية تسمح للمطورين بإنشاء ومعالجة وتحويل ملفات Excel في تطبيقات .NET الخاصة بهم. يوفر مجموعة كبيرة من الميزات للعمل مع أوراق العمل والخلايا والصيغ والأنماط والمزيد.

#### كيف يمكنني تثبيت Aspose.Cells for .NET؟

لتثبيت Aspose.Cells for .NET ، يمكنك تنزيل حزمة التثبيت من إصدارات Aspose (https://releases.aspose.com/cells/net) واتبع التعليمات المقدمة. ستحتاج إلى ترخيص صالح لاستخدام المكتبة في تطبيقاتك.

#### هل يمكنني حذف أوراق عمل متعددة مرة واحدة؟

نعم ، يمكنك حذف أوراق عمل متعددة باستخدام Aspose.Cells for .NET. يمكنك ببساطة تكرار خطوة الحذف لكل ورقة عمل تريد حذفها.

#### هل من الممكن استعادة ورقة العمل المحذوفة؟

لسوء الحظ ، بمجرد حذف ورقة العمل ، لا يمكن استعادتها مباشرة من ملف Excel. يوصى بإنشاء نسخة احتياطية من ملف Excel الخاص بك قبل حذف ورقة العمل لتجنب فقدان البيانات.

#### هل Aspose.Cells for .NET متوافق مع إصدارات Excel المختلفة؟

نعم ، Aspose.Cells for .NET متوافق مع إصدارات مختلفة من Excel بما في ذلك Excel 2003 و Excel 2007 و Excel 2010 و Excel 2013 و Excel 2016 و Excel 2019 و Excel لـ Office 365. وهو يدعم تنسيقات الملفات .xls و .xlsx.