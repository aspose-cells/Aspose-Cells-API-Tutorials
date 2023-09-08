---
title: إضافة التوقيع الرقمي إلى ملف Excel الموقع بالفعل
linktitle: إضافة التوقيع الرقمي إلى ملف Excel الموقع بالفعل
second_title: Aspose.Cells لمرجع .NET API
description: يمكنك بسهولة إضافة التوقيعات الرقمية إلى ملفات Excel الموجودة باستخدام Aspose.Cells لـ .NET.
type: docs
weight: 30
url: /ar/net/excel-workbook/add-digital-signature-to-an-already-signed-excel-file/
---
في هذا الدليل التفصيلي، سنشرح كود مصدر C# المقدم والذي سيسمح لك بإضافة توقيع رقمي إلى ملف Excel موقّع بالفعل باستخدام Aspose.Cells for .NET. اتبع الخطوات أدناه لإضافة توقيع رقمي جديد إلى ملف Excel موجود.

## الخطوة 1: قم بتعيين أدلة المصدر والإخراج

```csharp
// دليل المصدر
string sourceDir = RunExamples.Get_SourceDirectory();

// دليل الإخراج
string outputDir = RunExamples.Get_OutputDirectory();
```

في هذه الخطوة الأولى، نحدد دليل المصدر والمخرج الذي سيتم استخدامه لتحميل ملف Excel الموجود وحفظ الملف بالتوقيع الرقمي الجديد.

## الخطوة 2: تحميل ملف Excel الموجود

```csharp
// قم بتحميل مصنف Excel الموقع بالفعل
Aspose.Cells.Workbook workbook = new Aspose.Cells.Workbook(sourceDir + "sampleDigitallySignedByCells.xlsx");
```

 نقوم هنا بتحميل ملف Excel الموقع بالفعل باستخدام ملف`Workbook` فئة Aspose.Cells.

## الخطوة 3: إنشاء مجموعة التوقيعات الرقمية

```csharp
// إنشاء مجموعة التوقيعات الرقمية
Aspose.Cells.DigitalSignatures.DigitalSignatureCollection dsCollection = new Aspose.Cells.DigitalSignatures.DigitalSignatureCollection();
```

 نقوم بإنشاء مجموعة جديدة من التوقيعات الرقمية باستخدام`DigitalSignatureCollection` فصل.

## الخطوة 4: إنشاء شهادة جديدة

```csharp
// إنشاء شهادة جديدة
System.Security.Cryptography.X509Certificates.X509Certificate2 certificate = new System.Security.Cryptography.X509Certificates.X509Certificate2(certFileName, password);
```

نقوم هنا بإنشاء شهادة جديدة من الملف وكلمة المرور المقدمين.

## الخطوة 5: إضافة توقيع رقمي جديد إلى المجموعة

```csharp
// إنشاء توقيع رقمي جديد
Aspose.Cells.DigitalSignatures.DigitalSignature signature = new Aspose.Cells.DigitalSignatures.DigitalSignature(certificate, "Aspose.Cells added a new digital signature to the already signed workbook.", DateTime.Now);

// أضف التوقيع الرقمي إلى المجموعة
dsCollection.Add(signature);
```

 نقوم بإنشاء توقيع رقمي جديد باستخدام`DigitalSignature` فئة وإضافته إلى مجموعة التوقيعات الرقمية.

## الخطوة 6: أضف مجموعة التوقيعات الرقمية إلى المصنف

```csharp
//أضف مجموعة التوقيعات الرقمية إلى المصنف
workbook.AddDigitalSignature(dsCollection);
```

 نضيف مجموعة التوقيعات الرقمية إلى مصنف Excel الموجود باستخدام`AddDigitalSignature()` طريقة.

## الخطوة 7: احفظ المصنف وأغلقه

```csharp
// احفظ المصنف وأغلقه
workbook.Save(outputDir + "outputDigitallySignedByCells.xlsx");
workbook.Dispose();
```

نقوم بحفظ المصنف بالتوقيع الرقمي الجديد في دليل الإخراج المحدد، ثم نغلقه ونطلق الموارد المرتبطة به.

