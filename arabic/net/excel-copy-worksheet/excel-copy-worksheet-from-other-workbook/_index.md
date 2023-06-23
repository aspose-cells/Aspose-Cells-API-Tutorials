---
title: Excel نسخ ورقة العمل من مصنف آخر
linktitle: Excel نسخ ورقة العمل من مصنف آخر
second_title: Aspose.Cells لمرجع .NET API
description: انسخ ورقة عمل Excel بسهولة من مصنف إلى آخر باستخدام Aspose.Cells for .NET.
type: docs
weight: 10
url: /ar/net/excel-copy-worksheet/excel-copy-worksheet-from-other-workbook/
---
في هذا البرنامج التعليمي ، سنرشدك خلال الخطوات لنسخ ورقة عمل Excel من مصنف آخر باستخدام مكتبة Aspose.Cells لـ .NET. اتبع التعليمات أدناه لإكمال هذه المهمة.

## الخطوة الأولى: التحضير

قبل أن تبدأ ، تأكد من تثبيت Aspose.Cells لـ .NET وإنشاء مشروع C # في بيئة التطوير المتكاملة المفضلة لديك (IDE).

## الخطوة 2: قم بتعيين مسار دليل المستند

 تعلن أ`dataDir` متغير وتهيئته بالمسار إلى دليل المستندات. على سبيل المثال :

```csharp
string dataDir = "YOUR_DIRECTORY_OF_DOCUMENTS";
```

 تأكد من استبدال`"YOUR_DOCUMENTS_DIRECTORY"` مع المسار الفعلي للدليل الخاص بك.

## الخطوة 3: قم بإنشاء مصنف Excel جديد

 استخدم ال`Workbook` فئة من Aspose.Cells لإنشاء مصنف Excel جديد:

```csharp
Workbook excelWorkbook0 = new Workbook();
```

## الخطوة 4: احصل على ورقة العمل الأولى في المصنف

انتقل إلى ورقة العمل الأولى في المصنف باستخدام الفهرس 0:

```csharp
Worksheet ws0 = excelWorkbook0.Worksheets[0];
```

## الخطوة 5: إضافة البيانات إلى صفوف الرأس (A1: A4)

 إستخدم`for` حلقة لإضافة البيانات إلى صفوف الرأس (A1: A4):

```csharp
for (int i = 0; i < 5; i++)
{
     ws0.Cells[i, 0].PutValue(string.Format("Header row {0}", i));
}
```

## الخطوة 6: إضافة بيانات مفصلة (A5: A999)

 استخدم آخر`for` حلقة لإضافة بيانات مفصلة (A5: A999):

```csharp
for (int i = 5; i < 1000; i++)
{
     ws0.Cells[i, 0].PutValue(string.Format("Detail row {0}", i));
}
```

## الخطوة 7: تعيين خيارات التخطيط

 عيّن خيارات إعداد الصفحة لورقة العمل باستخدام امتداد`PageSetup` هدف:

```csharp
PageSetup pagesetup = ws0.PageSetup;
pagesetup.PrintTitleRows = "$1:$5";
```

## الخطوة 8: قم بإنشاء مصنف Excel آخر

قم بإنشاء مصنف Excel آخر:

```csharp
Workbook excelWorkbook1 = new Workbook();
```

## الخطوة 9: احصل على ورقة العمل الأولى من المصنف الثاني

انتقل إلى ورقة العمل الأولى في المصنف الثاني:

```csharp
Worksheet ws1 = excelWorkbook1.Worksheets[0];
```

## الخطوة 10: قم بتسمية ورقة العمل

اسم النار

جزيرة الحساب:

```csharp
ws1.Name = "MySheet";
```

## الخطوة 11: انسخ البيانات من ورقة العمل الأولى من المصنف الأول إلى ورقة العمل الأولى من المصنف الثاني

انسخ البيانات من ورقة العمل الأولى من المصنف الأول إلى ورقة العمل الأولى من المصنف الثاني:

```csharp
ws1.Copy(ws0);
```

## الخطوة 12: احفظ ملف Excel

احفظ ملف Excel:

```csharp
excelWorkbook1.Save(dataDir + "CopyWorkbookSheetToOther_out.xls");
```

تأكد من تحديد المسار المطلوب واسم الملف لملف الإخراج.

### نموذج التعليمات البرمجية المصدر لبرنامج Excel نسخ ورقة العمل من مصنف آخر باستخدام Aspose.Cells for .NET 
```csharp
// المسار إلى دليل المستندات.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// قم بإنشاء مصنف جديد.
Workbook excelWorkbook0 = new Workbook();
// احصل على ورقة العمل الأولى في الكتاب.
Worksheet ws0 = excelWorkbook0.Worksheets[0];
// ضع بعض البيانات في صفوف الرأس (A1: A4)
for (int i = 0; i < 5; i++)
{
	ws0.Cells[i, 0].PutValue(string.Format("Header Row {0}", i));
}
// ضع بعض البيانات التفصيلية (A5: A999)
for (int i = 5; i < 1000; i++)
{
	ws0.Cells[i, 0].PutValue(string.Format("Detail Row {0}", i));
}
// حدد كائن إعداد الصفحات بناءً على ورقة العمل الأولى.
PageSetup pagesetup = ws0.PageSetup;
// تتكرر الصفوف الخمسة الأولى في كل صفحة ...
// يمكن رؤيته في المعاينة قبل الطباعة.
pagesetup.PrintTitleRows = "$1:$5";
// قم بإنشاء مصنف آخر.
Workbook excelWorkbook1 = new Workbook();
// احصل على ورقة العمل الأولى في الكتاب.
Worksheet ws1 = excelWorkbook1.Worksheets[0];
// اسم ورقة العمل.
ws1.Name = "MySheet";
// انسخ البيانات من ورقة العمل الأولى من المصنف الأول إلى ملف
// ورقة العمل الأولى من المصنف الثاني.
ws1.Copy(ws0);
// احفظ ملف اكسل.
excelWorkbook1.Save(dataDir + "CopyWorksheetFromWorkbookToOther_out.xls");
```

## خاتمة

تهنئة ! لقد تعلمت الآن كيفية نسخ ورقة عمل Excel من مصنف آخر باستخدام Aspose.Cells for .NET. لا تتردد في استخدام هذه الطريقة في مشاريعك الخاصة لمعالجة ملفات Excel بكفاءة.

### أسئلة وأجوبة

#### س: ما هي المكتبات اللازمة لاستخدام Aspose.Cells لـ .NET؟

A. لاستخدام Aspose.Cells لـ .NET ، يجب عليك تضمين مكتبة Aspose.Cells في مشروعك. تأكد من الرجوع إلى هذه المكتبة بشكل صحيح في بيئة التطوير المتكاملة (IDE).

#### س: هل تدعم Aspose.Cells تنسيقات ملفات Excel الأخرى ، مثل XLSX؟

A. نعم ، Aspose.Cells يدعم العديد من تنسيقات ملفات Excel بما في ذلك XLSX و XLS و CSV و HTML وغيرها الكثير. يمكنك معالجة تنسيقات الملفات هذه باستخدام ميزات Aspose.Cells for .NET.

#### س هل يمكنني تخصيص خيارات التخطيط عند نسخ ورقة العمل؟

A.  نعم ، يمكنك تخصيص خيارات إعداد الصفحة عند نسخ ورقة العمل باستخدام خصائص ملف`PageSetup` هدف. يمكنك تحديد رؤوس الصفحات ، والتذييلات ، والهوامش ، والاتجاهات ، وما إلى ذلك.