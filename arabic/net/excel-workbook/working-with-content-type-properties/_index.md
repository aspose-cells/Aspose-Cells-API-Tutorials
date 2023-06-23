---
title: العمل مع خصائص نوع المحتوى
linktitle: العمل مع خصائص نوع المحتوى
second_title: Aspose.Cells لمرجع .NET API
description: تعرف على كيفية التعامل مع خصائص نوع المحتوى باستخدام Aspose.Cells for .NET.
type: docs
weight: 180
url: /ar/net/excel-workbook/working-with-content-type-properties/
---
تلعب خصائص نوع المحتوى دورًا حيويًا في إدارة ملفات Excel ومعالجتها باستخدام مكتبة Aspose.Cells لـ .NET. تتيح لك هذه الخصائص تحديد بيانات تعريف إضافية لملفات Excel ، مما يسهل تنظيم البيانات والعثور عليها. في هذا البرنامج التعليمي ، سنأخذك خطوة بخطوة لفهم خصائص نوع المحتوى والعمل معها باستخدام نموذج كود C #.

## المتطلبات الأساسية

قبل أن تبدأ ، تأكد من أن لديك ما يلي:

- Aspose.Cells for .NET مثبتة على جهاز التطوير الخاص بك.
- بيئة تطوير متكاملة (IDE) متوافقة مع C # ، مثل Visual Studio.

## الخطوة الأولى: تهيئة البيئة

قبل أن تبدأ العمل مع خصائص نوع المحتوى ، تأكد من إعداد بيئة التطوير الخاصة بك باستخدام Aspose.Cells for .NET. يمكنك إضافة المرجع إلى مكتبة Aspose.Cells في مشروعك واستيراد مساحة الاسم المطلوبة إلى فصلك الدراسي.

```csharp
using Aspose.Cells;
```

## الخطوة 2: إنشاء مصنف Excel جديد

 أولاً ، سننشئ مصنف Excel جديدًا باستخدام ملف`Workbook`فئة مقدمة من Aspose.Cells. يوضح الكود التالي كيفية إنشاء مصنف Excel جديد وتخزينه في دليل إخراج محدد.

```csharp
// وجهة بشكل مباشر
string outputDir = RunExamples.Get_OutputDirectory();

// قم بإنشاء مصنف Excel جديد
Workbook workbook = new Workbook(FileFormatType.Xlsx);
```

## الخطوة 3: إضافة خصائص نوع المحتوى

 الآن بعد أن أصبح لدينا مصنف Excel الخاص بنا ، يمكننا إضافة خصائص نوع المحتوى باستخدام امتداد`Add` طريقة`ContentTypeProperties` جمع`Workbook` فصل. يتم تمثيل كل خاصية باسم وقيمة. أنت

  يمكنك أيضًا تحديد نوع بيانات الموقع.

```csharp
// أضف خاصية نوع المحتوى الأولى
int index = workbook.ContentTypeProperties.Add("MK31", "Simple Data");
workbook.ContentTypeProperties[index].IsNillable = false;

// أضف خاصية نوع المحتوى الثانية
index = workbook.ContentTypeProperties.Add("MK32", DateTime.Now.ToString("yyyy-MM-dd'T'hh:mm:ss"), "DateTime");
workbook.ContentTypeProperties[index].IsNillable = true;
```

## الخطوة 4: حفظ مصنف Excel

 بعد إضافة خصائص نوع المحتوى ، يمكننا حفظ مصنف Excel مع التغييرات. استخدم ال`Save` طريقة`Workbook` فئة لتحديد دليل الإخراج واسم الملف.

```csharp
// احفظ مصنف Excel
workbook.Save(outputDir + "WorkingWithContentTypeProperties_out.xlsx");
```

### نموذج التعليمات البرمجية المصدر للعمل مع خصائص نوع المحتوى باستخدام Aspose.Cells لـ .NET 
```csharp
//دليل المصدر
string outputDir = RunExamples.Get_OutputDirectory();
Workbook workbook = new Workbook(FileFormatType.Xlsx);
int index = workbook.ContentTypeProperties.Add("MK31", "Simple Data");
workbook.ContentTypeProperties[index].IsNillable = false;
index = workbook.ContentTypeProperties.Add("MK32", DateTime.Now.ToString("yyyy-MM-dd'T'hh:mm:ss"), "DateTime");
workbook.ContentTypeProperties[index].IsNillable = true;
workbook.Save(outputDir + "WorkingWithContentTypeProperties_out.xlsx");
Console.WriteLine("WorkingWithContentTypeProperties executed successfully.");
```

## خاتمة

تهنئة ! لقد تعلمت كيفية التعامل مع خصائص نوع المحتوى باستخدام Aspose.Cells for .NET. يمكنك الآن إضافة بيانات وصفية مخصصة إلى ملفات Excel وإدارتها بشكل أكثر كفاءة.

### أسئلة وأجوبة

#### س: هل خصائص نوع المحتوى متوافقة مع كافة إصدارات Excel؟

ج: نعم ، خصائص نوع المحتوى متوافقة مع ملفات Excel التي تم إنشاؤها في كافة إصدارات Excel.

#### س: هل يمكنني تحرير خصائص نوع المحتوى بعد إضافتها إلى مصنف Excel؟

 ج: نعم ، يمكنك تغيير خصائص نوع المحتوى في أي وقت بالانتقال إلى`ContentTypeProperties` جمع`Workbook` class واستخدام خصائص p و p.

#### س: هل خصائص نوع المحتوى مدعومة عند الحفظ في PDF؟

ج: لا ، خصائص نوع المحتوى غير مدعومة عند الحفظ في PDF. إنها خاصة بملفات Excel.