### نموذج التعليمات البرمجية المصدر لإضافة توقيع رقمي إلى ملف Excel موقّع بالفعل باستخدام Aspose.Cells لـ .NET 
```csharp
//دليل المصدر
string sourceDir = RunExamples.Get_SourceDirectory();
//دليل الإخراج
string outputDir = RunExamples.Get_OutputDirectory();
//ملف الشهادة وكلمة المرور الخاصة بها
string certFileName = sourceDir + "AsposeDemo.pfx";
string password = "aspose";
//قم بتحميل المصنف الموقع رقميًا بالفعل لإضافة توقيع رقمي جديد
Aspose.Cells.Workbook workbook = new Aspose.Cells.Workbook(sourceDir + "sampleDigitallySignedByCells.xlsx");
//إنشاء مجموعة التوقيع الرقمي
Aspose.Cells.DigitalSignatures.DigitalSignatureCollection dsCollection = new Aspose.Cells.DigitalSignatures.DigitalSignatureCollection();
//إنشاء شهادة جديدة
System.Security.Cryptography.X509Certificates.X509Certificate2 certificate = new System.Security.Cryptography.X509Certificates.X509Certificate2(certFileName, password);
//قم بإنشاء توقيع رقمي جديد وإضافته إلى مجموعة التوقيع الرقمي
Aspose.Cells.DigitalSignatures.DigitalSignature signature = new Aspose.Cells.DigitalSignatures.DigitalSignature(certificate, "Aspose.Cells added new digital signature in existing digitally signed workbook.", DateTime.Now);
dsCollection.Add(signature);
//أضف مجموعة التوقيع الرقمي داخل المصنف
workbook.AddDigitalSignature(dsCollection);
//احفظ المصنف وتخلص منه.
workbook.Save(outputDir + "outputDigitallySignedByCells.xlsx");
workbook.Dispose();
Console.WriteLine("AddDigitalSignatureToAnAlreadySignedExcelFile executed successfully.\r\n");
```

## خاتمة

تهنئة ! لقد تعلمت الآن كيفية إضافة توقيع رقمي إلى ملف Excel موقع بالفعل باستخدام Aspose.Cells لـ .NET. تضيف التوقيعات الرقمية طبقة إضافية من الأمان إلى ملفات Excel الخاصة بك، مما يضمن صحتها وسلامتها.

### الأسئلة الشائعة

#### س: ما هو Aspose.Cells لـ .NET؟

ج: Aspose.Cells for .NET هي مكتبة فئة قوية تسمح لمطوري .NET بإنشاء ملفات Excel وتعديلها وتحويلها ومعالجتها بسهولة.

#### س: ما هو التوقيع الرقمي في ملف Excel؟

ج: التوقيع الرقمي في ملف Excel هو علامة إلكترونية تضمن صحة الوثيقة وسلامتها وأصلها. يتم استخدامه للتحقق من أن الملف لم يتم تعديله منذ التوقيع عليه وأنه يأتي من مصدر موثوق.

#### س: ما هي فوائد إضافة توقيع رقمي إلى ملف Excel؟

ج: توفر إضافة توقيع رقمي إلى ملف Excel العديد من الفوائد، بما في ذلك الحماية من التغييرات غير المصرح بها، وضمان سلامة البيانات، والمصادقة على مؤلف المستند، وتوفير الثقة في المعلومات "التي يحتوي عليها".

#### س: هل يمكنني إضافة توقيعات رقمية متعددة إلى ملف Excel؟

ج: نعم، يسمح لك Aspose.Cells بإضافة توقيعات رقمية متعددة إلى ملف Excel. يمكنك إنشاء مجموعة من التوقيعات الرقمية وإضافتها إلى الملف في عملية واحدة.

#### س: ما هي متطلبات إضافة توقيع رقمي إلى ملف Excel؟

ج: لإضافة توقيع رقمي إلى ملف Excel، فإنك تحتاج إلى شهادة رقمية صالحة سيتم استخدامها لتوقيع المستند. تأكد من حصولك على الشهادة وكلمة المرور الصحيحتين قبل إضافة التوقيع الرقمي.