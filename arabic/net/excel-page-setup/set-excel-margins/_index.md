---
title: قم بتعيين هوامش Excel
linktitle: قم بتعيين هوامش Excel
second_title: Aspose.Cells لمرجع .NET API
description: تعرف على كيفية تعيين الهوامش في Excel باستخدام Aspose.Cells for .NET. تعليمي خطوة بخطوة في C #.
type: docs
weight: 110
url: /ar/net/excel-page-setup/set-excel-margins/
---
في هذا البرنامج التعليمي ، سنرشدك خطوة بخطوة حول كيفية تعيين الهوامش في Excel باستخدام Aspose.Cells for .NET. سوف نستخدم كود المصدر C # لتوضيح العملية.

## الخطوة الأولى: تهيئة البيئة

تأكد من تثبيت Aspose.Cells for .NET على جهازك. قم أيضًا بإنشاء مشروع جديد في بيئة التطوير المفضلة لديك.

## الخطوة 2: استيراد المكتبات الضرورية

في ملف التعليمات البرمجية الخاص بك ، قم باستيراد المكتبات اللازمة للعمل مع Aspose.Cells. هذا هو الكود المقابل:

```csharp
using Aspose.Cells;
```

## الخطوة 3: تعيين دليل البيانات

قم بتعيين دليل البيانات حيث تريد حفظ ملف Excel المعدل. استخدم الكود التالي:

```csharp
string dataDir = "YOUR DATA DIRECTORY";
```

تأكد من تحديد مسار الدليل الكامل.

## الخطوة 4: إنشاء المصنف وورقة العمل

قم بإنشاء كائن مصنف جديد وانتقل إلى ورقة العمل الأولى في المصنف باستخدام التعليمات البرمجية التالية:

```csharp
Workbook workbook = new Workbook();
WorksheetCollection worksheets = workbook. Worksheets;
Worksheet worksheet = worksheets[0];
```

سيؤدي هذا إلى إنشاء مصنف فارغ بورقة عمل وتوفير الوصول إلى ورقة العمل هذه.

## الخطوة 5: ضبط الهوامش

قم بالوصول إلى كائن PageSetup الخاص بورقة العمل وقم بتعيين الهوامش باستخدام خصائص BottomMargin و LeftMargin و RightMargin و TopMargin. إليك نموذج التعليمات البرمجية:

```csharp
PageSetup pageSetup = worksheet.PageSetup;
pageSetup.BottomMargin = 2;
pageSetup.LeftMargin = 1;
pageSetup.RightMargin = 1;
pageSetup.TopMargin = 3;
```

سيؤدي هذا إلى تعيين الهوامش السفلية واليسرى واليمنى والعليا لورقة العمل على التوالي.

## الخطوة 6: حفظ المصنف المعدل

احفظ المصنف المعدل باستخدام الكود التالي:

```csharp
workbook.Save(dataDir + "OutputFileName.xls");
```

سيؤدي هذا إلى حفظ المصنف المعدل في دليل البيانات المحدد.

### نموذج التعليمات البرمجية المصدر لتعيين هوامش Excel باستخدام Aspose.Cells لـ .NET 
```csharp
// المسار إلى دليل المستندات.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// قم بإنشاء كائن مصنف
Workbook workbook = new Workbook();
// احصل على أوراق العمل في المصنف
WorksheetCollection worksheets = workbook.Worksheets;
// احصل على أول ورقة عمل (افتراضية)
Worksheet worksheet = worksheets[0];
// احصل على كائن pagesetup
PageSetup pageSetup = worksheet.PageSetup;
// تعيين هوامش الصفحة السفلية واليسرى واليمنى والعليا
pageSetup.BottomMargin = 2;
pageSetup.LeftMargin = 1;
pageSetup.RightMargin = 1;
pageSetup.TopMargin = 3;
// احفظ المصنف.
workbook.Save(dataDir + "SetMargins_out.xls");
```

## خاتمة

لقد تعلمت الآن كيفية تعيين الهوامش في Excel باستخدام Aspose.Cells لـ .NET. يرشدك هذا البرنامج التعليمي خلال كل خطوة من خطوات العملية ، من إعداد البيئة إلى حفظ المصنف المعدل. لا تتردد في استكشاف المزيد من ميزات Aspose.Cells لإجراء مزيد من التلاعب في ملفات Excel الخاصة بك.

### التعليمات (الأسئلة المتداولة)

#### 1. كيف يمكنني تحديد هوامش مخصصة لجدول البيانات الخاص بي؟

 يمكنك تحديد هوامش مخصصة باستخدام امتداد`BottomMargin`, `LeftMargin`, `RightMargin` ، و`TopMargin` خصائص`PageSetup` هدف. ما عليك سوى تعيين القيم المرغوبة لكل خاصية لضبط الهوامش حسب الحاجة.

#### 2. هل يمكنني تعيين هوامش مختلفة لأوراق عمل مختلفة في نفس المصنف؟

 نعم ، يمكنك تعيين هوامش مختلفة لكل ورقة عمل في نفس المصنف. فقط قم بالوصول إلى`PageSetup` كائن من كل ورقة عمل على حدة وتعيين الهوامش المحددة لكل منها.

#### 3. هل تنطبق الهوامش المحددة أيضًا على طباعة المصنف؟

نعم ، الهوامش المعينة باستخدام Aspose.Cells تنطبق أيضًا عند طباعة المصنف. ستؤخذ الهوامش المحددة في الاعتبار عند إنشاء الإخراج المطبوع للمصنف.

#### 4. هل يمكنني تغيير هوامش ملف Excel موجود باستخدام Aspose.Cells؟

 نعم ، يمكنك تغيير هوامش ملف Excel الحالي عن طريق تحميل الملف باستخدام Aspose.Cells ، والوصول إلى كل ورقة عمل.`PageSetup` الكائن ، وتغيير قيم خصائص الهوامش. ثم احفظ الملف المعدل لتطبيق الهوامش الجديدة.

#### 5. كيف يمكنني إزالة الهوامش من جدول بيانات؟

 لإزالة الهوامش من ورقة عمل ، يمكنك ببساطة تعيين قيم ملف`BottomMargin`, `LeftMargin`, `RightMargin` و`TopMargin` خصائص إلى الصفر. سيؤدي هذا إلى إعادة تعيين الهوامش إلى الافتراضي (عادةً صفر).