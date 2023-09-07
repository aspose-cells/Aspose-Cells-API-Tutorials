---
title: أضف التوقيع الرقمي إلى ملف Excel موقّع بالفعل
linktitle: أضف التوقيع الرقمي إلى ملف Excel موقّع بالفعل
second_title: Aspose.Cells لمرجع .NET API
description: قم بإضافة التوقيعات الرقمية بسهولة إلى ملفات Excel الموجودة باستخدام Aspose.Cells for .NET.
type: docs
weight: 30
url: /ar/net/excel-workbook/add-digital-signature-to-an-already-signed-excel-file/
---
في هذا الدليل المفصل خطوة بخطوة ، سنشرح الكود المصدري C # الذي سيتيح لك إضافة توقيع رقمي إلى ملف Excel موقّع بالفعل باستخدام Aspose.Cells for .NET. اتبع الخطوات أدناه لإضافة توقيع رقمي جديد إلى ملف Excel موجود.

## الخطوة 1: تعيين أدلة المصدر والمخرجات

```csharp
// دليل المصدر
string sourceDir = RunExamples.Get_SourceDirectory();

// دليل الإخراج
string outputDir = RunExamples.Get_OutputDirectory();
```

في هذه الخطوة الأولى ، نحدد مجلدات المصدر والمخرجات التي سيتم استخدامها لتحميل ملف Excel الحالي وحفظ الملف بالتوقيع الرقمي الجديد.

## الخطوة 2: تحميل ملف Excel الحالي

```csharp
// قم بتحميل مصنف Excel الموقع بالفعل
Aspose.Cells.Workbook workbook = new Aspose.Cells.Workbook(sourceDir + "sampleDigitallySignedByCells.xlsx");
```

 هنا نقوم بتحميل ملف Excel الموقع بالفعل باستخدام ملف`Workbook` فئة Aspose.Cells.

## الخطوة 3: قم بإنشاء مجموعة التوقيعات الرقمية

```csharp
// قم بإنشاء مجموعة التوقيعات الرقمية
Aspose.Cells.DigitalSignatures.DigitalSignatureCollection dsCollection = new Aspose.Cells.DigitalSignatures.DigitalSignatureCollection();
```

 نقوم بإنشاء مجموعة جديدة من التواقيع الرقمية باستخدام`DigitalSignatureCollection` فصل.

## الخطوة 4: إنشاء شهادة جديدة

```csharp
// قم بإنشاء شهادة جديدة
System.Security.Cryptography.X509Certificates.X509Certificate2 certificate = new System.Security.Cryptography.X509Certificates.X509Certificate2(certFileName, password);
```

هنا نقوم بإنشاء شهادة جديدة من الملف المقدم وكلمة المرور.

## الخطوة 5: أضف توقيعًا رقميًا جديدًا إلى المجموعة

```csharp
// قم بإنشاء توقيع رقمي جديد
Aspose.Cells.DigitalSignatures.DigitalSignature signature = new Aspose.Cells.DigitalSignatures.DigitalSignature(certificate, "Aspose.Cells added a new digital signature to the already signed workbook.", DateTime.Now);

// أضف التوقيع الرقمي إلى المجموعة
dsCollection.Add(signature);
```

 نقوم بإنشاء توقيع رقمي جديد باستخدام`DigitalSignature` فئة وإضافتها إلى مجموعة التوقيعات الرقمية.

## الخطوة 6: أضف مجموعة التوقيعات الرقمية إلى المصنف

```csharp
//أضف مجموعة التوقيعات الرقمية إلى المصنف
workbook.AddDigitalSignature(dsCollection);
```

 نضيف مجموعة التوقيعات الرقمية إلى مصنف Excel الحالي باستخدام ملف`AddDigitalSignature()` طريقة.

## الخطوة 7: احفظ وأغلق المصنف

```csharp
// احفظ المصنف وأغلقه
workbook.Save(outputDir + "outputDigitallySignedByCells.xlsx");
workbook.Dispose();
```

نحفظ المصنف بالتوقيع الرقمي الجديد في دليل الإخراج المحدد ، ثم نغلقه ونطلق الموارد المرتبطة به.

### نموذج التعليمات البرمجية المصدر لإضافة توقيع رقمي إلى ملف Excel تم توقيعه بالفعل باستخدام Aspose.Cells for .NET 
```csharp
//دليل المصدر
string sourceDir = RunExamples.Get_SourceDirectory();
//دليل الإخراج
string outputDir = RunExamples.Get_OutputDirectory();
//ملف الشهادة وكلمة المرور الخاصة به
string certFileName = sourceDir + "AsposeDemo.pfx";
string password = "aspose";
//قم بتحميل المصنف الموقّع رقميًا بالفعل لإضافة توقيع رقمي جديد
Aspose.Cells.Workbook workbook = new Aspose.Cells.Workbook(sourceDir + "sampleDigitallySignedByCells.xlsx");
//قم بإنشاء مجموعة التوقيع الرقمي
Aspose.Cells.DigitalSignatures.DigitalSignatureCollection dsCollection = new Aspose.Cells.DigitalSignatures.DigitalSignatureCollection();
//إنشاء شهادة جديدة
System.Security.Cryptography.X509Certificates.X509Certificate2 certificate = new System.Security.Cryptography.X509Certificates.X509Certificate2(certFileName, password);
//أنشئ توقيعًا رقميًا جديدًا وأضفه في مجموعة التوقيع الرقمي
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

تهنئة ! لقد تعلمت الآن كيفية إضافة توقيع رقمي إلى ملف Excel موقع بالفعل باستخدام Aspose.Cells for .NET. تضيف التوقيعات الرقمية طبقة إضافية من الأمان إلى ملفات Excel الخاصة بك ، مما يضمن صحتها وسلامتها.

### أسئلة وأجوبة

#### س: ما هو Aspose.Cells لـ .NET؟

ج: Aspose.Cells for .NET هي مكتبة فصول قوية تسمح لمطوري .NET بإنشاء وتعديل وتحويل ومعالجة ملفات Excel بسهولة.

#### س: ما هو التوقيع الرقمي في ملف Excel؟

ج: التوقيع الرقمي في ملف Excel هو علامة إلكترونية تضمن أصالة المستند وسلامته وأصله. يتم استخدامه للتحقق من أن الملف لم يتم تعديله منذ توقيعه وأنه يأتي من مصدر موثوق.

#### س: ما هي فوائد إضافة توقيع رقمي إلى ملف Excel؟

ج: توفر إضافة توقيع رقمي إلى ملف Excel العديد من الفوائد ، بما في ذلك الحماية من التغييرات غير المصرح بها ، وضمان سلامة البيانات ، ومصادقة مؤلف المستند ، وتوفير الثقة في المعلومات التي يحتوي عليها.

#### س: هل يمكنني إضافة عدة تواقيع رقمية إلى ملف Excel؟

ج: نعم ، يسمح لك Aspose.Cells بإضافة توقيعات رقمية متعددة إلى ملف Excel. يمكنك إنشاء مجموعة من التوقيعات الرقمية وإضافتها إلى الملف في عملية واحدة.

#### س: ما هي متطلبات إضافة توقيع رقمي إلى ملف Excel؟

ج: لإضافة توقيع رقمي إلى ملف Excel ، تحتاج إلى شهادة رقمية صالحة سيتم استخدامها لتوقيع المستند. تأكد من حصولك على الشهادة وكلمة المرور الصحيحين قبل إضافة التوقيع الرقمي.