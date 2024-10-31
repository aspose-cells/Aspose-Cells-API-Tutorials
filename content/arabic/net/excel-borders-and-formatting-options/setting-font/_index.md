---
title: ضبط الخط برمجياً في Excel
linktitle: ضبط الخط برمجياً في Excel
second_title: واجهة برمجة تطبيقات معالجة Excel الخاصة بـ Aspose.Cells .NET
description: تعرف على كيفية تعيين الخط برمجيًا في Excel باستخدام Aspose.Cells for .NET. قم بتعزيز جداول البيانات الخاصة بك باستخدام خطوط أنيقة.
type: docs
weight: 11
url: /ar/net/excel-borders-and-formatting-options/setting-font/
---
## مقدمة
هل تبحث عن التعامل مع ملفات Excel ببراعة؟ أنت في المكان المناسب! Aspose.Cells for .NET هي مكتبة استثنائية تتيح للمطورين العمل مع جداول بيانات Excel دون عناء. إحدى المهام الشائعة في Excel هي ضبط أنماط الخطوط لخلايا معينة، وخاصةً عند التعامل مع التنسيق الشرطي. تخيل أنك قادر على تسليط الضوء على البيانات المهمة تلقائيًا، مما يجعل تقاريرك ليس وظيفية فحسب، بل وجذابة بصريًا أيضًا. يبدو رائعًا، أليس كذلك؟ دعنا نتعمق في كيفية تعيين أنماط الخطوط برمجيًا باستخدام Aspose.Cells for .NET.
## المتطلبات الأساسية
قبل أن نبدأ في كتابة التعليمات البرمجية، دعنا نتأكد من أن كل شيء جاهز. إليك ما ستحتاج إليه:
1. Visual Studio: تأكد من تثبيت إصدار Visual Studio لديك (يوصى باستخدام إصدار 2017 أو إصدار أحدث).
2.  Aspose.Cells لـ .NET: إذا لم تقم بتنزيل مكتبة Aspose.Cells بالفعل، يمكنك الحصول عليها من[موقع اسبوس](https://releases.aspose.com/cells/net/).
3. المعرفة الأساسية بلغة C#: ستكون المعرفة بلغة C# مفيدة لأننا سنكتب التعليمات البرمجية بهذه اللغة.
4. .NET Framework: تأكد من تثبيت إصدار متوافق مع .NET Framework.
بمجرد حصولك على هذه المتطلبات الأساسية، ستكون جاهزًا لبدء الترميز!
## استيراد الحزم
للبدء في استخدام Aspose.Cells، يتعين عليك استيراد الحزم اللازمة إلى مشروعك. إليك كيفية القيام بذلك:
1. افتح مشروع Visual Studio الخاص بك.
2. انقر بزر الماوس الأيمن على مشروعك في مستكشف الحلول وحدد "إدارة حزم NuGet".
3. ابحث عن "Aspose.Cells" وقم بتثبيته. سيؤدي هذا إلى إضافة المراجع الضرورية إلى مشروعك تلقائيًا.
بمجرد تثبيت الحزمة، يمكنك البدء في كتابة التعليمات البرمجية للتعامل مع ملفات Excel!
```csharp
using System.IO;
using Aspose.Cells;
using System.Drawing;
```
الآن، دعونا نقوم بتقسيم عملية تعيين أنماط الخطوط في ورقة Excel خطوة بخطوة.
## الخطوة 1: تحديد دليل المستندات
أولاً وقبل كل شيء، عليك تحديد الدليل الذي تريد حفظ ملف Excel فيه. هذا هو المكان الذي ستخزن فيه كل عملك الشاق، لذا اختر بحكمة! إليك كيفية القيام بذلك:
```csharp
// المسار إلى دليل المستندات.
string dataDir = "Your Document Directory";
```
 يستبدل`"Your Document Directory"` مع المسار الفعلي على نظامك. قد يكون هذا شيئًا مثل`@"C:\Documents\"` إذا كنت تعمل على نظام التشغيل Windows.
## الخطوة 2: إنشاء مثيل لكائن مصنف
 الآن بعد أن قمنا بإعداد الدليل، حان الوقت لإنشاء مصنف جديد. فكر في`Workbook` استخدم الكائن كلوحة قماشية فارغة يمكنك من خلالها رسم بياناتك. وإليك كيفية إنشائه:
```csharp
// إنشاء كائن مصنف
Workbook workbook = new Workbook();
```
## الخطوة 3: الوصول إلى ورقة العمل الأولى
 بعد ذلك، نحتاج إلى الوصول إلى ورقة العمل التي سنطبق عليها التنسيق. في المصنف الجديد، تكون ورقة العمل الأولى عادةً في الفهرس`0`. إليك كيفية القيام بذلك:
```csharp
Worksheet sheet = workbook.Worksheets[0];
```
## الخطوة 4: إضافة التنسيق الشرطي
الآن، دعنا نضفي بعض الإثارة على الأمر بإضافة التنسيق الشرطي. يتيح لك التنسيق الشرطي تطبيق التنسيق فقط عند استيفاء شروط معينة. وإليك كيفية إضافته:
```csharp
// يضيف تنسيقًا شرطيًا فارغًا
int index = sheet.ConditionalFormattings.Add();
FormatConditionCollection fcs = sheet.ConditionalFormattings[index];
```
من خلال إضافة التنسيق الشرطي، نقوم بإعداد أنفسنا لتطبيق الأنماط استنادًا إلى معايير محددة.
## الخطوة 5: تعيين نطاق التنسيق الشرطي
بعد ذلك، سنحدد نطاق الخلايا التي نريد تطبيق التنسيق الشرطي عليها. وهذا يشبه قول: "مرحبًا، أريد تطبيق قواعدي على هذه المنطقة". وإليك كيفية تحديد النطاق:
```csharp
// تعيين نطاق التنسيق الشرطي.
CellArea ca = new CellArea();
ca.StartRow = 0;
ca.EndRow = 5;
ca.StartColumn = 0;
ca.EndColumn = 3;
fcs.AddArea(ca);
```
في هذا المثال، نقوم بتنسيق الخلايا من A1 إلى D6 (فهرسة 0). اضبط هذه القيم حسب الحاجة لحالة الاستخدام الخاصة بك!
## الخطوة 6: إضافة شرط
الآن، دعنا نحدد الشرط الذي سيتم تطبيق التنسيق بموجبه. في هذه الحالة، نريد تنسيق الخلايا التي تحتوي على قيم تتراوح بين 50 و100. وإليك كيفية إضافة هذا الشرط:
```csharp
// يضيف الشرط.
int conditionIndex = fcs.AddCondition(FormatConditionType.CellValue, OperatorType.Between, "50", "100");
```
يقول هذا السطر بشكل أساسي، "إذا كانت قيمة الخلية بين 50 و100، فقم بتطبيق التنسيق الخاص بي."
## الخطوة 7: تعيين أنماط الخط
وهنا يأتي الجزء المثير! الآن، يمكننا تحديد أنماط الخطوط التي نريد تطبيقها على خلايانا. فلنجعل الخط مائلًا، وعريضًا، ومشطوبًا، ومُسطرًا، ونغير لونه. إليك الكود الذي سيفعل ذلك:
```csharp
// تعيين لون الخلفية.
FormatCondition fc = fcs[conditionIndex];
// fc.Style.BackgroundColor = Color.Red; // إلغاء التعليق لتعيين لون الخلفية
fc.Style.Font.IsItalic = true;
fc.Style.Font.IsBold = true;
fc.Style.Font.IsStrikeout = true;
fc.Style.Font.Underline = FontUnderlineType.Double;
fc.Style.Font.Color = Color.Black;
```
لا تتردد في تجربة هذه الأنماط! ربما تريد خلفية زاهية أو ألوانًا مختلفة؟ افعل ذلك!
## الخطوة 8: احفظ المصنف
أخيرًا، بعد الانتهاء من كل هذا العمل الشاق، لا تنس حفظ تحفتك الفنية! إليك كيفية حفظ مصنف العمل الخاص بك:
```csharp
workbook.Save(dataDir + "output.xlsx");
```
 يحفظ هذا السطر ملف Excel الخاص بك باسم`output.xlsx` في الدليل المحدد. تأكد من حصولك على أذونات الكتابة في هذا الموقع!
## خاتمة
والآن، لقد تعلمت كيفية تعيين أنماط الخطوط برمجيًا في Excel باستخدام Aspose.Cells for .NET. بدءًا من تحديد دليل المستندات الخاص بك إلى تطبيق التنسيق الشرطي وأخيرًا حفظ عملك، أصبحت لديك الآن الأدوات اللازمة لجعل ملفات Excel جذابة بصريًا وعملية.
سواء كنت تقوم بإنشاء التقارير أو أتمتة المهام أو إنشاء لوحات معلومات، فإن إتقان فن التعامل مع الخطوط يمكن أن يرفع مستوى جداول البيانات الخاصة بك من الأساسية إلى الجميلة.
## الأسئلة الشائعة
### هل يمكنني تطبيق أنماط الخطوط المختلفة على ظروف مختلفة؟  
بالتأكيد! يمكنك إضافة شروط متعددة وتحديد أنماط خطوط مختلفة لكل منها.
### ما هي أنواع الشروط التي يمكنني استخدامها في التنسيق الشرطي؟  
يمكنك استخدام أنواع مختلفة من الشروط، بما في ذلك قيم الخلايا والصيغ والمزيد. يوفر Aspose.Cells مجموعة غنية من الخيارات.
### هل استخدام Aspose.Cells مجاني؟  
 Aspose.Cells هو منتج تجاري، ولكن يمكنك تجربته مجانًا مع توفر نسخة تجريبية محدودة[هنا](https://releases.aspose.com/).
### هل يمكنني تنسيق صف كامل بناءً على قيمة خلية؟  
نعم! يمكنك ضبط التنسيق لصف أو عمود بأكمله استنادًا إلى قيمة خلية معينة باستخدام التنسيق الشرطي.
### أين يمكنني العثور على مزيد من المعلومات حول Aspose.Cells؟  
 يمكنك العثور على وثائق وموارد موسعة على[صفحة توثيق Aspose.Cells](https://reference.aspose.com/cells/net/).