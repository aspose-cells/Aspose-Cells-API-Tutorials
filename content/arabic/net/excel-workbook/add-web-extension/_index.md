---
title: إضافة ملحق ويب
linktitle: إضافة ملحق ويب
second_title: Aspose.Cells لمرجع .NET API
description: أضف امتداد ويب إلى مصنفات Excel بسهولة باستخدام Aspose.Cells for .NET.
type: docs
weight: 40
url: /ar/net/excel-workbook/add-web-extension/
---
في هذا البرنامج التعليمي خطوة بخطوة ، سنشرح الكود المصدري C # المقدم والذي سيسمح لك بإضافة امتداد ويب باستخدام Aspose.Cells for .NET. اتبع الخطوات أدناه لإضافة ملحق ويب إلى مصنف Excel الخاص بك.

## الخطوة 1: تعيين دليل الإخراج

```csharp
// دليل الإخراج
string outDir = RunExamples.Get_OutputDirectory();
```

في هذه الخطوة الأولى ، نحدد دليل الإخراج حيث سيتم حفظ مصنف Excel المعدل.

## الخطوة 2: قم بإنشاء مصنف جديد

```csharp
//قم بإنشاء مصنف جديد
Workbook workbook = new Workbook();
```

 نحن هنا بصدد إنشاء مصنف Excel جديد باستخدام ملف`Workbook` فئة من Aspose.Cells.

## الخطوة 3: الوصول إلى مجموعة ملحقات الويب

```csharp
// الوصول إلى مجموعة من ملحقات الويب
WebExtensionCollection extensions = workbook.Worksheets.WebExtensions;
```

 نقوم بالوصول إلى مجموعة ملحقات الويب الخاصة بمصنف Excel باستخدام امتداد`WebExtensions` ممتلكات`Worksheets` هدف.

## الخطوة 4: قم بإضافة امتداد ويب جديد

```csharp
// إضافة امتداد ويب جديد
int extensionIndex = extensions.Add();
WebExtension extension = extensions[extensionIndex];
extension.Reference.Id = "wa104379955";
extension.Reference.StoreName = "en-US";
extension.Reference.StoreType = WebExtensionStoreType.OMEX;
```

نحن نضيف امتداد ويب جديدًا إلى مجموعة الامتدادات. نحدد المعرف المرجعي واسم المتجر ونوع المتجر الخاص بالامتداد.

## الخطوة 5: الوصول إلى مجموعة جزء مهام ملحق الويب

```csharp
// قم بالوصول إلى مجموعة جزء مهام ملحق الويب
WebExtensionTaskPaneCollection taskPanes = workbook.Worksheets.WebExtensionTaskPanes;
```

 نقوم بالوصول إلى مجموعة أجزاء مهام Excel Workbook Web Extension باستخدام ملحق`WebExtensionTaskPanes` ممتلكات`Worksheets` هدف.

## الخطوة 6: إضافة جزء مهام جديد

```csharp
// إضافة جزء مهام جديد
int taskPaneIndex = taskPanes.Add();
WebExtensionTaskPane taskPane = taskPanes[taskPaneIndex];
taskPane. IsVisible = true;
taskPane. DockState = "right";
taskPane. WebExtension = extension;
```

نحن نضيف جزء مهام جديدًا إلى مجموعة جزء المهام. قمنا بتعيين رؤية الجزء وحالة الإرساء وامتداد الويب المرتبط به.

## الخطوة 7: احفظ وأغلق المصنف

```csharp
// احفظ وأغلق المصنف
workbook.Save(outDir + "AddWebExtension_Out.xlsx");
Console.WriteLine("AddWebExtension executed successfully.");
```

نحفظ المصنف المعدل في دليل الإخراج المحدد ثم نغلقه.

### نموذج التعليمات البرمجية المصدر لـ Add Web Extension باستخدام Aspose.Cells for .NET 
```csharp
//دليل المصدر
string outDir = RunExamples.Get_OutputDirectory();
Workbook workbook = new Workbook();
WebExtensionCollection extensions = workbook.Worksheets.WebExtensions;
WebExtensionTaskPaneCollection taskPanes = workbook.Worksheets.WebExtensionTaskPanes;
int extensionIndex = extensions.Add();
int taskPaneIndex = taskPanes.Add();
WebExtension extension = extensions[extensionIndex];
extension.Reference.Id = "wa104379955";
extension.Reference.StoreName = "en-US";
extension.Reference.StoreType = WebExtensionStoreType.OMEX;
WebExtensionTaskPane taskPane = taskPanes[taskPaneIndex];
taskPane.IsVisible = true;
taskPane.DockState = "right";
taskPane.WebExtension = extension;
workbook.Save(outDir + "AddWebExtension_Out.xlsx");
Console.WriteLine("AddWebExtension executed successfully.");
```

## خاتمة

تهنئة ! لقد تعلمت الآن كيفية إضافة امتداد ويب باستخدام Aspose.Cells for .NET. جرب التعليمات البرمجية واستكشف الميزات الإضافية لـ Aspose.Cells لتحقيق أقصى استفادة من معالجة ملحقات الويب في مصنفات Excel.

## أسئلة وأجوبة

#### س: ما هو ملحق الويب في مصنف Excel؟

ج: يعد ملحق الويب في مصنف Excel مكونًا يسمح لك بإضافة وظائف إضافية إلى Excel عن طريق دمج تطبيقات الويب. يمكن أن تقدم ميزات تفاعلية ولوحات معلومات مخصصة وتكاملات خارجية والمزيد.

#### س: كيف تضيف امتداد ويب إلى مصنف Excel باستخدام Aspose.Cells؟

 ج: لإضافة امتداد ويب إلى مصنف Excel باستخدام Aspose.Cells ، يمكنك اتباع الخطوات الواردة في دليلنا خطوة بخطوة. استخدم ال`WebExtensionCollection` و`WebExtensionTaskPaneCollection` فئات لإضافة وتكوين امتداد الويب وجزء المهام المرتبط.

#### س: ما هي المعلومات المطلوبة لإضافة امتداد ويب؟

ج: عند إضافة امتداد ويب ، يجب عليك تقديم معرف SKU الملحق واسم المتجر ونوع المتجر. تساعد هذه المعلومات في تحديد الامتداد وتحميله بشكل صحيح.

#### س: هل يمكنني إضافة عدة ملحقات ويب إلى مصنف Excel واحد؟

 ج: نعم ، يمكنك إضافة عدة ملحقات ويب إلى مصنف Excel واحد. استخدم ال`Add` طريقة تجميع ملحقات الويب لإضافة كل امتداد ، ثم إقرانها بأجزاء المهام المقابلة.