---
title: تحرير النطاقات في ورقة عمل Excel
linktitle: تحرير النطاقات في ورقة عمل Excel
second_title: Aspose.Cells لمرجع .NET API
description: تعلم كيفية تحرير نطاقات معينة في جدول بيانات Excel باستخدام Aspose.Cells لـ .NET. البرنامج التعليمي خطوة بخطوة في C#.
type: docs
weight: 20
url: /ar/net/protect-excel-file/edit-ranges-in-excel-worksheet/
---
يعد Microsoft Excel أداة قوية لإنشاء جداول البيانات وإدارتها، حيث يقدم العديد من الميزات للتحكم في البيانات وتأمينها. إحدى هذه الميزات هي السماح للمستخدمين بتحرير نطاقات معينة في ورقة العمل مع حماية الأجزاء الأخرى. في هذا البرنامج التعليمي، سنرشدك خطوة بخطوة لتنفيذ هذه الوظيفة باستخدام Aspose.Cells for .NET، وهي مكتبة شائعة للعمل مع ملفات Excel برمجيًا.

سيسمح لك استخدام Aspose.Cells for .NET بمعالجة النطاقات في جدول بيانات Excel بسهولة، مما يوفر واجهة سهلة الاستخدام وميزات متقدمة. اتبع الخطوات الموضحة أدناه للسماح للمستخدمين بتحرير نطاقات محددة في جدول بيانات Excel باستخدام Aspose.Cells for .NET.
## الخطوة 1: تهيئة البيئة

تأكد من تثبيت Aspose.Cells for .NET في بيئة التطوير الخاصة بك. قم بتنزيل المكتبة من موقع Aspose الرسمي وتحقق من الوثائق للحصول على تعليمات التثبيت.

## الخطوة 2: تهيئة المصنف وورقة العمل

للبدء، نحتاج إلى إنشاء مصنف جديد والحصول على المرجع إلى ورقة العمل حيث نريد السماح بتغيير النطاقات. استخدم الكود التالي لتحقيق ذلك:

```csharp
// المسار إلى دليل المستندات.
string dataDir = "YOUR DOCUMENTS DIRECTORY";
// قم بإنشاء الدليل إذا لم يكن موجودًا بالفعل.
bool exists = System.IO.Directory.Exists(dataDir);
if (! exists)
     System.IO.Directory.CreateDirectory(dataDir);

// إنشاء مثيل لمصنف جديد
Workbook workbook = new Workbook();

// الحصول على ورقة العمل الأولى (افتراضي)
Worksheet sheet = workbook.Worksheets[0];
```

 في مقتطف التعليمات البرمجية هذا، نحدد أولاً المسار إلى الدليل الذي سيتم حفظ ملف Excel فيه. بعد ذلك، نقوم بإنشاء مثيل جديد من`Workbook` class واحصل على المرجع إلى ورقة العمل الأولى باستخدام ملف`Worksheets` ملكية.

## الخطوة 3: احصل على نطاقات قابلة للتحرير

نحتاج الآن إلى استرداد النطاقات التي نريد السماح بالتعديل فيها. استخدم الكود التالي:

```csharp
// احصل على النطاقات القابلة للتعديل
ProtectedRangeCollection EditableRanges = Sheet.AllowEditRanges;
```

## الخطوة 4: تعيين النطاق المحمي

قبل السماح بتعديل النطاقات، نحتاج إلى تحديد نطاق محمي. إليك الطريقة:

```csharp
// تحديد نطاق محمي
ProtectedRange ProtectedRange;

// قم بإنشاء النطاق
int index = ModifiableRanges.Add("r2", 1, 1, 3, 3);
rangeProtected = rangesEditable[index];
```

 في هذا الكود، قمنا بإنشاء مثيل جديد لـ`ProtectedRange` الصف واستخدام`Add` طريقة تحديد النطاق المراد حمايته.

## الخطوة 5: تحديد كلمة المرور

لتعزيز الأمان، يمكنك تحديد كلمة مرور للنطاق المحمي. إليك الطريقة:

```csharp
// تحديد كلمة المرور
protectedBeach.Password = "YOUR_PASSWORD";
```

## الخطوة 6: حماية ورقة العمل

الآن بعد أن قمنا بتعيين النطاق المحمي، يمكننا حماية ورقة العمل لمنع التعديل غير المصرح به. استخدم الكود التالي:

```csharp
// حماية ورقة العمل
leaf.Protect(ProtectionType.All);
```

## الخطوة 7: احفظ ملف Excel

وأخيرا، نقوم بحفظ ملف Excel مع التغييرات التي تم إجراؤها. هنا هو الكود الضروري:

```csharp
// احفظ ملف إكسل
workbook.Save(dataDir + "protectedrange.out.xls");
```

### نموذج التعليمات البرمجية المصدر لتحرير النطاقات في ورقة عمل Excel باستخدام Aspose.Cells لـ .NET 
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
proteced_range.Password = "YOUR_PASSWORD";

// حماية الورقة
sheet.Protect(ProtectionType.All);

// احفظ ملف إكسل
book.Save(dataDir + "protectedrange.out.xls");
```

## خاتمة

تهنئة ! لقد تعلمت كيفية السماح للمستخدمين بتحرير نطاقات معينة في جدول بيانات Excel باستخدام Aspose.Cells لـ .NET. يمكنك الآن تطبيق هذه التقنية في مشاريعك الخاصة وتحسين أمان ملفات Excel الخاصة بك.


#### الأسئلة الشائعة

#### س: لماذا يجب علي استخدام Aspose.Cells لـ .NET لتحرير النطاقات في جدول بيانات Excel؟

ج: يوفر Aspose.Cells for .NET واجهة برمجة تطبيقات قوية وسهلة الاستخدام للعمل مع ملفات Excel. فهو يوفر ميزات متقدمة، مثل معالجة النطاق وحماية ورقة العمل وما إلى ذلك.

#### س: هل يمكنني تعيين نطاقات متعددة قابلة للتحرير في ورقة العمل؟

 ج: نعم، يمكنك تحديد نطاقات متعددة قابلة للتحرير باستخدام`Add` طريقة`ProtectedRangeCollection` مجموعة. يمكن أن يكون لكل نطاق إعدادات الحماية الخاصة به.

####  س: هل من الممكن حذف نطاق قابل للتحرير بعد تحديده؟

 ج: نعم، يمكنك استخدام`RemoveAt` طريقة`ProtectedRangeCollection` مجموعة لإزالة نطاق محدد قابل للتحرير عن طريق تحديد فهرسه.

#### س: كيف يمكنني فتح ملف Excel المحمي بعد حفظه؟

ج: سوف تحتاج إلى توفير كلمة المرور المحددة عند إنشاء النطاق المحمي لفتح ملف Excel المحمي. تأكد من الاحتفاظ بكلمة المرور في مكان آمن لمنع فقدان الوصول إلى البيانات.