---
title: تحويل CSV إلى JSON برمجيًا في .NET
linktitle: تحويل CSV إلى JSON برمجيًا في .NET
second_title: واجهة برمجة تطبيقات معالجة Excel الخاصة بـ Aspose.Cells .NET
description: تعرف على كيفية تحويل CSV إلى JSON في .NET باستخدام Aspose.Cells. دليل خطوة بخطوة لتحويل البيانات مع أمثلة أكواد سهلة المتابعة.
type: docs
weight: 10
url: /ar/net/converting-excel-files-to-other-formats/converting-csv-to-json/
---
## مقدمة
في هذا البرنامج التعليمي، سنوضح لك عملية تحويل ملف CSV إلى تنسيق JSON باستخدام Aspose.Cells for .NET. وسنقسم كل شيء إلى خطوات سهلة المتابعة حتى تتمكن من دمج هذه الوظيفة في مشروعك بسرعة.
## المتطلبات الأساسية
قبل الغوص في الكود، تأكد من توفر المتطلبات الأساسية التالية:
1.  Aspose.Cells for .NET: يجب أن يكون لديك Aspose.Cells مثبتًا في مشروعك. إذا لم تكن قد قمت بذلك بالفعل، فيمكنك تنزيله[هنا](https://releases.aspose.com/cells/net/).
2. .NET Framework أو .NET Core: تأكد من تثبيت إصدار متوافق من .NET.
3. ملف CSV: ملف CSV نموذجي تريد تحويله إلى JSON.
## استيراد الحزم
قبل البدء في الترميز، من المهم استيراد مساحات الأسماء الضرورية من Aspose.Cells. سيتيح لك ذلك تحميل البيانات ومعالجتها وتصديرها بتنسيقات مختلفة.
```csharp
using Aspose.Cells.Utility;
using System;
using System.IO;
```
دعونا نحلل هذا الأمر خطوة بخطوة، حتى تعرف بالضبط كيف تسير العملية.
## الخطوة 1: تحميل ملف CSV
 الخطوة الأولى هي تحميل ملف CSV الخاص بك إلى`Workbook` هذا هو المكان الذي يتميز فيه Aspose.Cells. فهو يعامل ملفات CSV مثل أي جدول بيانات آخر، مما يمنحك المرونة في التعامل مع البيانات.
### الخطوة 1.1: تحديد دليل المصدر
سوف تحتاج إلى تحديد مكان ملف CSV الخاص بك. سيتم استخدام هذا الدليل لتحميل الملف.
```csharp
string sourceDir = "Your Document Directory";
```
تشير مهمة السلسلة البسيطة هذه إلى المجلد الذي يوجد به ملف CSV الخاص بك.
### الخطوة 1.2: تعيين خيارات التحميل لتنسيق CSV
 بعد ذلك، نحدد كيفية تعامل Aspose.Cells مع تنسيق الملف. ملفات CSV هي نوع محدد من ملفات النصوص، لذا نقوم بتعيين`LoadFormat` ل`Csv` استخدام`LoadOptions`.
```csharp
LoadOptions loadOptions = new LoadOptions(LoadFormat.Csv);
```
يضمن هذا أنه عند تحميل الملف، يعامله Aspose.Cells كملف CSV وليس جدول بيانات Excel التقليدي.
### الخطوة 1.3: تحميل ملف CSV في مصنف
 الآن، قم بتحميل ملف CSV إلى`Workbook`فكر في المصنف باعتباره حاوية بياناتك، والتي تحتوي على محتويات ملف CSV.
```csharp
Workbook workbook = new Workbook(sourceDir + "SampleCsv.csv", loadOptions);
```
الآن أصبح المصنف جاهزًا للتعامل معه، ويحتوي على الصفوف والأعمدة من ملف CSV الخاص بك.
## الخطوة 2: تحديد الخلية الأخيرة في ورقة العمل
لتحويل البيانات إلى JSON، تحتاج إلى معرفة مقدار البيانات الموجودة في ملف CSV. للقيام بذلك، نحتاج إلى تحديد آخر خلية مملوءة في ورقة العمل.
```csharp
Cell lastCell = workbook.Worksheets[0].Cells.LastCell;
```
يحدد هذا الخلية الأخيرة التي تحتوي على البيانات في ورقة العمل الأولى من المصنف المحمّل بملف CSV.
## الخطوة 3: تحديد نطاق البيانات المراد تصديرها
يتعين عليك إخبار Aspose.Cells بنطاق البيانات المطلوب تصديره. في هذه الحالة، ستحدد نطاق البيانات بالكامل من الخلية الأولى إلى الخلية الأخيرة التي تم تحديدها سابقًا.
### الخطوة 3.1: تعيين خيارات التصدير لـ JSON
 نحن نستخدم`ExportRangeToJsonOptions` لتحديد كيفية تصدير البيانات. يمكنك تخصيص ذلك بشكل أكبر إذا لزم الأمر، ولكن في الوقت الحالي، سنلتزم بالخيارات الافتراضية.
```csharp
ExportRangeToJsonOptions options = new ExportRangeToJsonOptions();
```
### الخطوة 3.2: إنشاء نطاق البيانات
يتم تحديد نطاق البيانات عن طريق تحديد الصف والعمود البدئيين (كلاهما 0)، والصف والعمود النهائيين استنادًا إلى موضع الخلية الأخيرة.
```csharp
Range range = workbook.Worksheets[0].Cells.CreateRange(0, 0, lastCell.Row + 1, lastCell.Column + 1);
```
يغطي هذا النطاق بيانات CSV بأكملها، جاهزة للتصدير.
## الخطوة 4: تحويل النطاق إلى JSON
 بعد تحديد نطاق البيانات، فإن الخطوة التالية هي تحويل هذا النطاق إلى JSON باستخدام`JsonUtility.ExportRangeToJson()` طريقة.
```csharp
string data = JsonUtility.ExportRangeToJson(range, options);
```
ستقوم هذه الوظيفة باستخراج البيانات من النطاق المحدد وتحويلها إلى سلسلة JSON.
## الخطوة 5: إخراج بيانات JSON
أخيرًا، يمكنك طباعة بيانات JSON أو معالجتها بشكل أكبر حسب الحاجة. وللتبسيط، سنخرج بيانات JSON إلى وحدة التحكم.
```csharp
Console.WriteLine(data);
```
## خاتمة
إن تحويل ملف CSV إلى JSON في .NET باستخدام Aspose.Cells عملية سهلة ومباشرة. من خلال الاستفادة من إمكانيات معالجة البيانات القوية في Aspose.Cells، يمكنك بسهولة تصدير تنسيقات البيانات المعقدة مثل CSV إلى تنسيقات أكثر ملاءمة للويب مثل JSON. وهذا مثالي لخدمات الويب أو تكامل واجهة برمجة التطبيقات أو أي سيناريو حيث تكون بيانات JSON مفضلة.
## الأسئلة الشائعة
### هل يمكن لـ Aspose.Cells التعامل مع ملفات CSV كبيرة الحجم لتحويلها إلى JSON؟  
نعم، تم تحسين Aspose.Cells لتحسين الأداء ويمكنه التعامل مع مجموعات البيانات الكبيرة بكفاءة. يمكنك العمل مع ملفات CSV التي تحتوي على آلاف الصفوف دون التعرض لمشكلات تتعلق بالأداء.
### هل من الممكن تنسيق مخرجات JSON بطريقة معينة؟  
 نعم،`ExportRangeToJsonOptions` تتيح لك الفئة تخصيص كيفية هيكلة بيانات JSON، مما يتيح لك التحكم في أشياء مثل تضمين الرؤوس والتنسيق والمزيد.
### هل أحتاج إلى ترخيص لاستخدام Aspose.Cells لهذا التحويل؟  
 يمكنك تجربة Aspose.Cells مع[نسخة تجريبية مجانية](https://releases.aspose.com/) أو التقدم بطلب للحصول على[رخصة مؤقتة](https://purchase.aspose.com/temporary-license/) إذا كنت تريد استكشاف إمكانياته الكاملة دون شرائه.
### هل يمكنني تحويل صيغ أخرى مثل Excel إلى JSON باستخدام نفس النهج؟  
بالتأكيد! يدعم Aspose.Cells تنسيقات مختلفة، بما في ذلك Excel (XLSX، XLS)، ويمكنك استخدام عملية مماثلة لتحويلها إلى JSON.
### هل يدعم Aspose.Cells تحويل البيانات من JSON إلى CSV أو Excel؟  
نعم، يوفر Aspose.Cells مرونة كاملة ليس فقط لتصدير البيانات إلى JSON ولكن أيضًا لاستيراد البيانات من JSON، مما يسمح لك بتحويل البيانات بين التنسيقات بسهولة.