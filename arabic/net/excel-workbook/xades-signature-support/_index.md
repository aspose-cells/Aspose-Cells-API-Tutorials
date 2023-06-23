---
title: دعم Xades المميز
linktitle: دعم Xades المميز
second_title: Aspose.Cells لمرجع .NET API
description: تعرف على كيفية إضافة توقيع Xades إلى ملف Excel باستخدام Aspose.Cells for .NET.
type: docs
weight: 190
url: /ar/net/excel-workbook/xades-signature-support/
---
في هذه المقالة ، سوف نأخذك خطوة بخطوة لشرح كود المصدر C # أدناه ، والذي يتعلق بدعم توقيع Xades باستخدام Aspose.Cells library for .NET. سوف تتعلم كيفية استخدام هذه المكتبة لإضافة توقيع Xades الرقمي إلى ملف Excel. سنزودك أيضًا بلمحة عامة عن عملية التوقيع وتنفيذها. اتبع الخطوات أدناه للحصول على نتائج قاطعة.

## الخطوة 1: تحديد أدلة المصدر والمخرجات
للبدء ، نحتاج إلى تحديد مجلدات المصدر والمخرجات في التعليمات البرمجية الخاصة بنا. تشير هذه الدلائل إلى مكان وجود ملفات المصدر وأين سيتم حفظ ملف الإخراج. هذا هو الكود المقابل:

```csharp
// دليل المصدر
string sourceDir = RunExamples.Get_SourceDirectory();
// دليل الإخراج
string outputDir = RunExamples.Get_OutputDirectory();
```

تأكد من تكييف مسارات الدليل حسب الحاجة.

## الخطوة 2: تحميل مصنف Excel
الخطوة التالية هي تحميل مصنف Excel الذي نريد إضافة توقيع Xades الرقمي عليه. هذا هو الكود لتحميل المصنف:

```csharp
Workbook workbook = new Workbook(sourceDir + "sourceFile.xlsx");
```

تأكد من تحديد اسم الملف المصدر بشكل صحيح في التعليمات البرمجية.

## الخطوة 3: تكوين التوقيع الرقمي
سنقوم الآن بتهيئة توقيع Xades الرقمي من خلال توفير المعلومات اللازمة. يجب أن نحدد ملف PFX الذي يحتوي على الشهادة الرقمية ، وكذلك كلمة المرور المرتبطة. هذا هو الكود المقابل:

```csharp
string password = "pfxPassword";
string pfx = "pfxFile";
DigitalSignature signature = new DigitalSignature(File.ReadAllBytes(pfx), password, "testXAdES", DateTime.Now);
signature.XAdESType = XAdESType.XAdES;
```

تأكد من استبدال "pfxPassword" بكلمة المرور الفعلية و "pfxFile" بالمسار إلى ملف PFX.

## الخطوة 4: إضافة التوقيع الرقمي
الآن بعد أن قمنا بتكوين التوقيع الرقمي ، يمكننا إضافته إلى مصنف Excel. هذا هو الكود المقابل:

```csharp
DigitalSignatureCollection dsCollection = new DigitalSignatureCollection();
dsCollection.Add(signature);
workbook.SetDigitalSignature(dsCollection);
```

تضيف هذه الخطوة توقيع Xades الرقمي إلى مصنف Excel.

## الخطوة 5: حفظ المصنف بالتوقيع
أخيرًا ، نحفظ مصنف Excel مع إضافة التوقيع الرقمي. هذا هو الكود المقابل:

```csharp
workbook.Save(outputDir + "XAdESSignatureSupport_out.xlsx");
```

تأكد من تعديل اسم ملف الإخراج وفقًا لاحتياجاتك.

### نموذج التعليمات البرمجية المصدر لـ Xades Signature Support باستخدام Aspose.Cells for .NET 
```csharp
//دليل المصدر
string sourceDir = RunExamples.Get_SourceDirectory();
//دليل الإخراج
string outputDir = RunExamples.Get_OutputDirectory();
Workbook workbook = new Workbook(sourceDir + "sourceFile.xlsx");
string password = "pfxPassword";
string pfx = "pfxFile";
DigitalSignature signature = new DigitalSignature(File.ReadAllBytes(pfx), password, "testXAdES", DateTime.Now);
signature.XAdESType = XAdESType.XAdES;
DigitalSignatureCollection dsCollection = new DigitalSignatureCollection();
dsCollection.Add(signature);
workbook.SetDigitalSignature(dsCollection);
workbook.Save(outputDir + "XAdESSignatureSupport_out.xlsx");
Console.WriteLine("XAdESSignatureSupport executed successfully.");
```

## خاتمة
تهنئة ! لقد تعلمت كيفية استخدام مكتبة Aspose.Cells لـ .NET لإضافة توقيع Xades الرقمي إلى ملف Excel. باتباع الخطوات الواردة في هذه المقالة ، ستتمكن من تنفيذ هذه الوظيفة في مشاريعك الخاصة. لا تتردد في تجربة المزيد مع المكتبة واكتشاف الميزات القوية الأخرى التي تقدمها.

### أسئلة وأجوبة

#### س: ما هو Xades؟

ج: Xades هو معيار توقيع إلكتروني متقدم يستخدم لضمان سلامة وأصالة المستندات الرقمية.

#### س: هل يمكنني استخدام أنواع أخرى من التوقيعات الرقمية مع Aspose.Cells؟

ج: نعم ، تدعم Aspose.Cells أيضًا أنواعًا أخرى من التوقيعات الرقمية ، مثل توقيعات XMLDSig وتوقيعات PKCS # 7.

#### س: هل يمكنني تطبيق توقيع على أنواع ملفات أخرى غير ملفات Excel؟
 
ج: نعم ، يسمح Aspose.Cells أيضًا بتطبيق التوقيعات الرقمية على أنواع الملفات المدعومة الأخرى مثل ملفات Word و PDF و PowerPoint.