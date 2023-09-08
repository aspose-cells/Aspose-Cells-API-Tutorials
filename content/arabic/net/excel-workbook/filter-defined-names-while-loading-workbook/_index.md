---
title: تصفية الأسماء المعرفة أثناء تحميل المصنف
linktitle: تصفية الأسماء المعرفة أثناء تحميل المصنف
second_title: Aspose.Cells لمرجع .NET API
description: تعرف على كيفية تصفية الأسماء المحددة عند تحميل مصنف Excel باستخدام Aspose.Cells لـ .NET.
type: docs
weight: 100
url: /ar/net/excel-workbook/filter-defined-names-while-loading-workbook/
---
عند العمل مع مصنفات Excel في تطبيق .NET، غالبًا ما يكون من الضروري تصفية البيانات عند التحميل. Aspose.Cells for .NET هي مكتبة قوية للتعامل بسهولة مع مصنفات Excel. سنوضح لك في هذا الدليل كيفية تصفية الأسماء المحددة عند تحميل مصنف باستخدام Aspose.Cells for .NET. اتبع هذه الخطوات البسيطة للحصول على النتائج المرجوة:

## الخطوة 1: تحديد خيارات التحميل

أولاً، تحتاج إلى تحديد خيارات التحميل لتحديد سلوك تحميل المصنف. في حالتنا، نريد تجاهل الأسماء المعينة عند التحميل. وإليك كيفية القيام بذلك باستخدام Aspose.Cells:

```csharp
// يحدد خيارات التحميل
LoadOptions opts = new LoadOptions();

// لا تقم بتحميل الأسماء المحددة
opts. LoadFilter = new LoadFilter(~LoadDataFilterOptions.DefinedNames);
```

## الخطوة 2: تحميل المصنف

بمجرد تكوين خيارات التحميل، يمكنك تحميل مصنف Excel من الملف المصدر. تأكد من تحديد مسار الملف الصحيح. هنا نموذج التعليمات البرمجية:

```csharp
// قم بتحميل المصنف
Workbook wb = new Workbook(sourceDir + "sampleFilterDefinedNamesWhileLoadingWorkbook.xlsx", opts);
```

## الخطوة 3: احفظ المصنف الذي تمت تصفيته

بعد تحميل المصنف، يمكنك إجراء عمليات أو تعديلات أخرى حسب الحاجة. وبعد ذلك يمكنك حفظ المصنف الذي تمت تصفيته في ملف إخراج. إليك الطريقة:

```csharp
// احفظ مصنف Excel الذي تمت تصفيته
wb.Save(outputDir + "outputFilterDefinedNamesWhileLoadingWorkbook.xlsx");
```

### نموذج التعليمات البرمجية المصدر لتصفية الأسماء المحددة أثناء تحميل المصنف باستخدام Aspose.Cells لـ .NET 
```csharp
//حدد خيارات التحميل
LoadOptions opts = new LoadOptions();
//لا نريد تحميل الأسماء المحددة
opts.LoadFilter = new LoadFilter(~LoadDataFilterOptions.DefinedNames);
//قم بتحميل المصنف
Workbook wb = new Workbook(sourceDir + "sampleFilterDefinedNamesWhileLoadingWorkbook.xlsx", opts);
//احفظ ملف Excel الناتج، وسيؤدي إلى كسر الصيغة في C1
wb.Save(outputDir + "outputFilterDefinedNamesWhileLoadingWorkbook.xlsx");
Console.WriteLine("FilterDefinedNamesWhileLoadingWorkbook executed successfully.");
```

## خاتمة

يمكن أن تكون تصفية الأسماء المحددة عند تحميل مصنف Excel أمرًا بالغ الأهمية للعديد من التطبيقات. يعمل Aspose.Cells for .NET على تسهيل هذه المهمة من خلال توفير خيارات مرنة لتحميل البيانات وتصفيتها. باتباع الخطوات الواردة في هذا الدليل، ستتمكن من تصفية الأسماء المحددة بشكل فعال وتحقيق النتائج المطلوبة في مصنفات Excel الخاصة بك.


### الأسئلة الشائعة

#### س: هل يدعم Aspose.Cells لغات البرمجة الأخرى إلى جانب C#؟
    
ج: نعم، Aspose.Cells هي مكتبة متعددة المنصات تدعم العديد من لغات البرمجة مثل Java وPython وC++، و أكثر من ذلك بكثير.

#### س: هل يمكنني تصفية أنواع البيانات الأخرى عند تحميل مصنف باستخدام Aspose.Cells؟
    
ج: نعم، تقدم Aspose.Cells مجموعة من خيارات تصفية البيانات بما في ذلك الصيغ والأنماط ووحدات الماكرو وما إلى ذلك.

#### س: هل يحتفظ Aspose.Cells بتنسيق المصنف الأصلي وخصائصه؟
    
ج: نعم، يحتفظ Aspose.Cells بالتنسيق والأنماط والصيغ والخصائص الأخرى للمصنف الأصلي عند العمل مع ملفات Excel.