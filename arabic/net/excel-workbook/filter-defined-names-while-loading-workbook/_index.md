---
title: تصفية الأسماء المعرفة أثناء تحميل المصنف
linktitle: تصفية الأسماء المعرفة أثناء تحميل المصنف
second_title: Aspose.Cells لمرجع .NET API
description: تعرف على كيفية تصفية الأسماء المحددة عند تحميل مصنف Excel باستخدام Aspose.Cells for .NET.
type: docs
weight: 100
url: /ar/net/excel-workbook/filter-defined-names-while-loading-workbook/
---
عند العمل مع مصنفات Excel في تطبيق .NET ، غالبًا ما يكون من الضروري تصفية البيانات عند التحميل. Aspose.Cells for .NET مكتبة قوية للتعامل بسهولة مع مصنفات Excel. في هذا الدليل ، سنوضح لك كيفية تصفية الأسماء المحددة عند تحميل مصنف باستخدام Aspose.Cells for .NET. اتبع هذه الخطوات البسيطة للحصول على النتائج المرجوة:

## الخطوة 1: حدد خيارات التحميل

أولاً ، تحتاج إلى تحديد خيارات التحميل لتحديد سلوك تحميل المصنف. في حالتنا ، نريد تجاهل الأسماء المحددة عند التحميل. إليك كيفية القيام بذلك باستخدام Aspose.Cells:

```csharp
// يحدد خيارات التحميل
LoadOptions opts = new LoadOptions();

// لا تقم بتحميل أسماء محددة
opts. LoadFilter = new LoadFilter(~LoadDataFilterOptions.DefinedNames);
```

## الخطوة 2: قم بتحميل المصنف

بمجرد تكوين خيارات التحميل ، يمكنك تحميل مصنف Excel من الملف المصدر. تأكد من تحديد مسار الملف الصحيح. إليك نموذج التعليمات البرمجية:

```csharp
// قم بتحميل المصنف
Workbook wb = new Workbook(sourceDir + "sampleFilterDefinedNamesWhileLoadingWorkbook.xlsx", opts);
```

## الخطوة 3: احفظ المصنف الذي تمت تصفيته

بعد تحميل المصنف ، يمكنك إجراء عمليات أو تعديلات أخرى حسب الحاجة. ثم يمكنك حفظ المصنف الذي تمت تصفيته في ملف الإخراج. إليك الطريقة:

```csharp
// احفظ مصنف Excel الذي تمت تصفيته
wb.Save(outputDir + "outputFilterDefinedNamesWhileLoadingWorkbook.xlsx");
```

### نموذج التعليمات البرمجية المصدر لـ Filter Defined Names أثناء تحميل المصنف باستخدام Aspose.Cells for .NET 
```csharp
//حدد خيارات التحميل
LoadOptions opts = new LoadOptions();
//لا نريد تحميل الأسماء المعرفة
opts.LoadFilter = new LoadFilter(~LoadDataFilterOptions.DefinedNames);
//قم بتحميل المصنف
Workbook wb = new Workbook(sourceDir + "sampleFilterDefinedNamesWhileLoadingWorkbook.xlsx", opts);
//احفظ ملف Excel الناتج ، وسوف يكسر الصيغة في C1
wb.Save(outputDir + "outputFilterDefinedNamesWhileLoadingWorkbook.xlsx");
Console.WriteLine("FilterDefinedNamesWhileLoadingWorkbook executed successfully.");
```

## خاتمة

يمكن أن تكون تصفية الأسماء المحددة عند تحميل مصنف Excel أمرًا بالغ الأهمية للعديد من التطبيقات. يجعل Aspose.Cells for .NET هذه المهمة أسهل من خلال توفير خيارات مرنة لتحميل البيانات وتصفيتها. باتباع الخطوات الواردة في هذا الدليل ، ستتمكن من تصفية الأسماء المحددة بفعالية وتحقيق النتائج المرجوة في مصنفات Excel الخاصة بك.


### أسئلة وأجوبة

#### س: هل تدعم Aspose.Cells لغات برمجة أخرى إلى جانب C #؟
    
ج: نعم ، Aspose.Cells هي مكتبة متعددة المنصات تدعم العديد من لغات البرمجة مثل Java و Python و C++، و أكثر من ذلك بكثير.

#### س: هل يمكنني تصفية أنواع البيانات الأخرى عند تحميل مصنف باستخدام Aspose.Cells؟
    
ج: نعم ، تقدم Aspose.Cells مجموعة من خيارات التصفية للبيانات بما في ذلك الصيغ والأنماط ووحدات الماكرو وما إلى ذلك.

#### س: هل تحتفظ Aspose.Cells بتنسيق وخصائص المصنف الأصلي؟
    
ج: نعم ، Aspose.Cells تحتفظ بالتنسيق والأنماط والصيغ والخصائص الأخرى للمصنف الأصلي عند العمل مع ملفات Excel.