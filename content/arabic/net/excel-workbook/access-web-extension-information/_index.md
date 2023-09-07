---
title: الوصول إلى معلومات ملحق الويب
linktitle: الوصول إلى معلومات ملحق الويب
second_title: Aspose.Cells لمرجع .NET API
description: الوصول إلى معلومات امتداد الويب باستخدام Aspose.Cells for .NET.
type: docs
weight: 10
url: /ar/net/excel-workbook/access-web-extension-information/
---
يعد الوصول إلى معلومات امتداد الويب ميزة أساسية عند تطوير التطبيقات باستخدام Aspose.Cells for .NET. في هذا الدليل خطوة بخطوة ، سنشرح الكود المصدري C # الذي سيتيح لك الوصول إلى معلومات امتداد الويب باستخدام Aspose.Cells for .NET. سنقدم لك أيضًا استنتاجًا وإجابة بتنسيق Markdown لتسهيل الفهم. اتبع الخطوات أدناه للحصول على معلومات قيمة حول ملحقات الويب.

## الخطوة 1: تعيين دليل المصدر

```csharp
// دليل المصدر
string sourceDir = RunExamples.Get_SourceDirectory();
```

في هذه الخطوة الأولى ، نحدد الدليل المصدر الذي سيتم استخدامه لتحميل ملف Excel الذي يحتوي على معلومات امتداد الويب.

## الخطوة 2: قم بتحميل ملف Excel

```csharp
// قم بتحميل ملف Excel كمثال
Workbook workbook = new Workbook(sourceDir + "WebExtensionsSample.xlsx");
```

هنا نقوم بتحميل نموذج ملف Excel الذي يحتوي على معلومات امتداد الويب التي نريد استردادها.

## الخطوة 3: الوصول إلى المعلومات من نافذة مهمة ملحق الويب

```csharp
WebExtensionTaskPaneCollection taskPanes = workbook.Worksheets.WebExtensionTaskPanes;
foreach(WebExtensionTaskPane taskPane in taskPanes)
{
Console.WriteLine("Width: " + taskPane.Width);
Console.WriteLine("Is visible: " + taskPane.IsVisible);
Console.WriteLine("Is locked: " + taskPane.IsLocked);
Console.WriteLine("Docking State: " + taskPane.DockState);
Console.WriteLine("Store Name: " + taskPane.WebExtension.Reference.StoreName);
Console.WriteLine("Store type: " + taskPane.WebExtension.Reference.StoreType);
Console.WriteLine("Web Extension ID: " + taskPane.WebExtension.Id);
}
```

في هذه الخطوة ، نقوم بالوصول إلى معلومات كل نافذة مهمة امتداد ويب موجودة في ملف Excel. نعرض خصائص مختلفة مثل العرض والرؤية وحالة القفل والحالة الرئيسية واسم المتجر ونوع المتجر ومعرف امتداد الويب.

## الخطوة 4: إظهار رسالة النجاح

```csharp
Console.WriteLine("AccessWebExtensionInformation executed successfully.");
```

أخيرًا ، نعرض رسالة تشير إلى أنه تم الوصول إلى معلومات امتداد الويب بنجاح.

### نموذج التعليمات البرمجية المصدر لـ Access Web Extension Information باستخدام Aspose.Cells لـ .NET 
```csharp
//دليل المصدر
string sourceDir = RunExamples.Get_SourceDirectory();
//تحميل ملف Excel عينة
Workbook workbook = new Workbook(sourceDir + "WebExtensionsSample.xlsx");
WebExtensionTaskPaneCollection taskPanes = workbook.Worksheets.WebExtensionTaskPanes;
foreach (WebExtensionTaskPane taskPane in taskPanes)
{
	Console.WriteLine("Width: " + taskPane.Width);
	Console.WriteLine("IsVisible: " + taskPane.IsVisible);
	Console.WriteLine("IsLocked: " + taskPane.IsLocked);
	Console.WriteLine("DockState: " + taskPane.DockState);
	Console.WriteLine("StoreName: " + taskPane.WebExtension.Reference.StoreName);
	Console.WriteLine("StoreType: " + taskPane.WebExtension.Reference.StoreType);
	Console.WriteLine("WebExtension.Id: " + taskPane.WebExtension.Id);
}
Console.WriteLine("AccessWebExtensionInformation executed successfully.");
```

## خاتمة

في هذا البرنامج التعليمي ، تعلمنا كيفية الوصول إلى معلومات امتداد الويب باستخدام Aspose.Cells for .NET. باتباع الخطوات المقدمة ، ستتمكن من استخراج معلومات نوافذ المهام بسهولة من امتداد ويب إلى ملف Excel.


### أسئلة وأجوبة

#### س: ما هو Aspose.Cells لـ .NET؟

ج: Aspose.Cells for .NET هي مكتبة فصول قوية تسمح لمطوري .NET بإنشاء وتعديل وتحويل ومعالجة ملفات Excel بسهولة.

#### س: هل تدعم Aspose.Cells لغات البرمجة الأخرى؟

ج: نعم ، تدعم Aspose.Cells لغات برمجة متعددة مثل C # و VB.NET و Java و PHP و Python وما إلى ذلك.

#### س: هل يمكنني استخدام Aspose.Cells في المشاريع التجارية؟

ج: نعم ، Aspose.Cells هي مكتبة تجارية ويمكن استخدامها في المشاريع التجارية وفقًا لاتفاقية الترخيص.

#### س: هل هناك وثائق إضافية حول Aspose.Cells؟

ج: نعم ، يمكنك التحقق من وثائق Aspose.Cells الكاملة على موقع Aspose الرسمي لمزيد من المعلومات والموارد.