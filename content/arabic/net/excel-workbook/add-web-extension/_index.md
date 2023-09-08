---
title: إضافة ملحق الويب
linktitle: إضافة ملحق الويب
second_title: Aspose.Cells لمرجع .NET API
description: يمكنك بسهولة إضافة امتداد الويب إلى مصنفات Excel الخاصة بك باستخدام Aspose.Cells for .NET.
type: docs
weight: 40
url: /ar/net/excel-workbook/add-web-extension/
---
في هذا البرنامج التعليمي خطوة بخطوة، سنشرح كود مصدر C# المقدم والذي سيسمح لك بإضافة ملحق ويب باستخدام Aspose.Cells لـ .NET. اتبع الخطوات أدناه لإضافة ملحق ويب إلى مصنف Excel الخاص بك.

## الخطوة 1: تعيين دليل الإخراج

```csharp
// دليل الإخراج
string outDir = RunExamples.Get_OutputDirectory();
```

في هذه الخطوة الأولى، نحدد دليل الإخراج حيث سيتم حفظ مصنف Excel المعدل.

## الخطوة 2: إنشاء مصنف جديد

```csharp
// إنشاء مصنف جديد
Workbook workbook = new Workbook();
```

نحن هنا نقوم بإنشاء مصنف Excel جديد باستخدام ملف`Workbook` فئة من Aspose.Cells.

## الخطوة 3: الوصول إلى مجموعة ملحقات الويب

```csharp
// الوصول إلى مجموعة ملحقات الويب
WebExtensionCollection extensions = workbook.Worksheets.WebExtensions;
```

 نحن نصل إلى مجموعة ملحقات الويب الخاصة بمصنف Excel باستخدام ملف`WebExtensions` ملكية`Worksheets` هدف.

## الخطوة 4: إضافة ملحق ويب جديد

```csharp
// إضافة ملحق ويب جديد
int extensionIndex = extensions.Add();
WebExtension extension = extensions[extensionIndex];
extension.Reference.Id = "wa104379955";
extension.Reference.StoreName = "en-US";
extension.Reference.StoreType = WebExtensionStoreType.OMEX;
```

نقوم بإضافة ملحق ويب جديد إلى مجموعة الملحقات. نحدد المعرف المرجعي واسم المتجر ونوع المتجر للامتداد.

## الخطوة 5: الوصول إلى مجموعة أجزاء مهام ملحق الويب

```csharp
// قم بالوصول إلى مجموعة أجزاء المهام الخاصة بملحق الويب
WebExtensionTaskPaneCollection taskPanes = workbook.Worksheets.WebExtensionTaskPanes;
```

 نحن نصل إلى مجموعة أجزاء المهام الخاصة بـ Excel Workbook Web Extension باستخدام ملف`WebExtensionTaskPanes` ملكية`Worksheets` هدف.

## الخطوة 6: إضافة جزء مهام جديد

```csharp
// إضافة جزء مهام جديد
int taskPaneIndex = taskPanes.Add();
WebExtensionTaskPane taskPane = taskPanes[taskPaneIndex];
taskPane. IsVisible = true;
taskPane. DockState = "right";
taskPane. WebExtension = extension;
```

نقوم بإضافة جزء مهام جديد إلى مجموعة أجزاء المهام. لقد قمنا بتعيين رؤية الجزء وحالة الإرساء الخاصة به وامتداد الويب المرتبط به.

## الخطوة 7: احفظ المصنف وأغلقه

```csharp
// احفظ المصنف وأغلقه
workbook.Save(outDir + "AddWebExtension_Out.xlsx");
Console.WriteLine("AddWebExtension executed successfully.");
```

نقوم بحفظ المصنف المعدل في دليل الإخراج المحدد ثم نغلقه.

### نموذج التعليمات البرمجية المصدر لإضافة ملحق ويب باستخدام Aspose.Cells لـ .NET 
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

تهنئة ! لقد تعلمت الآن كيفية إضافة ملحق ويب باستخدام Aspose.Cells لـ .NET. قم بتجربة التعليمات البرمجية واستكشف الميزات الإضافية لـ Aspose.Cells لتحقيق أقصى استفادة من معالجة ملحقات الويب في مصنفات Excel الخاصة بك.

## الأسئلة الشائعة

#### س: ما هو ملحق الويب الموجود في مصنف Excel؟

ج: يعد ملحق الويب الموجود في مصنف Excel مكونًا يسمح لك بإضافة وظائف إضافية إلى Excel من خلال دمج تطبيقات الويب. يمكنه تقديم ميزات تفاعلية ولوحات معلومات مخصصة وعمليات تكامل خارجية والمزيد.

#### س: كيفية إضافة ملحق الويب إلى مصنف Excel باستخدام Aspose.Cells؟

 ج: لإضافة ملحق ويب إلى مصنف Excel باستخدام Aspose.Cells، يمكنك اتباع الخطوات الواردة في دليلنا خطوة بخطوة. استخدم ال`WebExtensionCollection` و`WebExtensionTaskPaneCollection` فئات لإضافة وتكوين ملحق الويب وجزء المهام المرتبط به.

#### س: ما هي المعلومات المطلوبة لإضافة ملحق ويب؟

ج: عند إضافة ملحق ويب، يجب عليك تقديم معرف SKU للملحق واسم المتجر ونوع المتجر. تساعد هذه المعلومات في تحديد الامتداد وتحميله بشكل صحيح.

#### س: هل يمكنني إضافة ملحقات ويب متعددة إلى مصنف Excel واحد؟

 ج: نعم، يمكنك إضافة ملحقات ويب متعددة إلى مصنف Excel واحد. استخدم ال`Add` طريقة مجموعة ملحقات الويب لإضافة كل ملحق، ثم ربطها بأجزاء المهام المقابلة.