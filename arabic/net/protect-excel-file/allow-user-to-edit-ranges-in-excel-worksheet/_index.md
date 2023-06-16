---
title: السماح للمستخدم بتحرير النطاقات في ورقة عمل Excel
linktitle: السماح للمستخدم بتحرير النطاقات في ورقة عمل Excel
second_title: Aspose.Cells لمرجع .NET API
description: السماح للمستخدمين بتحرير نطاقات محددة في جدول بيانات Excel باستخدام Aspose.Cells لـ .NET. دليل خطوة بخطوة مع شفرة المصدر في C #.
type: docs
weight: 10
url: /ar/net/protect-excel-file/allow-user-to-edit-ranges-in-excel-worksheet/
---
في هذا الدليل ، سنرشدك إلى كيفية استخدام Aspose.Cells for .NET للسماح للمستخدم بتحرير نطاقات محددة في جدول بيانات Excel. اتبع الخطوات أدناه لإنجاز هذه المهمة.

## الخطوة الأولى: تهيئة البيئة

تأكد من قيامك بإعداد بيئة التطوير الخاصة بك وتثبيت Aspose.Cells لـ .NET. يمكنك تنزيل أحدث إصدار من المكتبة من موقع Aspose الرسمي.

## الخطوة 2: استيراد مساحات الأسماء المطلوبة

في مشروع C # الخاص بك ، قم باستيراد مساحات الأسماء الضرورية للعمل مع Aspose.

```csharp
using Aspose.Cells;
```

## الخطوة 3: تحديد المسار إلى دليل المستندات

 تعلن أ`dataDir` متغير لتحديد المسار إلى الدليل حيث تريد حفظ ملف Excel الذي تم إنشاؤه:

```csharp
string dataDir = "YOUR_DIRECTORY_OF_DOCUMENTS";
```

 تأكد من استبدال`"YOUR_DOCUMENT_DIRECTORY"` مع المسار الصحيح على نظامك.

## الخطوة 4: إنشاء كائن مصنف

إنشاء كائن مصنف جديد يمثل مصنف Excel الذي تريد إنشاءه:

```csharp
Workbook book = new Workbook();
```

## الخطوة 5: الوصول إلى ورقة العمل الأولى

انتقل إلى ورقة العمل الأولى في مصنف Excel باستخدام الكود التالي:

```csharp
Worksheet sheet = book.Worksheets[0];
```

## الخطوة 6: استرداد نطاقات التعديل المصرح بها

 احصل على مجموعة نطاقات التحرير المسموح بها باستخدام امتداد`AllowEditRanges` ملكية:

```csharp
ProtectedRangeCollection allowRanges = sheet.AllowEditRanges;
```

## الخطوة 7: تحديد نطاق محمي

 حدد نطاقًا محميًا باستخدام`Add` طريقة`AllowEditRanges` مجموعة:

```csharp
int idx = allowRanges.Add("r2", 1, 1, 3, 3);
protectedRange protectedRange = allowRanges[idx];
```

لقد أنشأنا هنا نطاقًا محميًا "r2" يمتد من الخلية A1 إلى الخلية C3.

## الخطوة 8: تحديد كلمة المرور

 حدد كلمة مرور للنطاق المحمي باستخدام امتداد`Password` ملكية:

```csharp
protectedRange.Password = "YOUR_PASSWORD";
```

 تأكد من استبدال`"YOUR_PASSWORD"` بكلمة المرور المطلوبة.

## الخطوة 9: حماية ورقة العمل

 قم بحماية ورقة العمل باستخدام الامتداد`Protect` طريقة`Worksheet` هدف:

```csharp
sheet.Protect(ProtectionType.All);
```

سيؤدي ذلك إلى حماية جدول البيانات عن طريق منع أي تعديل خارج النطاقات المسموح بها.

## الخطوة 10: تسجيل ملف

  ملف اكسل

 احفظ ملف Excel الذي تم إنشاؤه باستخدام ملف`Save` طريقة`Workbook` هدف:

```csharp
book.Save(dataDir + "protectedrange.out.xls");
```

تأكد من تحديد اسم الملف المطلوب والمسار الصحيح.

### نموذج التعليمات البرمجية المصدر لـ السماح للمستخدم بتحرير النطاقات في ورقة عمل Excel باستخدام Aspose.Cells for .NET 
```csharp
// المسار إلى دليل المستندات.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// قم بإنشاء دليل إذا لم يكن موجودًا بالفعل.
bool IsExists = System.IO.Directory.Exists(dataDir);
if (!IsExists)
    System.IO.Directory.CreateDirectory(dataDir);
// إنشاء مصنف جديد
Workbook book = new Workbook();
// احصل على أول ورقة عمل (افتراضية)
Worksheet sheet = book.Worksheets[0];
// احصل على السماح بتحرير النطاقات
ProtectedRangeCollection allowRanges = sheet.AllowEditRanges;
// حدد ProtectedRange
ProtectedRange proteced_range;
// قم بإنشاء النطاق
int idx = allowRanges.Add("r2", 1, 1, 3, 3);
proteced_range = allowRanges[idx];
// حدد كلمة المرور
proteced_range.Password = "123";
// احمِ الورقة
sheet.Protect(ProtectionType.All);
// احفظ ملف Excel
book.Save(dataDir + "protectedrange.out.xls");
```

## خاتمة

لقد تعلمت الآن كيفية استخدام Aspose.Cells لـ .NET للسماح للمستخدم بتحرير نطاقات محددة في جدول بيانات Excel. لا تتردد في استكشاف المزيد من الميزات التي تقدمها Aspose.Cells لتلبية احتياجاتك الخاصة.


### أسئلة وأجوبة

#### 1. كيف تسمح للمستخدم بتحرير نطاقات محددة في جدول بيانات Excel؟

 يمكنك استخدام ال`ProtectedRangeCollection` فئة لتحديد نطاقات التعديل المسموح بها. استخدم ال`Add` طريقة لإنشاء نطاق محمي جديد بالخلايا المرغوبة.

#### 2. هل يمكنني تعيين كلمة مرور لنطاقات التعديل المصرح بها؟

 نعم ، يمكنك تحديد كلمة مرور باستخدام امتداد`Password` ممتلكات`ProtectedRange` هدف. سيؤدي هذا إلى تقييد الوصول إلى المستخدمين الذين لديهم كلمة المرور فقط.

#### 3. كيف يمكنني حماية جدول البيانات بمجرد تعيين النطاقات المسموح بها؟

 استخدم ال`Protect` طريقة`Worksheet` كائن لحماية ورقة العمل. سيمنع هذا أي تغييرات خارج النطاقات المسموح بها ، وربما يطالب بكلمة مرور إذا حددت واحدة.