---
title: ضبط التنسيق التلقائي لجدول Pivot برمجيًا في .NET
linktitle: ضبط التنسيق التلقائي لجدول Pivot برمجيًا في .NET
second_title: واجهة برمجة تطبيقات معالجة Excel الخاصة بـ Aspose.Cells .NET
description: تعرف على كيفية تعيين التنسيق التلقائي لجداول البيانات المحورية في Excel برمجيًا باستخدام Aspose.Cells لـ .NET في هذا البرنامج التعليمي المفصل خطوة بخطوة.
type: docs
weight: 18
url: /ar/net/creating-and-configuring-pivot-tables/setting-auto-format/
---
## مقدمة
عندما يتعلق الأمر بتحليل البيانات، يمكن أن تكون الجداول المحورية في Excel بمثابة تغيير جذري. فهي تسمح لك بتلخيص البيانات وتحليلها ديناميكيًا، مما يساعدك على اكتساب رؤى يكاد يكون من المستحيل استخراجها يدويًا. ولكن ماذا لو كنت تريد أتمتة عملية تنسيق الجداول المحورية في .NET؟ هنا، سأوضح لك كيفية تعيين التنسيق التلقائي للجدول المحوري برمجيًا باستخدام مكتبة Aspose.Cells القوية لـ .NET.
في هذا الدليل، سنستكشف الأساسيات، ونستعرض المتطلبات الأساسية، ونستورد الحزم الضرورية، ثم ننتقل إلى برنامج تعليمي خطوة بخطوة لمساعدتك على تنسيق جداول البيانات المحورية مثل المحترفين. هل يبدو هذا جيدًا؟ دعنا نبدأ على الفور!
## المتطلبات الأساسية
قبل أن نبدأ، دعونا نتأكد من أن لديك كل ما تحتاجه للبدء:
1. بيئة تطوير .NET: تأكد من أن لديك نسخة عاملة من Visual Studio (أو أي بيئة تطوير متكاملة تدعم .NET).
2.  مكتبة Aspose.Cells: للعمل مع ملفات Excel بسلاسة، ستحتاج إلى تثبيت مكتبة Aspose.Cells. إذا لم تقم بذلك بعد، فيمكنك الحصول عليها من[صفحة التحميل](https://releases.aspose.com/cells/net/).
3. المعرفة الأساسية بلغة C#: ستساعدك المعرفة ببرمجة C# على فهم الخطوات بشكل أفضل.
4.  ملف Excel (قالب): ستحتاج إلى ملف قالب Excel للبدء به، والذي سيتم معالجته في مثالنا. من أجل التبسيط، يمكنك إنشاء ملف نموذجي باسم`Book1.xls`.
## استيراد الحزم
للبدء في استخدام Aspose.Cells في مشروعك، ستحتاج إلى استيراد الحزم اللازمة. إليك كيفية إعداد ذلك في مشروع .NET الخاص بك:
### إنشاء مشروع جديد
ابدأ بإنشاء مشروع .NET جديد في IDE المفضل لديك. 
### إضافة المراجع
تأكد من إضافة مرجع إلى مكتبة Aspose.Cells. إذا قمت بتنزيل المكتبة، فأضف ملفات DLL من عملية الاستخراج. إذا كنت تستخدم NuGet، فيمكنك ببساطة تشغيل:
```bash
Install-Package Aspose.Cells
```
### استيراد مساحات الأسماء
الآن، في ملف التعليمات البرمجية الخاص بك، ستحتاج إلى استيراد مساحة اسم Aspose.Cells. يمكنك القيام بذلك عن طريق إضافة السطر التالي في أعلى ملف C# الخاص بك:
```csharp
using System.IO;
using Aspose.Cells;
using System.Drawing;
using Aspose.Cells.Pivot;
```
بمجرد إكمال هذه الخطوات، ستكون جاهزًا لكتابة بعض التعليمات البرمجية!
الآن، دعنا نقسم الكود الذي قدمته إلى خطوات مفصلة مع توضيحات لما يفعله كل جزء. 
## الخطوة 1: قم بتحديد دليل المستندات الخاص بك
للبدء، تحتاج إلى تعيين المسار إلى دليل المستندات الذي توجد به ملفات Excel. في مثالنا، سنقوم بتعريفه على النحو التالي:
```csharp
string dataDir = "Your Document Directory";  // تعديل حسب الحاجة
```
 هذا الخط ينشئ متغير سلسلة`dataDir`الذي يحمل مسار الملف إلى مستنداتك. تأكد من استبدال`"Your Document Directory"` مع المسار الفعلي على نظامك.
## الخطوة 2: تحميل ملف القالب
بعد ذلك، قد ترغب في تحميل مصنف موجود يحتوي على جدول المحور الخاص بك:
```csharp
Workbook workbook = new Workbook(dataDir + "Book1.xls");
```
 يقوم هذا الخط بإنشاء خط جديد`Workbook` الكائن عن طريق تحميل ملف Excel المحدد. يجب أن يحتوي الملف على جدول محوري واحد على الأقل حتى تكون الخطوات اللاحقة فعالة.
## الخطوة 3: الوصول إلى ورقة العمل المطلوبة
حدد ورقة العمل التي تحتاج إلى العمل عليها للوصول إلى جدول البيانات المحوري. في هذه الحالة، سنحصل فقط على الورقة الأولى:
```csharp
int pivotIndex = 0;  // فهرس الجدول المحوري
Worksheet worksheet = workbook.Worksheets[0];
```
 هنا،`worksheet` يسترجع ورقة العمل الأولى من المصنف. يتم تعيين فهرس الجدول المحوري على`0`وهذا يعني أننا نقوم بالوصول إلى الجدول المحوري الأول في ورقة العمل تلك.
## الخطوة 4: تحديد موقع جدول المحور
بعد أن أصبحت ورقة العمل جاهزة، حان الوقت للوصول إلى جدولك المحوري:
```csharp
PivotTable pivotTable = worksheet.PivotTables[pivotIndex];
```
 يؤدي هذا إلى تهيئة ملف جديد`PivotTable` الكائن عن طريق الحصول على جدول المحور في الفهرس المحدد من ورقة العمل.
## الخطوة 5: تعيين خاصية التنسيق التلقائي
الآن نأتي إلى الجزء الأكثر أهمية: ضبط خيارات التنسيق التلقائي لجدولك المحوري.
```csharp
pivotTable.IsAutoFormat = true; // تمكين التنسيق التلقائي
```
 يتيح هذا الخط ميزة التنسيق التلقائي لجدول المحور. عند ضبطه على`true`سيقوم الجدول المحوري بتنسيق نفسه تلقائيًا استنادًا إلى الأنماط المحددة مسبقًا.
## الخطوة 6: اختر نوع تنسيق تلقائي محدد
سنرغب أيضًا في تحديد نمط التنسيق التلقائي الذي يجب أن يتبناه جدول البيانات المحوري. يحتوي Aspose.Cells على تنسيقات مختلفة يمكننا الاختيار من بينها. وإليك كيفية ضبطها:
```csharp
pivotTable.AutoFormatType = Aspose.Cells.Pivot.PivotTableAutoFormatType.Report5;
```
 باستخدام هذا السطر، نقوم بتعيين نوع تنسيق تلقائي محدد لجدول المحور.`Report5` هو مجرد مثال لنمط واحد؛ يمكنك الاختيار من بين مجموعة متنوعة من الخيارات اعتمادًا على احتياجاتك. 
## الخطوة 7: احفظ المصنف
وأخيرًا، لا تنس حفظ المصنف الخاص بك بعد إجراء كافة التغييرات:
```csharp
workbook.Save(dataDir + "output.xls");
```
 يحفظ هذا السطر من التعليمات البرمجية المصنف المعدل في ملف جديد يسمى`output.xls` في الدليل المحدد. تأكد من التحقق من هذا الملف لرؤية جدول البيانات المحوري الخاص بك بتنسيق جميل!
## خاتمة
تهانينا! لقد قمت للتو ببرمجة جدول بيانات محوري في Excel للتنسيق التلقائي باستخدام Aspose.Cells في .NET. لا توفر لك هذه العملية الوقت عند إعداد التقارير فحسب، بل تضمن أيضًا الاتساق في مظهر بياناتك مع كل تشغيل. باستخدام بضعة أسطر فقط من التعليمات البرمجية، يمكنك تحسين ملفات Excel بشكل كبير - تمامًا مثل الساحر الرقمي.
## الأسئلة الشائعة
### ما هو Aspose.Cells؟
Aspose.Cells عبارة عن مكتبة .NET قوية للتعامل مع ملفات Excel دون الحاجة إلى تثبيت Microsoft Excel.
### هل يمكنني تنسيق جداول محورية متعددة في مصنف؟
نعم، يمكنك التنقل عبر كائنات جدول محوري متعددة داخل المصنف الخاص بك لتنسيقها واحدًا تلو الآخر.
### هل هناك نسخة تجريبية مجانية متاحة لـ Aspose.Cells؟
 بالتأكيد! يمكنك البدء بإصدار تجريبي مجاني متاح[هنا](https://releases.aspose.com/).
### ماذا لو لم يتم تنسيق جدول المحور الخاص بي بشكل صحيح؟
تأكد من أن الجدول المحوري يتم الرجوع إليه بشكل صحيح وأن نوع التنسيق التلقائي موجود، وإلا فقد يعود إلى الإعدادات الافتراضية.
### هل يمكنني أتمتة هذه العملية باستخدام المهام المجدولة؟
نعم! من خلال دمج هذا الكود في مهمة مجدولة، يمكنك أتمتة إنشاء التقارير وتنسيقها بانتظام.