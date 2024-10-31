---
title: تدوير النص وتغيير اتجاهه في Excel
linktitle: تدوير النص وتغيير اتجاهه في Excel
second_title: واجهة برمجة تطبيقات معالجة Excel الخاصة بـ Aspose.Cells .NET
description: قم بتحويل اتجاه النص في Excel باستخدام Aspose.Cells for .NET. اتبع دليلنا خطوة بخطوة لتدوير النص وتعديله بسهولة.
type: docs
weight: 22
url: /ar/net/excel-formatting-and-styling/rotating-and-changing-text-direction/
---
## مقدمة
عندما يتعلق الأمر بالعمل مع ملفات Excel برمجيًا، فإننا غالبًا ما نواجه تحدي عرض البيانات بالتنسيق المطلوب. هل أردت يومًا تغيير اتجاه النص في خلية Excel؟ ربما تحتاج إلى قراءة النص من اليمين إلى اليسار، وخاصةً إذا كنت تعمل بلغات مثل العربية أو العبرية. أو ربما تبحث فقط عن طريقة لتحسين المظهر المرئي لجداول البيانات الخاصة بك. أياً كان سببك، يوفر Aspose.Cells for .NET حلاً مباشرًا للتلاعب باتجاه النص في ملفات Excel. في هذا البرنامج التعليمي، سنوضح الخطوات اللازمة لتدوير وتغيير اتجاه النص في Excel باستخدام Aspose.Cells.
## المتطلبات الأساسية
قبل أن نتعمق في جزء الترميز، تأكد من أن لديك بعض الأشياء جاهزة:
1. Visual Studio: تأكد من تثبيت Visual Studio على جهاز الكمبيوتر لديك. تعمل مكتبة Aspose.Cells بشكل جيد معه.
2.  مكتبة Aspose.Cells: ستحتاج إلى مكتبة Aspose.Cells لـ .NET. يمكنك تنزيلها من[موقع](https://releases.aspose.com/cells/net/).
3. المعرفة الأساسية بلغة C#: إن الإلمام ببرمجة C# سوف يسهل عليك متابعة البرنامج التعليمي.
4. .NET Framework: تأكد من أن مشروعك يستهدف .NET Framework، حيث تم تصميم Aspose.Cells للعمل ضمن تلك البيئة.
بمجرد أن تكون جميع المتطلبات الأساسية جاهزة، فأنت جاهز للبدء!
## استيراد الحزم
الآن، لنبدأ في تحضير مشروعنا عن طريق استيراد الحزم المطلوبة. وإليك كيفية القيام بذلك:
### إنشاء مشروع جديد
- افتح Visual Studio، وأنشئ مشروعًا جديدًا.
- حدد تطبيق وحدة التحكم من القوالب، وأعطه اسمًا مناسبًا مثل "ExcelTextDirectionDemo".
### إضافة مكتبة Aspose.Cells
- انقر بزر الماوس الأيمن فوق المشروع في مستكشف الحلول واختر إدارة حزم NuGet.
- ابحث عن Aspose.Cells وقم بتثبيته.
### استيراد المساحات الاسمية الضرورية
 الآن حان الوقت لإحضار مساحات الأسماء الضرورية. في الجزء العلوي من`Program.cs` الملف، يتضمن ما يلي:
```csharp
using System.IO;
using Aspose.Cells;
```
وبهذا تكون جاهزًا لبدء تعديل ملفات Excel! والآن، دعنا ننتقل إلى الترميز الفعلي.
## الخطوة 1: إعداد دليل المستندات الخاص بك
للتأكد من حفظ ملف Excel في المكان الصحيح، نحتاج إلى تحديد دليل. وإليك كيفية القيام بذلك:
```csharp
// المسار إلى دليل المستندات.
string dataDir = "Your Document Directory"; // ضبط مسار الدليل الخاص بك
// إنشاء الدليل إذا لم يكن موجودًا بالفعل.
bool IsExists = System.IO.Directory.Exists(dataDir);
if (!IsExists)
    System.IO.Directory.CreateDirectory(dataDir);
```

يحدد هذا الكود دليلاً لحفظ ملف Excel. يتحقق من وجود الدليل ويقوم بإنشائه إذا لم يكن موجودًا. تأكد من استبدال`"Your Document Directory"` مع مسار صالح.
## الخطوة 2: إنشاء مثيل لكائن مصنف
بعد ذلك، دعنا ننشئ مصنف Excel جديدًا. هذا هو المكان الذي سنتعامل فيه مع خلايانا.
```csharp
// إنشاء كائن مصنف
Workbook workbook = new Workbook();
```

 من خلال إنشاء`Workbook` الكائن، فأنت تبدأ في الأساس بملف Excel جديد فارغ يمكنك تعديله.
## الخطوة 3: الحصول على مرجع ورقة العمل
الآن قم بالوصول إلى ورقة العمل التي تريد إجراء التغييرات عليها.
```csharp
// الحصول على مرجع ورقة العمل
Worksheet worksheet = workbook.Worksheets[0];
```

 ال`Worksheet` يشير الكائن إلى ورقة العمل الأولى في المصنف الخاص بك. يمكنك الوصول إلى أوراق العمل الأخرى عن طريق تغيير الفهرس.
## الخطوة 4: الوصول إلى خلية محددة
دعونا نركز على خلية محددة، في هذه الحالة، "A1". 
```csharp
// الوصول إلى الخلية "A1" من ورقة العمل
Aspose.Cells.Cell cell = worksheet.Cells["A1"];
```

يتيح لك هذا السطر من التعليمات البرمجية الوصول إلى الخلية "A1"، والتي سنقوم بتعديلها قريبًا.
## الخطوة 5: إضافة القيمة إلى الخلية
حان الوقت لوضع بعض البيانات في خلايانا.
```csharp
// إضافة بعض القيمة إلى الخلية "A1"
cell.PutValue("Visit Aspose!");
```

هنا، نضيف ببساطة النص "Visit Aspose!" إلى الخلية "A1". ويمكنك تغيير هذا النص إلى أي نص تريده.
## الخطوة 6: إعداد نمط النص
الآن يأتي الجزء الذي نقوم فيه بتغيير اتجاه النص. 
```csharp
// ضبط المحاذاة الأفقية للنص في الخلية "A1"
Style style = cell.GetStyle();
```

يؤدي هذا إلى استرجاع نمط الخلية الحالي، مما يمهد الطريق للتعديلات.
## الخطوة 7: تغيير اتجاه النص 
وهنا يحدث السحر! يمكنك تغيير اتجاه النص على النحو التالي:
```csharp
// ضبط اتجاه النص من اليمين إلى اليسار
style.TextDirection = TextDirectionType.RightToLeft;
```

يقوم هذا السطر بتعيين اتجاه النص من اليمين إلى اليسار، وهو أمر ضروري للغات مثل العربية أو العبرية. 
## الخطوة 8: تطبيق النمط على الخلية
بعد تغيير نمط اتجاه النص، قم بتطبيق هذه التغييرات مرة أخرى على الخلية:
```csharp
cell.SetStyle(style);
```

قم بتطبيق النمط المعدل على الخلية مرة أخرى، مع التأكد من أنه يعكس اتجاه النص الجديد.
## الخطوة 9: حفظ ملف Excel
وأخيرًا، دعونا نحفظ تغييراتنا في ملف Excel جديد.
```csharp
// حفظ ملف Excel
workbook.Save(dataDir + "book1.out.xls", SaveFormat.Excel97To2003);
```

يحفظ هذا الكود المصنف باسم الملف المحدد في الدليل المحدد. التنسيق المحدد هو Excel 97-2003.
## خاتمة
والآن، لقد تعلمت بنجاح كيفية تدوير وتغيير اتجاه النص في خلية Excel باستخدام Aspose.Cells for .NET. أليس من المدهش كيف يمكن لبضعة أسطر من التعليمات البرمجية أن تغير تمامًا تخطيط جدول البيانات الخاص بك وإمكانية الوصول إلى اللغة؟ إن القدرة على التعامل مع ملفات Excel برمجيًا تفتح عالمًا من الاحتمالات، من أتمتة التقارير إلى تحسين عرض البيانات.
## الأسئلة الشائعة
### هل يمكنني تغيير اتجاه النص لخلايا متعددة؟  
نعم، يمكنك التنقل عبر نطاق من الخلايا وتطبيق نفس التغييرات.
### هل استخدام Aspose.Cells مجاني؟  
يقدم Aspose.Cells نسخة تجريبية مجانية، ولكن يلزم الحصول على ترخيص للاستخدام المستمر.
### ما هي التنسيقات الأخرى التي يمكنني الحفظ بها؟  
يدعم Aspose.Cells تنسيقات مختلفة مثل XLSX وCSV وPDF.
### هل أحتاج إلى تثبيت أي شيء آخر غير Visual Studio؟  
كل ما تحتاج إلى إضافته هو مكتبة Aspose.Cells إلى مشروعك.
### أين يمكنني العثور على مزيد من المعلومات حول Aspose.Cells؟  
 يمكنك التحقق من[التوثيق](https://reference.aspose.com/cells/net/) للحصول على أدلة شاملة ومراجع API.