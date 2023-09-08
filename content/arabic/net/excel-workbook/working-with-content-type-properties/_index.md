---
title: العمل مع خصائص نوع المحتوى
linktitle: العمل مع خصائص نوع المحتوى
second_title: Aspose.Cells لمرجع .NET API
description: تعرف على كيفية التعامل مع خصائص نوع المحتوى باستخدام Aspose.Cells لـ .NET.
type: docs
weight: 180
url: /ar/net/excel-workbook/working-with-content-type-properties/
---
تلعب خصائص نوع المحتوى دورًا حيويًا في إدارة ملفات Excel ومعالجتها باستخدام مكتبة Aspose.Cells لـ .NET. تتيح لك هذه الخصائص تحديد بيانات التعريف الإضافية لملفات Excel، مما يسهل تنظيم البيانات والعثور عليها. في هذا البرنامج التعليمي، سنأخذك خطوة بخطوة لفهم خصائص نوع المحتوى والتعامل معها باستخدام نموذج التعليمات البرمجية لـ C#.

## المتطلبات الأساسية

قبل أن تبدأ، تأكد من أن لديك ما يلي:

- تم تثبيت Aspose.Cells for .NET على جهاز التطوير الخاص بك.
- بيئة تطوير متكاملة (IDE) متوافقة مع لغة C#، مثل Visual Studio.

## الخطوة 1: تهيئة البيئة

قبل البدء في العمل مع خصائص نوع المحتوى، تأكد من أنك قمت بإعداد بيئة التطوير الخاصة بك باستخدام Aspose.Cells لـ .NET. يمكنك إضافة المرجع إلى مكتبة Aspose.Cells في مشروعك واستيراد مساحة الاسم المطلوبة إلى الفصل الدراسي الخاص بك.

```csharp
using Aspose.Cells;
```

## الخطوة 2: إنشاء مصنف Excel جديد

 أولاً، سنقوم بإنشاء مصنف Excel جديد باستخدام الملف`Workbook`الفئة المقدمة من Aspose.Cells. يوضح التعليمة البرمجية التالية كيفية إنشاء مصنف Excel جديد وتخزينه في دليل إخراج محدد.

```csharp
// وجهة بشكل مباشر
string outputDir = RunExamples.Get_OutputDirectory();

// إنشاء مصنف Excel جديد
Workbook workbook = new Workbook(FileFormatType.Xlsx);
```

## الخطوة 3: إضافة خصائص نوع المحتوى

 الآن بعد أن أصبح لدينا مصنف Excel، يمكننا إضافة خصائص نوع المحتوى باستخدام الملف`Add` طريقة`ContentTypeProperties` جمع من`Workbook` فصل. يتم تمثيل كل خاصية باسم وقيمة. أنت

  يمكنك أيضًا تحديد نوع بيانات الخاصية.

```csharp
// أضف خاصية نوع المحتوى الأول
int index = workbook.ContentTypeProperties.Add("MK31", "Simple Data");
workbook.ContentTypeProperties[index].IsNillable = false;

// أضف خاصية نوع المحتوى الثاني
index = workbook.ContentTypeProperties.Add("MK32", DateTime.Now.ToString("yyyy-MM-dd'T'hh:mm:ss"), "DateTime");
workbook.ContentTypeProperties[index].IsNillable = true;
```

## الخطوة 4: حفظ مصنف Excel

 بعد إضافة خصائص نوع المحتوى، يمكننا حفظ مصنف Excel بالتغييرات. استخدم ال`Save` طريقة`Workbook` فئة لتحديد دليل الإخراج واسم الملف.

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

تهنئة ! لقد تعلمت كيفية التعامل مع خصائص نوع المحتوى باستخدام Aspose.Cells لـ .NET. يمكنك الآن إضافة بيانات تعريف مخصصة إلى ملفات Excel وإدارتها بشكل أكثر كفاءة.

### الأسئلة الشائعة

#### س: هل خصائص نوع المحتوى متوافقة مع كافة إصدارات Excel؟

ج: نعم، تتوافق خصائص نوع المحتوى مع ملفات Excel التي تم إنشاؤها في كافة إصدارات Excel.

#### س: هل يمكنني تحرير خصائص نوع المحتوى بعد إضافتها إلى مصنف Excel؟

 ج: نعم، يمكنك تغيير خصائص نوع المحتوى في أي وقت عن طريق الذهاب إلى`ContentTypeProperties` جمع من`Workbook` فئة واستخدام الخصائص المناسبة للطرق و p.

#### س: هل يتم دعم خصائص نوع المحتوى عند الحفظ إلى PDF؟

ج: لا، خصائص نوع المحتوى غير مدعومة عند الحفظ بصيغة PDF. وهي خاصة بملفات Excel.