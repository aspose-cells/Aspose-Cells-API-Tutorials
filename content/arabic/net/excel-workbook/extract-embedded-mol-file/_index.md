---
title: استخراج ملف Mol المضمن
linktitle: استخراج ملف Mol المضمن
second_title: Aspose.Cells لمرجع .NET API
description: تعرف على كيفية استخراج ملفات MOL المضمنة بسهولة من مصنف Excel باستخدام Aspose.Cells لـ .NET.
type: docs
weight: 90
url: /ar/net/excel-workbook/extract-embedded-mol-file/
---
في هذا البرنامج التعليمي، سنرشدك خطوة بخطوة إلى كيفية استخراج ملف MOL مضمن من مصنف Excel باستخدام مكتبة Aspose.Cells لـ .NET. سوف تتعلم كيفية استعراض أوراق المصنف واستخراج كائنات OLE المقابلة وحفظ ملفات MOL المستخرجة. اتبع الخطوات أدناه لإكمال هذه المهمة بنجاح.

## الخطوة 1: تحديد أدلة المصدر والإخراج
أولاً، نحتاج إلى تحديد مجلدي المصدر والمخرجات في الكود الخاص بنا. تشير هذه الدلائل إلى مكان وجود مصنف Excel المصدر والمكان الذي سيتم فيه حفظ ملفات MOL المستخرجة. هنا هو الكود المقابل:

```csharp
// الدلائل
string SourceDir = RunExamples.Get_SourceDirectory();
string outputDir = RunExamples.Get_OutputDirectory();
```

تأكد من تحديد المسارات المناسبة حسب الحاجة.

## الخطوة 2: تحميل مصنف Excel
الخطوة التالية هي تحميل مصنف Excel الذي يحتوي على كائنات OLE وملفات MOL المضمنة. وهذا هو الكود لتحميل المصنف:

```csharp
Workbook workbook = new Workbook(SourceDir + "EmbeddedMolSample.xlsx");
```

تأكد من تحديد اسم الملف المصدر بشكل صحيح في التعليمات البرمجية.

## الخطوة 3: اجتياز الأوراق واستخراج ملفات MOL
سنقوم الآن باستعراض كل ورقة في المصنف واستخراج كائنات OLE المقابلة، والتي تحتوي على ملفات MOL. هنا هو الكود المقابل:

```csharp
var index = 1;
foreach(Worksheet sheet in workbook.Worksheets)
{
     OleObjectCollection oles = sheet.OleObjects;
     foreach(OleObject ole in oles)
     {
         string fileName = outputDir + "OleObject" + index + ".mol";
         FileStream fs = File.Create(fileName);
         fs.Write(ole.ObjectData, 0, ole.ObjectData.Length);
         fs. Close();
         index++;
     }
}
Console.WriteLine("ExtractEmbeddedMolFile executed successfully.");
```

يتكرر هذا الرمز خلال كل ورقة في المصنف، ويجلب كائنات OLE، ويحفظ ملفات MOL المستخرجة في دليل الإخراج.

### نموذج التعليمات البرمجية المصدر لاستخراج ملف Embedded Mol باستخدام Aspose.Cells لـ .NET 
```csharp
//الدلائل
string SourceDir = RunExamples.Get_SourceDirectory();
string outputDir = RunExamples.Get_OutputDirectory();
Workbook workbook = new Workbook(SourceDir + "EmbeddedMolSample.xlsx");
var index = 1;
foreach (Worksheet sheet in workbook.Worksheets)
{
	OleObjectCollection oles = sheet.OleObjects;
	foreach (OleObject ole in oles)
	{
		string fileName = outputDir + "OleObject" + index + ".mol ";
		FileStream fs = File.Create(fileName);
		fs.Write(ole.ObjectData, 0, ole.ObjectData.Length);
		fs.Close();
		index++;
	}
}
Console.WriteLine("ExtractEmbeddedMolFile executed successfully.");
```

## خاتمة
تهنئة ! لقد تعلمت كيفية استخراج ملف MOL مضمن من مصنف Excel باستخدام Aspose.Cells لـ .NET. يمكنك الآن تطبيق هذه المعرفة لاستخراج ملفات MOL من مصنفات Excel الخاصة بك. لا تتردد في استكشاف مكتبة Aspose.Cells بشكل أكبر والتعرف على ميزاتها القوية الأخرى.

### الأسئلة الشائعة

#### س: ما هو ملف MOL؟
 
ج: ملف MOL هو تنسيق ملف يستخدم لتمثيل الهياكل الكيميائية في الكيمياء الحاسوبية. أنه يحتوي على معلومات حول الذرات والروابط وغيرها من الخصائص الجزيئية.

#### س: هل تعمل هذه الطريقة مع كافة أنواع ملفات Excel؟

ج: نعم، تعمل هذه الطريقة مع جميع أنواع ملفات Excel التي يدعمها Aspose.Cells.

#### س: هل يمكنني استخراج ملفات MOL متعددة في وقت واحد؟

ج: نعم، يمكنك استخراج ملفات MOL متعددة مرة واحدة عن طريق التكرار عبر كائنات OLE الموجودة في كل ورقة في المصنف.