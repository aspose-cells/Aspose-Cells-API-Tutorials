---
title: دعم توقيع Xades
linktitle: دعم توقيع Xades
second_title: Aspose.Cells لمرجع .NET API
description: تعرف على كيفية إضافة توقيع Xades إلى ملف Excel باستخدام Aspose.Cells لـ .NET.
type: docs
weight: 190
url: /ar/net/excel-workbook/xades-signature-support/
---
في هذه المقالة، سنأخذك خطوة بخطوة لشرح الكود المصدري لـ C# أدناه، والذي يتعلق بدعم توقيع Xades باستخدام مكتبة Aspose.Cells لـ .NET. سوف تكتشف كيفية استخدام هذه المكتبة لإضافة توقيع Xades الرقمي إلى ملف Excel. سنزودك أيضًا بنظرة عامة على عملية التوقيع وتنفيذها. اتبع الخطوات أدناه للحصول على نتائج حاسمة.

## الخطوة 1: تحديد أدلة المصدر والإخراج
للبدء، نحتاج إلى تحديد مجلدات المصدر والمخرجات في الكود الخاص بنا. تشير هذه الدلائل إلى مكان وجود الملفات المصدر والمكان الذي سيتم فيه حفظ ملف الإخراج. هنا هو الكود المقابل:

```csharp
// دليل المصدر
string sourceDir = RunExamples.Get_SourceDirectory();
// دليل الإخراج
string outputDir = RunExamples.Get_OutputDirectory();
```

تأكد من تعديل مسارات الدليل حسب الحاجة.

## الخطوة 2: تحميل مصنف Excel
الخطوة التالية هي تحميل مصنف Excel الذي نريد إضافة توقيع Xades الرقمي إليه. وهذا هو الكود لتحميل المصنف:

```csharp
Workbook workbook = new Workbook(sourceDir + "sourceFile.xlsx");
```

تأكد من تحديد اسم الملف المصدر بشكل صحيح في التعليمات البرمجية.

## الخطوة 3: تكوين التوقيع الرقمي
سنقوم الآن بتكوين توقيع Xades الرقمي من خلال توفير المعلومات الضرورية. يجب علينا تحديد ملف PFX الذي يحتوي على الشهادة الرقمية، بالإضافة إلى كلمة المرور المرتبطة بها. هنا هو الكود المقابل:

```csharp
string password = "pfxPassword";
string pfx = "pfxFile";
DigitalSignature signature = new DigitalSignature(File.ReadAllBytes(pfx), password, "testXAdES", DateTime.Now);
signature.XAdESType = XAdESType.XAdES;
```

تأكد من استبدال "pfxPassword" بكلمة المرور الفعلية و"pfxFile" بالمسار إلى ملف PFX.

## الخطوة 4: إضافة التوقيع الرقمي
الآن بعد أن قمنا بتكوين التوقيع الرقمي، يمكننا إضافته إلى مصنف Excel. هنا هو الكود المقابل:

```csharp
DigitalSignatureCollection dsCollection = new DigitalSignatureCollection();
dsCollection.Add(signature);
workbook.SetDigitalSignature(dsCollection);
```

تضيف هذه الخطوة توقيع Xades الرقمي إلى مصنف Excel.

## الخطوة 5: حفظ المصنف بالتوقيع
أخيرًا، نقوم بحفظ مصنف Excel مع إضافة التوقيع الرقمي. هنا هو الكود المقابل:

```csharp
workbook.Save(outputDir + "XAdESSignatureSupport_out.xlsx");
```

تأكد من تعديل اسم ملف الإخراج وفقًا لاحتياجاتك.

### نموذج التعليمات البرمجية المصدر لدعم توقيع Xades باستخدام Aspose.Cells لـ .NET 
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
تهنئة ! لقد تعلمت كيفية استخدام مكتبة Aspose.Cells لـ .NET لإضافة توقيع Xades الرقمي إلى ملف Excel. باتباع الخطوات الواردة في هذه المقالة، ستتمكن من تنفيذ هذه الوظيفة في مشاريعك الخاصة. لا تتردد في تجربة المزيد مع المكتبة واكتشاف الميزات القوية الأخرى التي تقدمها.

### الأسئلة الشائعة

#### س: ما هو Xades؟

ج: Xades هو معيار توقيع إلكتروني متقدم يستخدم لضمان سلامة وصحة المستندات الرقمية.

#### س: هل يمكنني استخدام أنواع أخرى من التوقيعات الرقمية مع Aspose.Cells؟

ج: نعم، يدعم Aspose.Cells أيضًا أنواعًا أخرى من التوقيعات الرقمية، مثل توقيعات XMLDSig وتوقيعات PKCS#7.

#### س: هل يمكنني تطبيق التوقيع على أنواع ملفات أخرى غير ملفات Excel؟
 
ج: نعم، يسمح Aspose.Cells أيضًا بتطبيق التوقيعات الرقمية على أنواع الملفات المدعومة الأخرى مثل ملفات Word وPDF وPowerPoint.