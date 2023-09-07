---
title: استخراج ملف Mol المضمّن
linktitle: استخراج ملف Mol المضمّن
second_title: Aspose.Cells لمرجع .NET API
description: تعرف على كيفية استخراج ملفات MOL المضمنة بسهولة من مصنف Excel باستخدام Aspose.Cells for .NET.
type: docs
weight: 90
url: /ar/net/excel-workbook/extract-embedded-mol-file/
---
في هذا البرنامج التعليمي ، سنرشدك خطوة بخطوة حول كيفية استخراج ملف MOL مضمن من مصنف Excel باستخدام مكتبة Aspose.Cells لـ .NET. سوف تتعلم كيفية استعراض أوراق المصنفات ، واستخراج كائنات OLE المقابلة وحفظ ملفات MOL المستخرجة. اتبع الخطوات أدناه لإكمال هذه المهمة بنجاح.

## الخطوة 1: تحديد أدلة المصدر والمخرجات
أولاً ، نحتاج إلى تحديد مجلدات المصدر والمخرجات في التعليمات البرمجية الخاصة بنا. تشير هذه الدلائل إلى مكان وجود مصنف Excel المصدر ومكان حفظ ملفات MOL المستخرجة. هذا هو الكود المقابل:

```csharp
// الدلائل
string SourceDir = RunExamples.Get_SourceDirectory();
string outputDir = RunExamples.Get_OutputDirectory();
```

تأكد من تحديد المسارات المناسبة حسب الحاجة.

## الخطوة 2: تحميل مصنف Excel
الخطوة التالية هي تحميل مصنف Excel الذي يحتوي على كائنات OLE المضمنة وملفات MOL. هذا هو الكود لتحميل المصنف:

```csharp
Workbook workbook = new Workbook(SourceDir + "EmbeddedMolSample.xlsx");
```

تأكد من تحديد اسم الملف المصدر بشكل صحيح في التعليمات البرمجية.

## الخطوة 3: اجتياز الأوراق واستخراج ملفات MOL
سنقوم الآن بالمرور عبر كل ورقة في المصنف واستخراج كائنات OLE المقابلة ، والتي تحتوي على ملفات MOL. هذا هو الكود المقابل:

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

يتنقل هذا الرمز عبر كل ورقة في المصنف ، ويجلب كائنات OLE ، ويحفظ ملفات MOL المستخرجة في دليل الإخراج.

### نموذج التعليمات البرمجية المصدر لاستخراج ملف Mol المضمّن باستخدام Aspose.Cells لـ .NET 
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
تهنئة ! لقد تعلمت كيفية استخراج ملف MOL مضمن من مصنف Excel باستخدام Aspose.Cells for .NET. يمكنك الآن تطبيق هذه المعرفة لاستخراج ملفات MOL من مصنفات Excel الخاصة بك. لا تتردد في استكشاف مكتبة Aspose.Cells بشكل أكبر والتعرف على ميزاتها القوية الأخرى.

### أسئلة وأجوبة

#### س: ما هو ملف MOL؟
 
ج: ملف MOL هو تنسيق ملف يستخدم لتمثيل الهياكل الكيميائية في الكيمياء الحسابية. يحتوي على معلومات حول الذرات والروابط والخصائص الجزيئية الأخرى.

#### س: هل تعمل هذه الطريقة مع جميع أنواع ملفات Excel؟

ج: نعم ، تعمل هذه الطريقة مع جميع أنواع ملفات Excel التي يدعمها Aspose.Cells.

#### س: هل يمكنني استخراج عدة ملفات MOL مرة واحدة؟

ج: نعم ، يمكنك استخراج عدة ملفات MOL مرة واحدة عن طريق التكرار خلال كائنات OLE في كل ورقة في المصنف.