---
title: الوصول إلى معلومات ملحق الويب
linktitle: الوصول إلى معلومات ملحق الويب
second_title: Aspose.Cells لمرجع .NET API
description: قم بالوصول إلى معلومات ملحق الويب باستخدام Aspose.Cells لـ .NET.
type: docs
weight: 10
url: /ar/net/excel-workbook/access-web-extension-information/
---
يعد الوصول إلى معلومات ملحق الويب ميزة أساسية عند تطوير التطبيقات باستخدام Aspose.Cells for .NET. في هذا الدليل خطوة بخطوة، سنشرح كود مصدر C# المقدم والذي سيسمح لك بالوصول إلى معلومات ملحق الويب باستخدام Aspose.Cells for .NET. سنزودك أيضًا باستنتاج وإجابة بتنسيق Markdown لتسهيل الفهم. اتبع الخطوات أدناه للحصول على معلومات قيمة حول ملحقات الويب.

## الخطوة 1: تعيين الدليل المصدر

```csharp
// دليل المصدر
string sourceDir = RunExamples.Get_SourceDirectory();
```

في هذه الخطوة الأولى، نحدد الدليل المصدر الذي سيتم استخدامه لتحميل ملف Excel الذي يحتوي على معلومات ملحق الويب.

## الخطوة 2: قم بتحميل ملف Excel

```csharp
// قم بتحميل مثال ملف Excel
Workbook workbook = new Workbook(sourceDir + "WebExtensionsSample.xlsx");
```

نقوم هنا بتحميل نموذج ملف Excel الذي يحتوي على معلومات ملحق الويب التي نريد استردادها.

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

في هذه الخطوة، نصل إلى المعلومات الخاصة بكل نافذة مهمة ملحق ويب موجودة في ملف Excel. نعرض خصائص مختلفة مثل العرض والرؤية وحالة القفل والحالة الرئيسية واسم المتجر ونوع المتجر ومعرف ملحق الويب.

## الخطوة 4: عرض رسالة النجاح

```csharp
Console.WriteLine("AccessWebExtensionInformation executed successfully.");
```

وأخيرًا، نعرض رسالة تشير إلى أنه تم الوصول إلى معلومات ملحق الويب بنجاح.

### نموذج التعليمات البرمجية المصدر لمعلومات Access Web Extension باستخدام Aspose.Cells لـ .NET 
```csharp
//دليل المصدر
string sourceDir = RunExamples.Get_SourceDirectory();
//قم بتحميل نموذج ملف Excel
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

في هذا البرنامج التعليمي، تعلمنا كيفية الوصول إلى معلومات ملحق الويب باستخدام Aspose.Cells لـ .NET. باتباع الخطوات المتوفرة، ستتمكن بسهولة من استخراج معلومات نوافذ المهام من امتداد الويب إلى ملف Excel.


### الأسئلة الشائعة

#### س: ما هو Aspose.Cells لـ .NET؟

ج: Aspose.Cells for .NET هي مكتبة فئة قوية تسمح لمطوري .NET بإنشاء ملفات Excel وتعديلها وتحويلها ومعالجتها بسهولة.

#### س: هل يدعم Aspose.Cells لغات البرمجة الأخرى؟

ج: نعم، يدعم Aspose.Cells لغات برمجة متعددة مثل C#، وVB.NET، وJava، وPHP، وPython، وما إلى ذلك.

#### س: هل يمكنني استخدام Aspose.Cells في المشاريع التجارية؟

ج: نعم، Aspose.Cells هي مكتبة تجارية ويمكن استخدامها في المشاريع التجارية بموجب اتفاقية الترخيص.

#### س: هل هناك وثائق إضافية حول Aspose.Cells؟

ج: نعم، يمكنك الاطلاع على وثائق Aspose.Cells الكاملة على موقع Aspose الرسمي لمزيد من المعلومات والموارد.