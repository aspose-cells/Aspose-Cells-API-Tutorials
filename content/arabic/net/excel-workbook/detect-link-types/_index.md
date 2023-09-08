---
title: كشف أنواع الارتباط
linktitle: كشف أنواع الارتباط
second_title: Aspose.Cells لمرجع .NET API
description: اكتشف أنواع الارتباطات في مصنف Excel باستخدام Aspose.Cells لـ .NET.
type: docs
weight: 80
url: /ar/net/excel-workbook/detect-link-types/
---
في هذا البرنامج التعليمي، سنرشدك عبر التعليمات البرمجية المصدر لـ C# المتوفرة خطوة بخطوة والتي ستسمح لك باكتشاف أنواع الروابط في مصنف Excel باستخدام Aspose.Cells for .NET. اتبع الخطوات أدناه لتنفيذ هذه العملية.

## الخطوة 1: تعيين الدليل المصدر

```csharp
// دليل المصدر
string SourceDir = RunExamples.Get_SourceDirectory();
```

في هذه الخطوة الأولى، نقوم بتحديد الدليل المصدر حيث يوجد مصنف Excel الذي يحتوي على الروابط.

## الخطوة 2: تحميل مصنف Excel

```csharp
// قم بتحميل مصنف Excel
Workbook workbook = new Workbook(SourceDir + "LinkTypes.xlsx");
```

نقوم بتحميل مصنف Excel باستخدام مسار الملف المصدر.

## الخطوة 3: الحصول على جدول البيانات

```csharp
// الحصول على ورقة العمل الأولى (افتراضي)
Worksheet worksheet = workbook.Worksheets[0];
```

 نحصل على ورقة العمل الأولى من المصنف. يمكنك تغيير`[0]` فهرس للوصول إلى ورقة عمل محددة إذا لزم الأمر.

## الخطوة 4: إنشاء نطاق من الخلايا

```csharp
// إنشاء نطاق من الخلايا A1:B3
Range range = worksheet.Cells.CreateRange("A1", "A7");
```

نقوم بإنشاء نطاق من الخلايا، في هذا المثال من الخلية A1 إلى الخلية A7. يمكنك ضبط مراجع الخلايا حسب الحاجة.

## الخطوة 5: احصل على الارتباطات التشعبية في النطاق

```csharp
// الحصول على الارتباطات التشعبية في النطاق
Hyperlink[] hyperlinks = range.Hyperlinks;
```

نحصل على كافة الارتباطات التشعبية الموجودة في النطاق المحدد.

## الخطوة 6: تصفح الارتباطات التشعبية وعرض أنواع الارتباطات

```csharp
foreach (Hyperlink link in hyperlinks)
{
Console.WriteLine(link.TextToDisplay + ": " + link.LinkType);
}
```

نقوم بالتكرار خلال كل رابط ونعرض نص العرض ونوع الرابط المرتبط به.

### نموذج التعليمات البرمجية المصدر لكشف أنواع الارتباطات باستخدام Aspose.Cells لـ .NET 
```csharp
//دليل المصدر
string SourceDir = RunExamples.Get_SourceDirectory();
Workbook workbook = new Workbook(SourceDir + "LinkTypes.xlsx");
// احصل على ورقة العمل الأولى (الافتراضية).
Worksheet worksheet = workbook.Worksheets[0];
// قم بإنشاء نطاق A2:B3
Range range = worksheet.Cells.CreateRange("A1", "A7");
// احصل على الارتباطات التشعبية في النطاق
Hyperlink[] hyperlinks = range.Hyperlinks;
foreach (Hyperlink link in hyperlinks)
{
	Console.WriteLine(link.TextToDisplay + ": " + link.LinkType);
}
Console.WriteLine("DetectLinkTypes executed successfully.");
```

## خاتمة

تهنئة ! لقد تعلمت كيفية اكتشاف أنواع الارتباطات في مصنف Excel باستخدام Aspose.Cells لـ .NET. تتيح لك هذه الميزة العمل مع الارتباطات التشعبية الموجودة في مصنفات Excel الخاصة بك. استمر في استكشاف ميزات Aspose.Cells لتوسيع إمكانات معالجة مصنفات Excel لديك.

### الأسئلة الشائعة

#### س: كيف يمكنني تثبيت Aspose.Cells لـ .NET في مشروعي؟

 ج: يمكنك تثبيت Aspose.Cells لـ .NET باستخدام مدير الحزم NuGet. بحث عن[إصدارات Aspose](https://releases.aspose.com/cells/net) في وحدة تحكم NuGet Package Manager وقم بتثبيت أحدث إصدار.

#### س: هل يمكنني اكتشاف أنواع الارتباطات في أوراق عمل محددة بدلاً من الورقة الأولى؟

 ج: نعم، يمكنك تعديل`workbook.Worksheets[0]` الفهرس للوصول إلى ورقة عمل محددة. على سبيل المثال، للوصول إلى الورقة الثانية، استخدم`workbook.Worksheets[1]`.

#### س: هل يمكن تعديل أنواع الروابط المكتشفة في النطاق؟

ج: نعم، يمكنك تصفح الارتباطات التشعبية وإجراء عمليات التحرير، مثل تحديث عناوين URL أو إزالة الروابط غير المرغوب فيها.

#### س: ما أنواع الروابط الممكنة في Aspose.Cells لـ .NET؟

ج: تتضمن أنواع الارتباطات المحتملة الارتباطات التشعبية، والروابط إلى أوراق العمل الأخرى، والارتباطات إلى الملفات الخارجية، والارتباطات إلى مواقع الويب، وما إلى ذلك.

#### س: هل يدعم Aspose.Cells for .NET إنشاء روابط جديدة في جدول بيانات؟

 ج: نعم، يدعم Aspose.Cells for .NET إنشاء روابط جديدة باستخدام`Hyperlink` الطبقة والخصائص المرتبطة بها. يمكنك إضافة ارتباطات تشعبية، وروابط إلى عناوين URL، وروابط إلى جداول بيانات أخرى، وما إلى ذلك.

#### س: هل يمكنني استخدام Aspose.Cells لـ .NET في تطبيقات الويب؟

ج: نعم، يمكن استخدام Aspose.Cells for .NET في تطبيقات الويب. يمكنك تضمينه في ASP.NET وASP.NET Core وأطر عمل الويب الأخرى المستندة إلى .NET.

#### س: هل هناك أي حدود لحجم الملف عند استخدام Aspose.Cells لـ .NET؟

ج: يمكن لـ Aspose.Cells for .NET معالجة مصنفات Excel الكبيرة دون قيود محددة. ومع ذلك، قد يكون حجم الملف الفعلي محدودًا بموارد النظام المتاحة.