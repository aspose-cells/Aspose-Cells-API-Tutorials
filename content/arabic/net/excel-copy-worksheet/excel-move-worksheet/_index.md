---
title: Excel نقل ورقة العمل
linktitle: Excel نقل ورقة العمل
second_title: Aspose.Cells لمرجع .NET API
description: انقل ورقة العمل بسهولة إلى مصنف Excel باستخدام Aspose.Cells for .NET.
type: docs
weight: 40
url: /ar/net/excel-copy-worksheet/excel-move-worksheet/
---
في هذا البرنامج التعليمي ، سنرشدك عبر خطوات نقل ورقة العمل إلى مصنف Excel باستخدام مكتبة Aspose.Cells لـ .NET. اتبع التعليمات أدناه لإكمال هذه المهمة.


## الخطوة الأولى: التحضير

تأكد من تثبيت Aspose.Cells لـ .NET وإنشاء مشروع C # في بيئة التطوير المتكاملة المفضلة لديك (IDE).

## الخطوة 2: قم بتعيين مسار دليل المستند

 تعلن أ`dataDir` متغير وتهيئته بالمسار إلى دليل المستندات. على سبيل المثال :

```csharp
string dataDir = "YOUR_DIRECTORY_OF_DOCUMENTS";
```

 تأكد من استبدال`"YOUR_DOCUMENTS_DIRECTORY"` مع المسار الفعلي للدليل الخاص بك.

## الخطوة 3: تحديد مسار ملف الإدخال

 نعلن`InputPath` متغيرًا وتهيئته بالمسار الكامل لملف Excel الحالي الذي تريد تعديله. على سبيل المثال :

```csharp
string InputPath = dataDir + "book1.xls";
```

 تأكد من أن لديك ملف Excel`book1.xls` في دليل المستندات الخاص بك أو تحديد اسم الملف الصحيح والموقع.

## الخطوة 4: افتح ملف Excel

 استخدم ال`Workbook` فئة Aspose.Cells لفتح ملف Excel المحدد:

```csharp
Workbook wb = new Workbook(InputPath);
```

## الخطوة 5: احصل على مجموعة جداول البيانات

 إنشاء`WorksheetCollection` كائن للإشارة إلى أوراق العمل في المصنف:

```csharp
WorksheetCollection sheets = wb.Worksheets;
```

## الخطوة 6: احصل على ورقة العمل الأولى

احصل على ورقة العمل الأولى في المصنف:

```csharp
Worksheet worksheet = sheets[0];
```

## الخطوة 7: انقل ورقة العمل

 استخدم ال`MoveTo` طريقة لنقل ورقة العمل الأولى إلى المركز الثالث في المصنف:

```csharp
worksheet.MoveTo(2);
```

## الخطوة 8: احفظ ملف Excel المعدل

احفظ ملف Excel بورقة العمل المنقولة:

```csharp
wb.Save(dataDir + "MoveWorksheet_out.xls");
```

تأكد من تحديد المسار المطلوب واسم الملف لملف الإخراج.

### نموذج التعليمات البرمجية المصدر لـ Excel Move Worksheet باستخدام Aspose.Cells for .NET 
```csharp
// المسار إلى دليل المستندات.
string dataDir = "YOUR DOCUMENT DIRECTORY";
string InputPath = dataDir + "book1.xls";
// افتح ملف Excel موجود.
Workbook wb = new Workbook(InputPath);
// قم بإنشاء كائن أوراق عمل بالإشارة إلى
// أوراق المصنف.
WorksheetCollection sheets = wb.Worksheets;
// احصل على ورقة العمل الأولى.
Worksheet worksheet = sheets[0];
// انقل الورقة الأولى إلى الموضع الثالث في المصنف.
worksheet.MoveTo(2);
// احفظ ملف اكسل.
wb.Save(dataDir + "MoveWorksheet_out.xls");
```

## خاتمة

تهنئة ! لقد تعلمت الآن كيفية نقل ورقة عمل إلى مصنف Excel باستخدام Aspose.Cells for .NET. لا تتردد في استخدام هذه الطريقة في مشاريعك الخاصة لمعالجة ملفات Excel بكفاءة.

### أسئلة وأجوبة

#### س هل يمكنني نقل ورقة عمل إلى موضع آخر في مصنف Excel نفسه؟

A.  نعم ، يمكنك نقل ورقة عمل إلى موضع آخر في نفس مصنف Excel باستخدام`MoveTo` طريقة كائن ورقة العمل. ما عليك سوى تحديد فهرس موضع الوجهة في المصنف.

#### س هل يمكنني نقل ورقة عمل إلى مصنف Excel آخر؟

A.  نعم ، يمكنك نقل ورقة عمل إلى مصنف Excel آخر باستخدام ملحق`MoveTo` طريقة كائن ورقة العمل. ما عليك سوى تحديد فهرس موضع الوجهة في المصنف الهدف.

#### س. هل تعمل التعليمات البرمجية المصدر المتوفرة مع تنسيقات ملفات Excel الأخرى ، مثل XLSX؟

A. نعم ، يعمل كود المصدر المقدم مع تنسيقات ملفات Excel الأخرى ، بما في ذلك XLSX. يدعم Aspose.Cells for .NET مجموعة متنوعة من تنسيقات ملفات Excel ، مما يسمح لك بمعالجة ورقة العمل ونقلها إلى أنواع ملفات مختلفة.

#### س كيف يمكنني تحديد مسار واسم ملف الإخراج عند حفظ ملف Excel المعدل؟

A.  عند حفظ ملف Excel المعدل ، استخدم ملحق`Save` أسلوب كائن المصنف يحدد المسار الكامل واسم ملف الإخراج. تأكد من تحديد امتداد الملف المناسب ، مثل`.xls` أو`.xlsx`، حسب تنسيق الملف المطلوب.