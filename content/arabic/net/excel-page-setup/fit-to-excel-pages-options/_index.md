---
title: تناسب خيارات صفحات Excel
linktitle: تناسب خيارات صفحات Excel
second_title: Aspose.Cells لمرجع .NET API
description: تعرف على كيفية احتواء الصفحات تلقائيًا في جدول بيانات Excel باستخدام Aspose.Cells for .NET.
type: docs
weight: 30
url: /ar/net/excel-page-setup/fit-to-excel-pages-options/
---
في هذه المقالة ، سوف نأخذك خطوة بخطوة لشرح كود مصدر C # التالي: خيارات ملائمة لصفحات Excel باستخدام Aspose.Cells for .NET. سنستخدم مكتبة Aspose.Cells لـ .NET لإجراء هذه العملية. اتبع الخطوات أدناه لتكوين الملاءمة للصفحات في Excel.

## الخطوة 1: إنشاء مصنف
الخطوة الأولى هي إنشاء مصنف. سنقوم بإنشاء مثيل لكائن مصنف. إليك التعليمات البرمجية لإنشاء مصنف:

```csharp
// المسار إلى دليل المستندات
string dataDir = "YOUR_DIRECTORY_OF_DOCUMENTS";

// إنشاء كائن مصنف
Workbook workbook = new Workbook();
```

## الخطوة 2: الوصول إلى ورقة العمل
الآن بعد أن أنشأنا المصنف ، نحتاج إلى الانتقال إلى ورقة العمل الأولى. سنستخدم الفهرس 0 للوصول إلى الورقة الأولى. ها هو الكود للوصول إليه:

```csharp
// الوصول إلى ورقة العمل الأولى في المصنف
Worksheet worksheet = workbook.Worksheets[0];
```

## الخطوة 3: ضبط الملاءمة للصفحات
 في هذه الخطوة ، سنقوم بتكوين التعديل على صفحات ورقة العمل. سوف نستخدم ملف`FitToPagesTall` و`FitToPagesWide` خصائص`PageSetup` لتحديد عدد الصفحات المطلوب لارتفاع وعرض ورقة العمل. هذا هو الكود الخاص بذلك:

```csharp
// قم بتكوين عدد الصفحات لارتفاع ورقة العمل
worksheet.PageSetup.FitToPagesTall = 1;

// قم بتكوين عدد الصفحات لعرض ورقة العمل
worksheet.PageSetup.FitToPagesWide = 1;
```

## الخطوة 4: حفظ المصنف
 الآن بعد أن قمنا بتكوين الملاءمة للصفحات ، يمكننا حفظ المصنف. سوف نستخدم ملف`Save` طريقة كائن المصنف لهذا الغرض. هذا هو الكود لحفظ المصنف:

```csharp
// احفظ المصنف
workbook.Save(dataDir + "FitToPagesOptions_out.xls");
```

### نموذج التعليمات البرمجية المصدر لخيارات Fit To Excel Pages باستخدام Aspose.Cells لـ .NET 
```csharp
// المسار إلى دليل المستندات.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// إنشاء كائن مصنف
Workbook workbook = new Workbook();
// الوصول إلى ورقة العمل الأولى في ملف Excel
Worksheet worksheet = workbook.Worksheets[0];
// تعيين عدد الصفحات التي سيتم توزيع طول ورقة العمل عليها
worksheet.PageSetup.FitToPagesTall = 1;
//تعيين عدد الصفحات التي سيتم عرض ورقة العمل عليها
worksheet.PageSetup.FitToPagesWide = 1;
// احفظ المصنف.
workbook.Save(dataDir + "FitToPagesOptions_out.xls");
```

## خاتمة
في هذه المقالة ، تعلمنا كيفية تكوين الملاءمة للصفحات في Excel باستخدام Aspose.Cells لـ .NET. انتقلنا من خلال الخطوات التالية: إنشاء المصنف ، والوصول إلى ورقة العمل ، وتكوين الملاءمة للصفحات ، وحفظ المصنف. الآن يمكنك استخدام هذه المعرفة لضبط جداول البيانات الخاصة بك على الصفحات المطلوبة.

### أسئلة وأجوبة

#### س: كيف يمكنني تثبيت Aspose.Cells لـ .NET؟

ج: لتثبيت Aspose.Cells for .NET ، يمكنك استخدام مدير الحزم NuGet في Visual Studio. ابحث عن حزمة Aspose.Cells وقم بتثبيتها في مشروعك.

#### س: هل يمكنني احتواء الصفحات من حيث الطول والعرض؟

 ج: نعم ، يمكنك ضبط ارتفاع ورقة العمل وعرضها باستخدام ملف`FitToPagesTall` و`FitToPagesWide` ملكيات. يمكنك تحديد عدد الصفحات المطلوب لكل بُعد.

#### س: كيف يمكنني تخصيص خيارات Fit to Pages؟

ج: بالإضافة إلى تحديد عدد الصفحات ، يمكنك أيضًا تخصيص خيارات أخرى مناسبة للصفحات مثل مقياس ورقة العمل واتجاه الورق والهوامش والمزيد. استخدم الخصائص المتوفرة في`PageSetup` كائن لهذا.

#### س: هل يمكنني استخدام Aspose.Cells لـ .NET لمعالجة المصنفات الحالية؟

ج: نعم ، يمكنك استخدام Aspose.Cells لـ .NET لفتح المصنفات الموجودة وتحريرها. يمكنك الوصول إلى أوراق العمل والخلايا والصيغ والأنماط وعناصر المصنف الأخرى لإجراء عمليات متنوعة.