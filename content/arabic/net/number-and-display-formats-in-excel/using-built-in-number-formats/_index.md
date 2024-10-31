---
title: استخدام تنسيقات الأرقام المضمنة في برنامج Excel برمجيًا
linktitle: استخدام تنسيقات الأرقام المضمنة في برنامج Excel برمجيًا
second_title: واجهة برمجة تطبيقات معالجة Excel الخاصة بـ Aspose.Cells .NET
description: أتمتة تنسيق الأرقام في Excel باستخدام Aspose.Cells for .NET. تعرف على كيفية تطبيق تنسيقات التاريخ والنسبة المئوية والعملة برمجيًا.
type: docs
weight: 10
url: /ar/net/number-and-display-formats-in-excel/using-built-in-number-formats/
---
## مقدمة
في هذا البرنامج التعليمي، سنوضح لك كيفية استخدام تنسيقات الأرقام المضمنة في Excel باستخدام Aspose.Cells for .NET. سنغطي كل شيء بدءًا من إعداد البيئة الخاصة بك إلى تطبيق تنسيقات مختلفة مثل التواريخ والنسب المئوية والعملات. سواء كنت محترفًا متمرسًا أو كنت تخوض تجربة جديدة في بيئة .NET، فإن هذا الدليل سيساعدك على تنسيق خلايا Excel بسهولة.
## المتطلبات الأساسية
قبل الغوص، تأكد من أن لديك ما يلي:
-  تم تثبيت مكتبة Aspose.Cells لـ .NET. يمكنك[تحميله هنا](https://releases.aspose.com/cells/net/).
- معرفة عملية بلغة C# وبرمجة .NET الأساسية.
- Visual Studio أو أي .NET IDE مثبت على جهازك.
-  ترخيص Aspose صالح أو[رخصة مؤقتة](https://purchase.aspose.com/temporary-license/).
- تم تثبيت إطار عمل .NET (الإصدار 4.0 أو أعلى).
  
إذا كنت تفتقد أيًا مما سبق، فاتبع الروابط المقدمة لإعداد كل شيء. هل أنت مستعد؟ دعنا ننتقل إلى الجزء الممتع!
## استيراد الحزم
قبل أن نبدأ بالبرنامج التعليمي، تأكد من استيراد المساحات الأساسية اللازمة للعمل مع Aspose.Cells لـ .NET:
```csharp
using System.IO;
using Aspose.Cells;
using System;
```
بمجرد استيراد هذه الملفات، تصبح جاهزًا للتعامل مع ملفات Excel برمجيًا. الآن، دعنا ننتقل إلى الدليل خطوة بخطوة!
## الخطوة 1: إنشاء مصنف Excel أو الوصول إليه
في هذه الخطوة، ستقوم بإنشاء مصنف جديد. فكر في هذا الأمر كما لو كنت تفتح ملف Excel جديدًا، إلا أنك تفعل ذلك من خلال الكود!
```csharp
// المسار إلى دليل المستندات.
string dataDir = "Your Document Directory";
// إنشاء الدليل إذا لم يكن موجودًا بالفعل.
bool IsExists = System.IO.Directory.Exists(dataDir);
if (!IsExists)
	System.IO.Directory.CreateDirectory(dataDir);
// إنشاء كائن مصنف
Workbook workbook = new Workbook();
```
 هنا، نقوم ببساطة بإنشاء مثيل جديد`Workbook` الكائن. يعمل هذا كملف Excel الخاص بك، جاهزًا لمعالجة البيانات. يمكنك أيضًا تحميل ملف موجود من خلال توفير مساره.
## الخطوة 2: الوصول إلى ورقة العمل
يمكن أن تحتوي مصنفات Excel على أوراق عمل متعددة. في هذه الخطوة، سنتمكن من الوصول إلى ورقة العمل الأولى في المصنف الخاص بك:
```csharp
Worksheet worksheet = workbook.Worksheets[0];
```
نقوم الآن بالوصول إلى ورقة العمل الأولى في المصنف. إذا كنت بحاجة إلى معالجة أوراق عمل إضافية، فيمكنك الرجوع إليها باستخدام الفهرس أو الاسم الخاص بها.
## الخطوة 3: إضافة البيانات إلى الخلايا
لنبدأ بإضافة بعض البيانات إلى خلايا معينة. أولاً، سنقوم بإدراج تاريخ النظام الحالي في الخلية "A1":
```csharp
worksheet.Cells["A1"].PutValue(DateTime.Now);
```
يقوم هذا السطر بإدراج التاريخ الحالي في الخلية A1. إنه أمر رائع، أليس كذلك؟ تخيل القيام بذلك يدويًا لمئات الخلايا - سيكون الأمر بمثابة كابوس. الآن، سننتقل إلى التنسيق!
## الخطوة 4: تنسيق التاريخ في الخلية "A1"
بعد ذلك، دعنا ننسق هذا التاريخ بتنسيق أكثر قابلية للقراءة، مثل "15-Oct-24". وهنا تبرز ميزة Aspose.Cells حقًا:
1. استرداد نمط الخلية:
```csharp
Style style = worksheet.Cells["A1"].GetStyle();
```
هنا، نلتقط نمط الخلية A1. فكر في هذا الأمر باعتباره التقاط "نمط" الخلية قبل إجراء أي تعديلات.
2. تعيين تنسيق التاريخ:
```csharp
style.Number = 15;
```
 ضبط`Number` تطبق الخاصية 15 تنسيق التاريخ المطلوب. هذا هو رمز تنسيق رقمي مدمج لعرض التواريخ بتنسيق "d-mmm-yy".
3. تطبيق النمط على الخلية:
```csharp
worksheet.Cells["A1"].SetStyle(style);
```
يطبق هذا السطر تغييرات النمط على الخلية. الآن، بدلاً من تنسيق التاريخ الافتراضي، سترى شيئًا أكثر سهولة في الاستخدام مثل "15-Oct-24".
## الخطوة 5: إضافة وتنسيق النسبة المئوية في الخلية "A2"
لننتقل الآن إلى تنسيق النسب المئوية. تخيل أنك تريد إدراج قيمة وعرضها كنسبة مئوية. في هذه الخطوة، سنضيف قيمة رقمية إلى الخلية "A2" وننسقها كنسبة مئوية:
1. إدراج قيمة رقمية:
```csharp
worksheet.Cells["A2"].PutValue(20);
```
يؤدي هذا إلى إدراج الرقم 20 في الخلية A2. قد تتساءل، "هذا مجرد رقم عادي - كيف أحوله إلى نسبة مئوية؟" حسنًا، نحن على وشك الوصول إلى هذه النقطة.
2. استرداد النمط وتعيين تنسيق النسبة المئوية:
```csharp
style = worksheet.Cells["A2"].GetStyle();
style.Number = 9;  // التنسيق كنسبة مئوية
worksheet.Cells["A2"].SetStyle(style);
    ```
Setting the `Number` property to 9 applies the built-in percentage format. Now the value in A2 will be displayed as "2000%." (Yes, 20 is treated as 2000% in percentage formatting).
## Step 6: Add and Format Currency in Cell "A3"
Now, let’s add a numeric value in cell A3 and format it as currency. This is a common use case for financial reports.
1. Insert Numeric Value:
```csharp
worksheet.Cells["A3"].PutValue(2546);
```
هنا، نضيف 2546 إلى الخلية A3. بعد ذلك، سنقوم بتنسيق هذا الرقم ليظهر كعملة.
2. استرداد النمط وتعيين تنسيق العملة:
```csharp
style = worksheet.Cells["A3"].GetStyle();
style.Number = 6;  // تنسيق كعملة
worksheet.Cells["A3"].SetStyle(style);
```
 ضبط`Number` تطبق الخاصية 6 تنسيق العملة. الآن سيتم عرض القيمة في الخلية A3 على أنها "2,546.00"، مع وضع الفواصل ورقمين عشريين.
## الخطوة 7: حفظ ملف Excel
الآن بعد أن قمنا بتطبيق كل سحر التنسيق، حان الوقت لحفظ الملف:
```csharp
// حفظ ملف Excel
workbook.Save(dataDir + "book1.out.xls", SaveFormat.Excel97To2003);
```
 يحفظ هذا السطر ملف Excel بتنسيق Excel 97-2003. يمكنك تغيير`SaveFormat`لتناسب احتياجاتك. وهكذا تكون قد أنشأت ملف Excel ونسقته برمجيًا!
## خاتمة
تهانينا! لقد نجحت في تعلم كيفية استخدام Aspose.Cells for .NET لتطبيق تنسيقات الأرقام المضمنة على الخلايا في ملف Excel. بدءًا من التواريخ إلى النسب المئوية والعملات، قمنا بتغطية بعض احتياجات التنسيق الأكثر شيوعًا لمعالجة بيانات Excel. الآن، بدلاً من تنسيق الخلايا يدويًا، يمكنك أتمتة العملية بالكامل - مما يوفر لك الوقت ويقلل من الأخطاء.
## الأسئلة الشائعة
### هل يمكنني تطبيق تنسيقات الأرقام المخصصة باستخدام Aspose.Cells لـ .NET؟
 نعم! بالإضافة إلى التنسيقات المضمنة، يدعم Aspose.Cells أيضًا تنسيقات الأرقام المخصصة. يمكنك إنشاء تنسيقات محددة للغاية باستخدام`Custom` الممتلكات في`Style` فصل.
### كيف يمكنني تنسيق خلية كعملة برمز محدد؟
 لتطبيق رمز عملة محدد، يمكنك استخدام التنسيق المخصص عن طريق ضبط`Style.Custom` ملكية.
### هل يمكنني تنسيق الصفوف أو الأعمدة بأكملها؟
 بالتأكيد! يمكنك تطبيق الأنماط على الصفوف أو الأعمدة بأكملها باستخدام`Rows` أو`Columns`المجموعات في`Worksheet` هدف.
### كيف يمكنني تنسيق خلايا متعددة في وقت واحد؟
يمكنك استخدام`Range` كائن لتحديد خلايا متعددة وتطبيق الأنماط عليها جميعًا مرة واحدة.
### هل أحتاج إلى تثبيت Microsoft Excel لاستخدام Aspose.Cells؟
لا، يعمل Aspose.Cells بشكل مستقل عن Microsoft Excel، لذا لا تحتاج إلى تثبيت Excel على جهازك.