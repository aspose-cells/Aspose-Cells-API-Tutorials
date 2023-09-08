---
title: إخفاء وإظهار ورقة العمل
linktitle: إخفاء وإظهار ورقة العمل
second_title: Aspose.Cells لمرجع .NET API
description: مكتبة قوية للتعامل مع ملفات Excel، بما في ذلك إنشاء البيانات وتعديلها ومعالجتها.
type: docs
weight: 90
url: /ar/net/excel-display-settings-csharp-tutorials/hide-and-unhide-worksheet/
---
في هذا البرنامج التعليمي، سنأخذك خطوة بخطوة لشرح كود مصدر C# التالي والذي يُستخدم لإخفاء وإظهار ورقة العمل باستخدام Aspose.Cells for .NET. اتبع الخطوات التالية:

## الخطوة 1: إعداد البيئة

قبل البدء، تأكد من تثبيت Aspose.Cells for .NET على نظامك. إذا لم تكن قد قمت بتثبيته بالفعل، فيمكنك تنزيله من موقع Aspose الرسمي. بمجرد التثبيت، يمكنك إنشاء مشروع جديد في بيئة التطوير المتكاملة المفضلة لديك (IDE).

## الخطوة 2: استيراد مساحات الأسماء المطلوبة

في ملف مصدر C#، أضف مساحات الأسماء الضرورية لاستخدام ميزات Aspose.Cells. أضف الأسطر التالية إلى بداية ملفك:

```csharp
using Aspose.Cells;
using System.IO;
```

## الخطوة 3: قم بتحميل ملف Excel

قبل إخفاء ورقة العمل أو إظهارها، يجب عليك تحميل ملف Excel في التطبيق الخاص بك. تأكد من أن لديك ملف Excel الذي تريد استخدامه في نفس الدليل مثل مشروعك. استخدم الكود التالي لتحميل ملف Excel:

```csharp
string dataDir = "PATH TO YOUR DOCUMENTS DIRECTORY";
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
Workbook workbook = new Workbook(fstream);
```

تأكد من استبدال "PATH TO YOUR DOCUMENTS DIRECTORY" بالمسار الفعلي للدليل الذي يحتوي على ملف Excel الخاص بك.

## الخطوة 4: الوصول إلى جدول البيانات

بمجرد تحميل ملف Excel، يمكنك الانتقال إلى ورقة العمل التي تريد إخفاءها أو إظهارها. استخدم الكود التالي للوصول إلى ورقة العمل الأولى في الملف:

```csharp
Worksheet worksheet = workbook.Worksheets[0];
```

## الخطوة 5: إخفاء ورقة العمل

 الآن بعد أن قمت بالوصول إلى ورقة العمل، يمكنك إخفائها باستخدام`IsVisible` ملكية. استخدم الكود التالي لإخفاء ورقة العمل الأولى في الملف:

```csharp
worksheet. IsVisible = false;
```

## الخطوة 6: إعادة عرض ورقة العمل

إذا كنت تريد إعادة عرض ورقة العمل المخفية مسبقًا، فيمكنك استخدام نفس الرمز عن طريق تغيير قيمة ملف`IsVisible` ملكية. استخدم الكود التالي لإعادة عرض ورقة العمل الأولى:

```csharp
worksheet. IsVisible = true;
```

## الخطوة 7: حفظ التغييرات

بمجرد

  قمت بإخفاء ورقة العمل أو إظهارها حسب الحاجة، فيجب عليك حفظ التغييرات في ملف Excel. استخدم الكود التالي لحفظ التغييرات:

```csharp
workbook.Save(dataDir + "output.out.xls");
fstream.Close();
```

تأكد من تحديد مسار الإخراج الصحيح لحفظ ملف Excel المعدل.

### نموذج التعليمات البرمجية المصدر لـ Hide And Unhide Worksheet باستخدام Aspose.Cells لـ .NET 

```csharp
//المسار إلى دليل المستندات.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// إنشاء دفق ملف يحتوي على ملف Excel المراد فتحه
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
// إنشاء مثيل لكائن المصنف من خلال فتح ملف Excel من خلال دفق الملف
Workbook workbook = new Workbook(fstream);
// الوصول إلى ورقة العمل الأولى في ملف Excel
Worksheet worksheet = workbook.Worksheets[0];
// إخفاء ورقة العمل الأولى من ملف Excel
worksheet.IsVisible = false;
// يظهر ورقة العمل الأولى من ملف Excel
//Worksheet.IsVisible = true;
// حفظ ملف Excel المعدل بالتنسيق الافتراضي (أي Excel 2003).
workbook.Save(dataDir + "output.out.xls");
// إغلاق دفق الملف لتحرير كافة الموارد
fstream.Close();
```

## خاتمة

تهنئة ! لقد تعلمت كيفية إخفاء جدول بيانات وإظهاره باستخدام Aspose.Cells لـ .NET. يمكنك الآن استخدام هذه الميزة للتحكم في رؤية جداول البيانات الخاصة بك في ملفات Excel.

### أسئلة وأجوبة (FAQ)

#### كيف يمكنني تثبيت Aspose.Cells لـ .NET؟

 يمكنك تثبيت Aspose.Cells لـ .NET عن طريق تنزيل حزمة NuGet ذات الصلة من[إصدارات Aspose](https://releases/aspose.com/cells/net/) وإضافته إلى مشروع Visual Studio الخاص بك.

#### ما هو الحد الأدنى المطلوب من إصدار .NET Framework لاستخدام Aspose.Cells لـ .NET؟

يدعم Aspose.Cells for .NET .NET Framework 2.0 والإصدارات الأحدث.

#### هل يمكنني فتح ملفات Excel الموجودة وتحريرها باستخدام Aspose.Cells لـ .NET؟

نعم، يمكنك فتح ملفات Excel الموجودة وتحريرها باستخدام Aspose.Cells لـ .NET. يمكنك الوصول إلى أوراق العمل والخلايا والصيغ والعناصر الأخرى في ملف Excel.

#### هل يدعم Aspose.Cells for .NET إعداد التقارير والتصدير إلى تنسيقات ملفات أخرى؟

نعم، يدعم Aspose.Cells for .NET إنشاء التقارير وتصديرها إلى تنسيقات مثل PDF وHTML وCSV وTXT وما إلى ذلك.

#### هل التعديل على ملف الاكسل نهائي؟

نعم، يصبح تعديل ملف Excel نهائيًا بمجرد حفظه. تأكد من حفظ نسخة احتياطية قبل إجراء أي تغييرات على الملف الأصلي.