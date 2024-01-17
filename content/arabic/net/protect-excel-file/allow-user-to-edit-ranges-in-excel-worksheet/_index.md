---
title: السماح للمستخدم بتحرير النطاقات في ورقة عمل Excel
linktitle: السماح للمستخدم بتحرير النطاقات في ورقة عمل Excel
second_title: Aspose.Cells لمرجع .NET API
description: السماح للمستخدمين بتحرير نطاقات معينة في جدول بيانات Excel باستخدام Aspose.Cells لـ .NET. دليل خطوة بخطوة مع الكود المصدري في C#.
type: docs
weight: 10
url: /ar/net/protect-excel-file/allow-user-to-edit-ranges-in-excel-worksheet/
---
سنرشدك في هذا الدليل إلى كيفية استخدام Aspose.Cells لـ .NET للسماح للمستخدم بتحرير نطاقات معينة في جدول بيانات Excel. اتبع الخطوات أدناه لإنجاز هذه المهمة.

## الخطوة 1: تهيئة البيئة

تأكد من قيامك بإعداد بيئة التطوير الخاصة بك وتثبيت Aspose.Cells لـ .NET. يمكنك تنزيل أحدث إصدار من المكتبة من موقع Aspose الرسمي.

## الخطوة 2: استيراد مساحات الأسماء المطلوبة

في مشروع C# الخاص بك، قم باستيراد مساحات الأسماء الضرورية للعمل مع Aspose.Cells:

```csharp
using Aspose.Cells;
```

## الخطوة 3: تحديد المسار إلى دليل المستندات

 أعلن أ`dataDir` متغير لتحديد المسار إلى الدليل الذي تريد حفظ ملف Excel الذي تم إنشاؤه فيه:

```csharp
string dataDir = "YOUR_DIRECTORY_OF_DOCUMENTS";
```

 تأكد من استبدال`"YOUR_DOCUMENT_DIRECTORY"` بالمسار الصحيح على نظامك.

## الخطوة 4: إنشاء كائن المصنف

قم بإنشاء كائن مصنف جديد يمثل مصنف Excel الذي تريد إنشاءه:

```csharp
Workbook book = new Workbook();
```

## الخطوة 5: الوصول إلى ورقة العمل الأولى

انتقل إلى ورقة العمل الأولى في مصنف Excel باستخدام الكود التالي:

```csharp
Worksheet sheet = book.Worksheets[0];
```

## الخطوة 6: استرداد نطاقات التعديل المعتمدة

 احصل على مجموعة نطاقات التحرير المسموح بها باستخدام`AllowEditRanges` ملكية:

```csharp
ProtectedRangeCollection allowRanges = sheet.AllowEditRanges;
```

## الخطوة 7: تحديد النطاق المحمي

 تحديد نطاق محمي باستخدام`Add` طريقة`AllowEditRanges` مجموعة:

```csharp
int idx = allowRanges.Add("r2", 1, 1, 3, 3);
protectedRange protectedRange = allowRanges[idx];
```

قمنا هنا بإنشاء نطاق محمي "r2" يمتد من الخلية A1 إلى الخلية C3.

## الخطوة 8: تحديد كلمة المرور

 حدد كلمة مرور للنطاق المحمي باستخدام`Password` ملكية:

```csharp
protectedRange.Password = "YOUR_PASSWORD";
```

 تأكد من استبدال`"YOUR_PASSWORD"` مع كلمة المرور المطلوبة.

## الخطوة 9: حماية ورقة العمل

 حماية ورقة العمل باستخدام`Protect` طريقة`Worksheet` هدف:

```csharp
sheet.Protect(ProtectionType.All);
```

سيؤدي هذا إلى حماية جدول البيانات عن طريق منع أي تعديل خارج النطاقات المسموح بها.

## الخطوة 10: تسجيل

  ملف اكسل

 احفظ ملف Excel الذي تم إنشاؤه باستخدام ملف`Save` طريقة`Workbook` هدف:

```csharp
book.Save(dataDir + "protectedrange.out.xls");
```

تأكد من تحديد اسم الملف المطلوب والمسار الصحيح.

### نموذج التعليمات البرمجية المصدر للسماح للمستخدم بتحرير النطاقات في ورقة عمل Excel باستخدام Aspose.Cells لـ .NET 
```csharp
//المسار إلى دليل المستندات.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// قم بإنشاء الدليل إذا لم يكن موجودًا بالفعل.
bool IsExists = System.IO.Directory.Exists(dataDir);
if (!IsExists)
    System.IO.Directory.CreateDirectory(dataDir);
// إنشاء مثيل لمصنف جديد
Workbook book = new Workbook();
// احصل على ورقة العمل الأولى (الافتراضية).
Worksheet sheet = book.Worksheets[0];
// احصل على السماح بنطاقات التحرير
ProtectedRangeCollection allowRanges = sheet.AllowEditRanges;
// تعريف النطاق المحمي
ProtectedRange proteced_range;
// قم بإنشاء النطاق
int idx = allowRanges.Add("r2", 1, 1, 3, 3);
proteced_range = allowRanges[idx];
// تحديد كلمة المرور
proteced_range.Password = "123";
// حماية الورقة
sheet.Protect(ProtectionType.All);
// احفظ ملف إكسل
book.Save(dataDir + "protectedrange.out.xls");
```

## خاتمة

لقد تعلمت الآن كيفية استخدام Aspose.Cells لـ .NET للسماح للمستخدم بتحرير نطاقات معينة في جدول بيانات Excel. لا تتردد في استكشاف المزيد من الميزات التي تقدمها Aspose.Cells لتلبية احتياجاتك الخاصة.


### الأسئلة الشائعة

#### 1. كيف تسمح للمستخدم بتحرير نطاقات محددة في جدول بيانات Excel؟

 يمكنك استخدام ال`ProtectedRangeCollection` فئة لتحديد نطاقات التعديل المسموح بها. استخدم ال`Add` طريقة لإنشاء نطاق محمي جديد بالخلايا المطلوبة.

#### 2. هل يمكنني تعيين كلمة مرور لنطاقات التعديل المعتمدة؟

 نعم، يمكنك تحديد كلمة مرور باستخدام`Password` ملكية`ProtectedRange` هدف. سيؤدي هذا إلى تقييد الوصول فقط للمستخدمين الذين لديهم كلمة المرور.

#### 3. كيف يمكنني حماية جدول البيانات بمجرد تعيين النطاقات المسموح بها؟

 استخدم ال`Protect` طريقة`Worksheet` كائن لحماية ورقة العمل. سيؤدي هذا إلى منع أي تغييرات خارج النطاقات المسموح بها، وربما المطالبة بكلمة مرور إذا قمت بتحديد واحدة.