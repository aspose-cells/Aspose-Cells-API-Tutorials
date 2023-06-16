---
title: قم بإزالة إعدادات الطابعة الحالية لأوراق العمل
linktitle: قم بإزالة إعدادات الطابعة الحالية لأوراق العمل
second_title: Aspose.Cells لمرجع .NET API
description: تعرف على كيفية إزالة إعدادات الطابعة الحالية من جداول بيانات Excel باستخدام Aspose.Cells for .NET.
type: docs
weight: 80
url: /ar/net/excel-page-setup/remove-existing-printer-settings-of-worksheets/
---
في هذا البرنامج التعليمي ، سنرشدك خطوة بخطوة حول كيفية إزالة إعدادات الطابعة الحالية من أوراق العمل في Excel باستخدام Aspose.Cells for .NET. سوف نستخدم كود المصدر C # لتوضيح العملية.

## الخطوة الأولى: تهيئة البيئة

تأكد من تثبيت Aspose.Cells for .NET على جهازك. قم أيضًا بإنشاء مشروع جديد في بيئة التطوير المفضلة لديك.

## الخطوة 2: استيراد المكتبات الضرورية

في ملف التعليمات البرمجية الخاص بك ، قم باستيراد المكتبات اللازمة للعمل مع Aspose.Cells. هذا هو الكود المقابل:

```csharp
using Aspose.Cells;
```

## الخطوة 3: تعيين أدلة المصدر والمخرجات

قم بتعيين مجلدي المصدر والمخرجات حيث يوجد ملف Excel الأصلي والمكان الذي تريد حفظ الملف المعدل فيه على التوالي. استخدم الكود التالي:

```csharp
string sourceDir = "SOURCE DIRECTORY PATH";
string outputDir = "OUTPUT DIRECTORY PATH";
```

تأكد من تحديد مسارات الدليل الكاملة.

## الخطوة 4: تحميل ملف Excel المصدر

قم بتحميل ملف Excel المصدر باستخدام الكود التالي:

```csharp
Workbook wb = new Workbook(sourceDir + "fileName.xlsx");
```

سيؤدي هذا إلى تحميل ملف Excel المحدد في كائن المصنف.

## الخطوة 5: تصفح أوراق العمل

كرر خلال جميع أوراق العمل في المصنف باستخدام حلقة. استخدم الكود التالي:

```csharp
int sheetCount = wb. Worksheets. Count;

for (int i = 0; i < sheetCount; i++)
{
     Worksheet ws = wb.Worksheets[i];
     // ستتم إضافة باقي الكود في الخطوة التالية.
}
```

## الخطوة 6: حذف إعدادات الطابعة الموجودة

تحقق من وجود إعدادات الطابعة لكل ورقة عمل وحذفها إذا لزم الأمر. استخدم الكود التالي:

```csharp
PageSetup ps = ws.PageSetup;

if (ps.PrinterSettings != null)
{
     Console.WriteLine("Printer settings for this spreadsheet exist.");
     Console.WriteLine("Sheet name: " + ws.Name);
     Console.WriteLine("Paper size: " + ps.PaperSize);

     ps.PrinterSettings = null;

     Console.WriteLine("Printer settings for this spreadsheet have been removed by setting them to null.");
     Console.WriteLine("");
}
```

## الخطوة 7: حفظ المصنف المعدل

احفظ المصنف المعدل باستخدام الكود التالي:

```csharp
wb.Save(outputDir + "modifiedFilename.xlsx");
```

سيؤدي هذا إلى حفظ المصنف المعدل في دليل الإخراج المحدد.

### نموذج التعليمات البرمجية المصدر لإزالة إعدادات الطابعة الحالية لأوراق العمل باستخدام Aspose.Cells for .NET 
```csharp
//دليل المصدر
string sourceDir = RunExamples.Get_SourceDirectory();
//دليل الإخراج
string outputDir = RunExamples.Get_OutputDirectory();
//تحميل ملف Excel المصدر
Workbook wb = new Workbook(sourceDir + "sampleRemoveExistingPrinterSettingsOfWorksheets.xlsx");
//احصل على عدد أوراق المصنف
int sheetCount = wb.Worksheets.Count;
//كرر كل الأوراق
for (int i = 0; i < sheetCount; i++)
{
    //قم بالوصول إلى ورقة العمل i
    Worksheet ws = wb.Worksheets[i];
    //الوصول إلى إعداد صفحة ورقة العمل
    PageSetup ps = ws.PageSetup;
    //تحقق من وجود إعدادات الطابعة لورقة العمل هذه
    if (ps.PrinterSettings != null)
    {
        //اطبع الرسالة التالية
        Console.WriteLine("PrinterSettings of this worksheet exist.");
        //طباعة اسم الورقة وحجم الورق الخاص بها
        Console.WriteLine("Sheet Name: " + ws.Name);
        Console.WriteLine("Paper Size: " + ps.PaperSize);
        //قم بإزالة إعدادات الطابعة عن طريق تعيينها فارغة
        ps.PrinterSettings = null;
        Console.WriteLine("Printer settings of this worksheet are now removed by setting it null.");
        Console.WriteLine("");
    }//لو
}//ل
//احفظ المصنف
wb.Save(outputDir + "outputRemoveExistingPrinterSettingsOfWorksheets.xlsx");
```

## خاتمة

لقد تعلمت الآن كيفية إزالة إعدادات الطابعة الموجودة من أوراق العمل في Excel باستخدام Aspose.Cells for .NET. يرشدك هذا البرنامج التعليمي خلال كل خطوة من خطوات العملية ، من إعداد البيئة إلى التنقل عبر جداول البيانات ومسح إعدادات الطابعة. يمكنك الآن استخدام هذه المعرفة لإدارة إعدادات الطابعة في ملفات Excel الخاصة بك.

### التعليمات

#### س 1: كيف يمكنني معرفة ما إذا كان جدول بيانات يحتوي على إعدادات طابعة موجودة؟

 ج ١: يمكنك التحقق مما إذا كانت إعدادات الطابعة موجودة لورقة عمل عن طريق الوصول إلى ملف`PrinterSettings` ممتلكات`PageSetup` هدف. إذا كانت القيمة غير فارغة ، فهذا يعني أن هناك إعدادات طابعة موجودة.

#### س 2: هل يمكنني حذف إعدادات الطابعة لجدول بيانات معين فقط؟

 ج 2: نعم ، يمكنك استخدام نفس الأسلوب لإزالة إعدادات الطابعة لورقة عمل معينة عن طريق الوصول إلى ورقة العمل هذه`PageSetup` هدف.

#### س 3: هل تقوم هذه الطريقة بإزالة إعدادات التخطيط الأخرى أيضًا؟

ج ٣: لا ، هذه الطريقة تحذف فقط إعدادات الطابعة. تظل إعدادات التخطيط الأخرى ، مثل الهوامش واتجاه الورق وما إلى ذلك ، بدون تغيير.

#### س 4: هل تعمل هذه الطريقة مع كافة تنسيقات ملفات Excel ، مثل .xls و. xlsx؟

A4: نعم ، تعمل هذه الطريقة مع جميع تنسيقات ملفات Excel التي يدعمها Aspose.Cells ، بما في ذلك .xls و. xlsx.

#### س 5: هل التغييرات التي يتم إجراؤها على إعدادات الطابعة دائمة في ملف Excel المحرر؟

ج 5: نعم ، يتم حفظ التغييرات التي تم إجراؤها على إعدادات الطابعة بشكل دائم في ملف Excel المحرر.