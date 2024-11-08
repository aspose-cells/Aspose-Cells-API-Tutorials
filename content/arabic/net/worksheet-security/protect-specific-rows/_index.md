---
title: حماية صفوف محددة في ورقة العمل باستخدام Aspose.Cells
linktitle: حماية صفوف محددة في ورقة العمل باستخدام Aspose.Cells
second_title: واجهة برمجة تطبيقات معالجة Excel الخاصة بـ Aspose.Cells .NET
description: تعرف على كيفية حماية صفوف معينة في ورقة عمل Excel باستخدام Aspose.Cells for .NET من خلال هذا الدليل خطوة بخطوة. قم بتأمين بياناتك بفعالية.
type: docs
weight: 16
url: /ar/net/worksheet-security/protect-specific-rows/
---
## مقدمة
في هذا البرنامج التعليمي، سنرشدك خلال عملية حماية صفوف معينة في ورقة عمل Excel باستخدام Aspose.Cells for .NET. سنشرح كل خطوة بالتفصيل، ونغطي المتطلبات الأساسية، واستيراد الحزم المطلوبة، وتقسيم التعليمات البرمجية إلى تعليمات سهلة المتابعة. وبحلول النهاية، ستكون مجهزًا بالمعرفة اللازمة لتطبيق حماية الصفوف في تطبيقاتك الخاصة.
## المتطلبات الأساسية
قبل الغوص في التنفيذ، هناك بعض المتطلبات الأساسية التي يجب عليك تلبيتها لمتابعة هذا البرنامج التعليمي:
1. Aspose.Cells for .NET: ستحتاج إلى تثبيت Aspose.Cells for .NET. إذا لم تقم بتثبيته بعد، يمكنك الحصول على أحدث إصدار من خلال زيارة موقع Aspose على الويب.
2. فهم أساسي لـ C# و.NET: يفترض هذا البرنامج التعليمي أنك على دراية بـ C# ولديك معرفة أساسية ببرمجة .NET. إذا لم تكن على دراية بهذه، فقد ترغب في التحقق من بعض الموارد التمهيدية أولاً.
3. Visual Studio أو أي بيئة تطوير متكاملة لـ .NET: ستحتاج إلى بيئة تطوير متكاملة مثل Visual Studio لتشغيل التعليمات البرمجية. توفر هذه البيئة جميع الأدوات اللازمة وإمكانيات التصحيح.
4. ترخيص Aspose.Cells: إذا كنت تريد تجنب قيود الإصدار التجريبي، فتأكد من حصولك على ترخيص Aspose.Cells صالح. يمكنك أيضًا استخدام ترخيص مؤقت إذا كنت قد بدأت للتو.
 للحصول على معلومات مفصلة حول Aspose.Cells والتثبيت، يمكنك التحقق من[التوثيق](https://reference.aspose.com/cells/net/).
## استيراد الحزم
للبدء في استخدام Aspose.Cells، تحتاج إلى استيراد المساحات الأساسية اللازمة في مشروع C# الخاص بك. تتيح لك هذه المساحات الأساسية الوصول إلى الفئات والطرق المطلوبة للتعامل مع ملفات Excel.
إليك كيفية استيراد المساحات المطلوبة:
```csharp
using System.IO;
using Aspose.Cells;
```
تعتبر عمليات الاستيراد هذه بالغة الأهمية لأنها توفر الوصول إلى وظائف Aspose.Cells وتسمح لك بالتفاعل مع ملفات Excel في مشروع .NET الخاص بك.
الآن بعد أن قمت بإعداد المتطلبات الأساسية والاستيرادات اللازمة، حان الوقت للبدء في التعامل مع الكود الفعلي. سنقوم بتقسيم العملية إلى عدة خطوات لضمان الوضوح.
## الخطوة 1: إعداد دليل المشروع الخاص بك
في أي برنامج، يعد تنظيم الملفات أمرًا بالغ الأهمية. أولاً، دعنا ننشئ دليلًا يمكننا تخزين المصنف فيه. نتحقق من وجود الدليل وننشئه إذا لزم الأمر.
```csharp
// قم بتحديد المسار إلى دليل المستندات.
string dataDir = "Your Document Directory";
// إنشاء الدليل إذا لم يكن موجودًا بالفعل.
bool IsExists = System.IO.Directory.Exists(dataDir);
if (!IsExists)
    System.IO.Directory.CreateDirectory(dataDir);
```
هنا، يمكنك تحديد المسار الذي سيتم تخزين ملفات Excel فيه. إذا لم يكن المجلد موجودًا، فنحن نقوم بإنشائه. هذه الخطوة ضرورية لضمان وجود مكان لحفظ المصنف.
## الخطوة 2: إنشاء مصنف جديد
 بعد ذلك، نقوم بإنشاء مصنف جديد باستخدام`Workbook` توفر هذه الفئة كافة الوظائف المطلوبة للعمل مع ملفات Excel.
```csharp
// إنشاء مصنف جديد.
Workbook wb = new Workbook();
```
في هذه المرحلة، أصبح لدينا الآن كتاب عمل جديد للعمل عليه.
## الخطوة 3: الوصول إلى ورقة العمل
نصل الآن إلى ورقة العمل الأولى من المصنف الذي تم إنشاؤه حديثًا. يمكن أن يحتوي المصنف على أوراق عمل متعددة، ولكن في هذه الحالة، نركز على الورقة الأولى.
```csharp
// إنشاء كائن ورقة عمل والحصول على الورقة الأولى.
Worksheet sheet = wb.Worksheets[0];
```
 هنا،`Worksheets[0]` يشير إلى ورقة العمل الأولى في المصنف (والتي يتم فهرستها بدءًا من 0).
## الخطوة 4: إلغاء قفل جميع الأعمدة
في برنامج Excel، يتم تأمين الخلايا افتراضيًا عند حماية الورقة. إذا كنت تريد حماية صفوف معينة، فيجب عليك أولاً إلغاء تأمين الأعمدة. في هذه الخطوة، ننتقل عبر جميع الأعمدة ونقوم بإلغاء تأمينها.
```csharp
// تعريف كائن النمط.
Style style;
// تعريف كائن styleflag.
StyleFlag flag;
// قم بالمرور على جميع الأعمدة في ورقة العمل وإلغاء قفلها.
for (int i = 0; i <= 255; i++)
{
    style = sheet.Cells.Columns[(byte)i].Style;
    style.IsLocked = false;
    flag = new StyleFlag();
    flag.Locked = true;
    sheet.Cells.Columns[(byte)i].ApplyStyle(style, flag);
}
```
هنا، ننتقل عبر الأعمدة من 0 إلى 255 (إجمالي عدد الأعمدة في ورقة عمل Excel) ونقوم بإلغاء قفلها. وهذا يضمن إمكانية التفاعل مع الصفوف التي نريد حمايتها، بينما تظل الصفوف الأخرى مقفلة.
## الخطوة 5: قفل الصف الأول
الآن بعد أن تم إلغاء قفل جميع الأعمدة، يمكننا الانتقال إلى حماية الصفوف. في هذه الخطوة، نقوم بقفل الصف الأول، مما يجعله غير قابل للتعديل بمجرد حماية الورقة.
```csharp
//احصل على نمط الصف الأول.
style = sheet.Cells.Rows[0].Style;
// قفله.
style.IsLocked = true;
//إنشاء العلم.
flag = new StyleFlag();
// ضبط إعداد القفل.
flag.Locked = true;
// قم بتطبيق النمط على الصف الأول.
sheet.Cells.ApplyRowStyle(0, style, flag);
```
يقوم هذا الرمز بقفل الصف الأول، مما يضمن بقائه محميًا بمجرد تطبيق الحماية على الورقة.
## الخطوة 6: حماية ورقة العمل
في هذه المرحلة، نكون مستعدين لحماية ورقة العمل. تطبق هذه الخطوة إعدادات الحماية على ورقة العمل بأكملها، مع التأكد من عدم إمكانية تحرير أي خلايا مقفلة.
```csharp
// حماية الورقة.
sheet.Protect(ProtectionType.All);
```
 عن طريق استخدام`ProtectionType.All`نضمن أن جميع الخلايا، باستثناء الخلايا التي تم إلغاء قفلها صراحةً (مثل الأعمدة)، محمية. هذه هي الخطوة التي يتم بها تطبيق الحماية على ورقة العمل.
## الخطوة 7: حفظ ملف Excel
أخيرًا، بعد تطبيق الحماية، نقوم بحفظ المصنف. يمكنك تحديد التنسيق الذي تريد حفظ الملف به. في هذا المثال، نقوم بحفظ المصنف كملف Excel 97-2003.
```csharp
// احفظ ملف Excel.
wb.Save(dataDir + "output.out.xls", SaveFormat.Excel97To2003);
```
تؤدي هذه الخطوة إلى حفظ الملف في المسار المحدد، مما يكمل مهمة حماية صفوف محددة في ورقة العمل.
## خاتمة
إن حماية صفوف معينة في ورقة عمل Excel باستخدام Aspose.Cells for .NET هي عملية بسيطة بمجرد تقسيمها خطوة بخطوة. من خلال إلغاء قفل الأعمدة وقفل صفوف معينة وتطبيق إعدادات الحماية، فإنك تضمن أن تظل بياناتك آمنة وقابلة للتحرير فقط عند الضرورة. غطى هذا البرنامج التعليمي جميع الخطوات الرئيسية، من إعداد دليل المشروع الخاص بك إلى حفظ المصنف النهائي.
سواء كنت تقوم بإنشاء قوالب أو تقارير أو جداول بيانات تفاعلية، فإن استخدام حماية الصفوف يعد طريقة بسيطة وفعّالة للحفاظ على التحكم في بياناتك. جرّب هذه العملية في مشاريعك الخاصة واستكشف الإمكانات الكاملة لـ Aspose.Cells لـ .NET.
## الأسئلة الشائعة
### هل يمكنني حماية صفوف متعددة في ورقة العمل؟  
نعم، يمكنك تطبيق نفس خطوات الحماية على صفوف متعددة عن طريق تعديل الحلقة أو تطبيق الأنماط على صفوف أخرى.
### ماذا سيحدث إذا لم أقم بإلغاء قفل أي أعمدة قبل حماية الورقة؟  
إذا لم تقم بإلغاء قفل الأعمدة، فسيتم قفلها عند حماية الورقة، ولن يتمكن المستخدمون من التفاعل معها.
### كيف يمكنني فتح خلايا محددة بدلاً من الأعمدة بأكملها؟  
 يمكنك فتح خلايا معينة عن طريق الوصول إلى أسلوبها وتعيينه`IsLocked` الممتلكات ل`false`.
### هل يمكنني استخدام هذه الطريقة لحماية أوراق العمل بأكملها؟  
نعم، يمكنك حماية ورقة العمل بأكملها عن طريق تطبيق الحماية على جميع الخلايا وعدم ترك أي خلايا مفتوحة.
### كيف يمكنني إلغاء حماية ورقة العمل؟  
 يمكنك إزالة الحماية عن طريق الاتصال بـ`Unprotect`الطريقة الموجودة في ورقة العمل وتوفير كلمة مرور الحماية (إذا تم تعيين واحدة).