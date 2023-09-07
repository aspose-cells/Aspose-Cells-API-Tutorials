---
title: السماح بادئة الفاصلة العليا
linktitle: السماح بادئة الفاصلة العليا
second_title: Aspose.Cells لمرجع .NET API
description: السماح بعلامة الفاصلة العليا في مصنفات Excel باستخدام Aspose.Cells for .NET.
type: docs
weight: 60
url: /ar/net/excel-workbook/allow-leading-apostrophe/
---
في هذا البرنامج التعليمي خطوة بخطوة ، سنشرح الكود المصدري C # الذي سيتيح لك السماح باستخدام فاصلة عليا في مصنف Excel باستخدام Aspose.Cells for .NET. اتبع الخطوات أدناه لإجراء هذه العملية.

## الخطوة 1: تعيين أدلة المصدر والمخرجات

```csharp
// دليل المصدر
string sourceDir = RunExamples.Get_SourceDirectory();
// دليل الإخراج
string outputDir = RunExamples.Get_OutputDirectory();
```

في هذه الخطوة الأولى ، نحدد مجلدات المصدر والمخرجات لملفات Excel.

## الخطوة 2: إنشاء كائن WorkbookDesigner

```csharp
// إنشاء كائن WorkbookDesigner
WorkbookDesigner designer = new WorkbookDesigner();
```

 نقوم بإنشاء مثيل لـ`WorkbookDesigner` فئة من Aspose.Cells.

## الخطوة 3: تحميل مصنف Excel

```csharp
//قم بتحميل مصنف Excel
Workbook workbook = new Workbook(sourceDir + "AllowLeadingApostropheSample.xlsx");
workbook.Settings.QuotePrefixToStyle = false;
designer.Workbook = workbook;
```

نقوم بتحميل مصنف Excel من الملف المحدد وتعطيل التحويل التلقائي للفواصل العليا الأولية إلى نمط النص.

## الخطوة 4: تعيين مصدر البيانات

```csharp
// حدد مصدر البيانات لمصنف المصمم
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

 نحدد قائمة كائنات البيانات ونستخدم الامتداد`SetDataSource` طريقة لتعيين مصدر البيانات لمصنف المصمم.

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

نقوم بحفظ مصنف Excel المعدل بالتغييرات التي تم إجراؤها.

### عينة من التعليمات البرمجية المصدر للسماح بابتداء الفاصلة العليا باستخدام Aspose.Cells لـ .NET 
```csharp
//دليل المصدر
string sourceDir = RunExamples.Get_SourceDirectory();
string outputDir = RunExamples.Get_OutputDirectory();
// إنشاء كائن WorkbookDesigner
WorkbookDesigner designer = new WorkbookDesigner();
Workbook workbook = new Workbook(sourceDir + "AllowLeadingApostropheSample.xlsx");
workbook.Settings.QuotePrefixToStyle = false;
// افتح جدول بيانات مصمم يحتوي على علامات ذكية
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

تهنئة ! لقد تعلمت كيفية السماح باستخدام فاصلة عليا في مصنف Excel باستخدام Aspose.Cells لـ .NET. جرب بياناتك الخاصة لتخصيص مصنفات Excel بشكل أكبر.

### أسئلة وأجوبة

#### س: ما المقصود بإذن الفاصلة العليا في مصنف Excel؟

ج: يسمح السماح بالفاصلة العليا الأولية في مصنف Excel بعرض البيانات التي تبدأ بعلامة اقتباس أحادية ليتم عرضها بشكل صحيح دون تحويلها إلى نمط نص. يكون هذا مفيدًا عندما تريد الاحتفاظ بعلامة اقتباس أحادية كجزء من البيانات.

#### س: لماذا أحتاج إلى إيقاف التحويل التلقائي للفواصل العليا؟

ج: من خلال تعطيل التحويل التلقائي للاقتباسات البادئة ، يمكنك الحفاظ على استخدامها كما هو في بياناتك. يؤدي ذلك إلى تجنب أي تعديل غير مقصود للبيانات أثناء فتح مصنف Excel أو معالجته.

#### س: كيفية تعيين مصدر البيانات في مصنف المصمم؟

 ج: لتعيين مصدر البيانات في مصنف المصمم ، يمكنك استخدام ملف`SetDataSource` طريقة تحدد اسم مصدر البيانات وقائمة كائنات البيانات المقابلة.

#### س: هل يؤثر السماح بعلامة اقتباس أحادية أولى على البيانات الأخرى في مصنف Excel؟

ج: لا ، السماح للفاصلة العليا في البداية يؤثر فقط على البيانات التي تبدأ بعلامة اقتباس أحادية. تبقى البيانات الأخرى في مصنف Excel دون تغيير.

#### س: هل يمكنني استخدام هذه الميزة مع تنسيقات ملفات Excel الأخرى؟

ج: نعم ، يمكنك استخدام هذه الميزة مع تنسيقات ملفات Excel الأخرى التي تدعمها Aspose.Cells ، مثل .xls ، .xlsm ، إلخ.