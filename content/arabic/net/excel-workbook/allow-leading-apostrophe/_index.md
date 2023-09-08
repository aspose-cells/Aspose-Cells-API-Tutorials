---
title: السماح بالفاصلة العليا البادئة
linktitle: السماح بالفاصلة العليا البادئة
second_title: Aspose.Cells لمرجع .NET API
description: السماح بالفاصلة العليا البادئة في مصنفات Excel باستخدام Aspose.Cells لـ .NET.
type: docs
weight: 60
url: /ar/net/excel-workbook/allow-leading-apostrophe/
---
في هذا البرنامج التعليمي خطوة بخطوة، سنشرح التعليمات البرمجية المصدر لـ C# المتوفرة والتي ستسمح لك بالسماح باستخدام فاصلة عليا بادئة في مصنف Excel باستخدام Aspose.Cells لـ .NET. اتبع الخطوات أدناه لتنفيذ هذه العملية.

## الخطوة 1: قم بتعيين أدلة المصدر والإخراج

```csharp
// دليل المصدر
string sourceDir = RunExamples.Get_SourceDirectory();
// دليل الإخراج
string outputDir = RunExamples.Get_OutputDirectory();
```

في هذه الخطوة الأولى، نقوم بتحديد مجلدات المصدر والمخرجات لملفات Excel.

## الخطوة 2: إنشاء كائن WorkbookDesigner

```csharp
// إنشاء مثيل لكائن WorkbookDesigner
WorkbookDesigner designer = new WorkbookDesigner();
```

 نقوم بإنشاء مثيل لـ`WorkbookDesigner` فئة من Aspose.Cells.

## الخطوة 3: تحميل مصنف Excel

```csharp
// قم بتحميل مصنف Excel
Workbook workbook = new Workbook(sourceDir + "AllowLeadingApostropheSample.xlsx");
workbook.Settings.QuotePrefixToStyle = false;
designer.Workbook = workbook;
```

نقوم بتحميل مصنف Excel من الملف المحدد ونقوم بتعطيل التحويل التلقائي للفواصل العليا الأولية إلى نمط النص.

## الخطوة 4: تعيين مصدر البيانات

```csharp
// تحديد مصدر البيانات لمصنف المصمم
List<DataObject> list = new List<DataObject>
{
new DataObject
{
Id=1,
Name = "demo"
},
new DataObject
{
ID=2,
Name = "'demo"
}
};
designer.SetDataSource("sampleData", list);
```

 نحدد قائمة بكائنات البيانات ونستخدمها`SetDataSource` طريقة لتعيين مصدر البيانات لمصنف المصمم.

## الخطوة 5: معالجة العلامات الذكية

```csharp
// معالجة العلامات الذكية
designer. Process();
```

 نحن نستخدم ال`Process` طريقة لمعالجة العلامات الذكية في مصنف المصمم.

## الخطوة 6: احفظ مصنف Excel المعدل

```csharp
// احفظ مصنف Excel المعدل
designer.Workbook.Save(outputDir + "AllowLeadingApostropheSample_out.xlsx");
```

نقوم بحفظ مصنف Excel المعدل مع التغييرات التي تم إجراؤها.

### نموذج التعليمات البرمجية المصدر للسماح بالفاصلة العليا باستخدام Aspose.Cells لـ .NET 
```csharp
//دليل المصدر
string sourceDir = RunExamples.Get_SourceDirectory();
string outputDir = RunExamples.Get_OutputDirectory();
// إنشاء مثيل لكائن WorkbookDesigner
WorkbookDesigner designer = new WorkbookDesigner();
Workbook workbook = new Workbook(sourceDir + "AllowLeadingApostropheSample.xlsx");
workbook.Settings.QuotePrefixToStyle = false;
// افتح جدول بيانات المصمم الذي يحتوي على علامات ذكية
designer.Workbook = workbook;
List<DataObject> list = new List<DataObject>
{
	new DataObject
	{
		 Id =1,
		 Name = "demo"
	},
	new DataObject
	{
		Id=2,
		Name = "'demo"
	}
};
// قم بتعيين مصدر البيانات لجدول بيانات المصمم
designer.SetDataSource("sampleData", list);
// معالجة العلامات الذكية
designer.Process();
designer.Workbook.Save(outputDir + "AllowLeadingApostropheSample_out.xlsx");
Console.WriteLine("AllowLeadingApostrophe executed successfully.");
```

## خاتمة

تهنئة ! لقد تعلمت كيفية السماح باستخدام الفاصلة العليا البادئة في مصنف Excel باستخدام Aspose.Cells لـ .NET. قم بتجربة البيانات الخاصة بك لتخصيص مصنفات Excel الخاصة بك بشكل أكبر.

### الأسئلة الشائعة

#### س: ما هو إذن الفاصلة العليا في مصنف Excel؟

ج: يسمح السماح بالفاصلة العليا الأولية في مصنف Excel بعرض البيانات التي تبدأ بفاصلة عليا بشكل صحيح دون تحويلها إلى نمط نص. يكون هذا مفيدًا عندما تريد الاحتفاظ بالفاصلة العليا كجزء من البيانات.

#### س: لماذا أحتاج إلى إيقاف التحويل التلقائي للفواصل العليا الأولية؟

ج: من خلال تعطيل التحويل التلقائي لعلامات الاقتباس البادئة، يمكنك الحفاظ على استخدامها كما هو في بياناتك. يؤدي هذا إلى تجنب أي تعديل غير مقصود للبيانات أثناء فتح مصنف Excel أو معالجته.

#### س: كيفية تعيين مصدر البيانات في مصنف المصمم؟

 ج: لتعيين مصدر البيانات في مصنف المصمم، يمكنك استخدام`SetDataSource` طريقة تحدد اسم مصدر البيانات وقائمة كائنات البيانات المقابلة.

#### س: هل يؤثر السماح بالفاصلة العليا البادئة على البيانات الأخرى في مصنف Excel؟

ج: لا، فالسماح بالفاصلة العليا البادئة يؤثر فقط على البيانات التي تبدأ بفاصلة عليا. تظل البيانات الأخرى في مصنف Excel دون تغيير.

#### س: هل يمكنني استخدام هذه الميزة مع تنسيقات ملفات Excel الأخرى؟

ج: نعم، يمكنك استخدام هذه الميزة مع تنسيقات ملفات Excel الأخرى التي يدعمها Aspose.Cells، مثل .xls و.xlsm وما إلى ذلك.