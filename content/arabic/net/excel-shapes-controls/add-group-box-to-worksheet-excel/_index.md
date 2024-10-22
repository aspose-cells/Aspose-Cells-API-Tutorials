---
title: إضافة مربع المجموعة إلى ورقة العمل في Excel
linktitle: إضافة مربع المجموعة إلى ورقة العمل في Excel
second_title: واجهة برمجة تطبيقات معالجة Excel الخاصة بـ Aspose.Cells .NET
description: تعرف على كيفية إضافة مربع مجموعة وأزرار اختيار في Excel باستخدام Aspose.Cells for .NET. دليل خطوة بخطوة للمطورين من جميع المستويات.
type: docs
weight: 24
url: /ar/net/excel-shapes-controls/add-group-box-to-worksheet-excel/
---
## مقدمة
عندما يتعلق الأمر بعرض البيانات، فإن برنامج Excel هو الملك. إن إضافة عناصر تفاعلية مثل مربعات المجموعات يمكن أن تجعل جداول البيانات الخاصة بك أكثر جاذبية وسهولة في الاستخدام. اليوم، نتعمق في عالم Aspose.Cells for .NET، وهي مكتبة قوية تساعدك على التعامل مع جداول بيانات Excel دون عناء. ولكن لا تقلق إذا لم تكن من خبراء البرمجة، فهذا الدليل يقسم كل شيء إلى خطوات بسيطة. هل أنت مستعد لتحسين مهاراتك في Excel؟ لنبدأ!
## المتطلبات الأساسية
قبل أن ننتقل إلى الكود، هناك بعض الأشياء التي ستحتاجها:
1. Visual Studio: تأكد من تثبيت Visual Studio على جهازك؛ فهو المكان الذي ستكتب فيه كود .NET.
2.  Aspose.Cells for .NET: تحتاج إلى تنزيل هذه المكتبة. يمكنك العثور عليها[هنا](https://releases.aspose.com/cells/net/). 
3. المعرفة الأساسية بلغة C#: على الرغم من أنني سأشرح كل شيء خطوة بخطوة، إلا أن القليل من الفهم بلغة C# سيساعدك على المتابعة.
## استيراد الحزم
بالنسبة لأي مشروع، ستحتاج أولاً إلى استيراد الحزم اللازمة. هنا، سيكون Aspose.Cells هو محور اهتمامك الرئيسي. وإليك كيفية القيام بذلك:
## الخطوة 1: افتح مشروعك في Visual Studio
قم بتشغيل Visual Studio وافتح مشروعك الحالي أو قم بإنشاء مشروع جديد. 
## الخطوة 2: إضافة مرجع إلى Aspose.Cells
- انقر بزر الماوس الأيمن على مشروعك في مستكشف الحلول.
- حدد "إدارة حزم NuGet".
- ابحث عن "Aspose.Cells" وقم بتثبيته. سيسمح لك هذا باستخدام كافة الفئات والطرق التي توفرها مكتبة Aspose.Cells.
## الخطوة 3: تضمين استخدام التوجيه
في الجزء العلوي من ملف C# الخاص بك، قم بتضمين مساحة اسم Aspose.Cells:
```csharp
using System.IO;
using Aspose.Cells;
using Aspose.Cells.Drawing;
using System.Drawing;
```
يتيح لك هذا الوصول إلى الفئات اللازمة للعمل مع ملفات Excel.
الآن بعد أن انتهينا من الإعداد، فلننتقل إلى لب البرنامج التعليمي، وهو إضافة مربع مجموعة يحتوي على أزرار اختيارية إلى ورقة عمل Excel. وسنقسم هذه العملية إلى عدة خطوات من أجل التوضيح.
## الخطوة 1: إعداد دليل المستندات الخاص بك
قبل إنشاء أي ملف Excel، ستحتاج إلى تحديد المكان الذي ترغب في حفظه فيه. دعنا ننشئ دليلًا إذا لم يكن موجودًا بالفعل.
```csharp
// المسار إلى دليل المستندات
string dataDir = "Your Document Directory"; // حدد المسار المطلوب
//إنشاء الدليل إذا لم يكن موجودًا بالفعل.
bool IsExists = System.IO.Directory.Exists(dataDir);
if (!IsExists)
    System.IO.Directory.CreateDirectory(dataDir);
```
يتحقق هذا الكود من وجود الدليل الذي سيتم حفظ ملف Excel فيه. وإذا لم يكن موجودًا، فإنه ينشئ دليلًا — الأمر أشبه بإعداد مساحة العمل الخاصة بك قبل الانخراط في المشروع!
## الخطوة 2: إنشاء مصنف جديد
بعد ذلك، ستحتاج إلى إنشاء مصنف Excel حيث ستضيف مربع المجموعة الخاص بك.
```csharp
// إنشاء مصنف جديد.
Workbook excelbook = new Workbook();
```
يقوم هذا السطر بتهيئة مثيل جديد من مصنف. يمكنك اعتبار هذا الأمر بمثابة فتح ملف Excel جديد فارغ وجاهز للتعديل.
## الخطوة 3: إضافة مربع المجموعة
الآن، دعونا نضيف صندوق المجموعة هذا. 
```csharp
// أضف مربع المجموعة إلى ورقة العمل الأولى.
GroupBox box = excelbook.Worksheets[0].Shapes.AddGroupBox(1, 0, 1, 0, 300, 250);
```
هنا، تقوم بإضافة مربع مجموعة عند إحداثيات محددة في ورقة العمل الأولى. تحدد المعلمات موضع وحجم المربع، تمامًا مثل وضع الأثاث في الغرفة!
## الخطوة 4: تعيين تسمية توضيحية لمربع المجموعة
الآن، دعونا نعطي صندوق مجموعتك عنوانًا!
```csharp
// تعيين تسمية توضيحية لمربع المجموعة.
box.Text = "Age Groups";
box.Placement = PlacementType.FreeFloating;
```
 يحدد سلسلة "المجموعات العمرية" التسمية التي تظهر في مربع المجموعة.`Placement` مثل`FreeFloating` يسمح للصندوق بالتحرك - المرونة هي المفتاح!
## الخطوة 5: اجعل مربع المجموعة ثنائي الأبعاد
رغم أن المظهر ثلاثي الأبعاد قد يبدو رائعًا، إلا أننا نهدف إلى المظهر الكلاسيكي هنا.
```csharp
// اجعله صندوقًا ثنائي الأبعاد.
box.Shadow = false;
```
يقوم هذا الكود بإزالة تأثير الظل، مما يمنح الصندوق مظهرًا مسطحًا - مثل قطعة ورق بسيطة!
## الخطوة 6: إضافة أزرار الاختيار
دعونا نضفي بعض الإثارة على الأمور من خلال إضافة بعض أزرار الاختيار لإدخال المستخدم.
## الخطوة 6.1: إضافة زر الاختيار الأول
```csharp
// إضافة زر الاختيار.
Aspose.Cells.Drawing.RadioButton radio1 = excelbook.Worksheets[0].Shapes.AddRadioButton(3, 0, 2, 0, 30, 110);
// تعيين سلسلة النص الخاصة به.
radio1.Text = "20-29";
// تعيين الخلية A1 كخلية مرتبطة لزر الاختيار.
radio1.LinkedCell = "A1";
```
يمكنك إنشاء زر اختيار للفئة العمرية 20-29 عامًا، وربطه بالخلية A1 في ورقة العمل. وهذا يعني أنه عند تحديد هذا الزر، تعكس الخلية A1 هذا الاختيار!
## الخطوة 6.2: تخصيص زر الاختيار الأول
الآن دعونا نعطيها بعض الأناقة.
```csharp
// جعل زر الاختيار ثلاثي الأبعاد.
radio1.Shadow = true;
// ضبط وزن زر الاختيار.
radio1.Line.Weight = 4;
// تعيين نمط شرطة زر الاختيار.
radio1.Line.DashStyle = MsoLineDashStyle.Solid;
```
من خلال إضافة ظل وتعديل نمط الخط، نعمل على تحسين رؤية الزر. الأمر أشبه بإضافة زخارف لجعله بارزًا عن الصفحة!
## الخطوة 6.3: كرر ذلك للحصول على المزيد من أزرار الاختيار
كرر هذه العملية للمجموعات العمرية الإضافية:
```csharp
// زر الاختيار الثاني
Aspose.Cells.Drawing.RadioButton radio2 = excelbook.Worksheets[0].Shapes.AddRadioButton(6, 0, 2, 0, 30, 110);
radio2.Text = "30-39";
radio2.LinkedCell = "A1";
radio2.Shadow = true;
radio2.Line.Weight = 4;
radio2.Line.DashStyle = MsoLineDashStyle.Solid;
// زر الاختيار الثالث
Aspose.Cells.Drawing.RadioButton radio3 = excelbook.Worksheets[0].Shapes.AddRadioButton(9, 0, 2, 0, 30, 110);
radio3.Text = "40-49";
radio3.LinkedCell = "A1";
radio3.Shadow = true;
radio3.Line.Weight = 4;
radio3.Line.DashStyle = MsoLineDashStyle.Solid;
```
يعمل كل زر اختيار كخيار لفئات عمرية مختلفة، ويرتبط بنفس الخلية A1. وهذا يسمح بعملية اختيار بسيطة وسهلة الاستخدام.
## الخطوة 7: تجميع الأشكال
وبعد أن أصبح كل شيء في مكانه، دعونا نقوم بترتيب الأشياء عن طريق تجميع أشكالنا. 
```csharp
// احصل على الأشكال.
Aspose.Cells.Drawing.Shape[] shapeobjects = new Shape[] { box, radio1, radio2, radio3 };
// تجميع الأشكال.
Aspose.Cells.Drawing.GroupShape group = excelbook.Worksheets[0].Shapes.Group(shapeobjects);
```
تجمع هذه الخطوة كل شيء في وحدة متماسكة واحدة. الأمر أشبه بوضع إطار حول مجموعتك الفنية، فهو يربطها معًا بشكل جميل!
## الخطوة 8: حفظ ملف Excel
وأخيرا، دعونا نحفظ تحفتنا الفنية!
```csharp
// احفظ ملف Excel.
excelbook.Save(dataDir + "book1.out.xls");
```
يكتب هذا السطر من التعليمات البرمجية التغييرات التي أجريتها في ملف Excel جديد باسم "book1.out.xls" في الدليل المحدد. وكما لو كنت تغلق مظروفًا، يتم الآن تخزين عملك بأمان!
## خاتمة
والآن لديك الدليل الكامل لإضافة مربع مجموعة وأزرار اختيار إلى ورقة عمل Excel باستخدام Aspose.Cells for .NET! مع كل خطوة، ستتعلم كيفية التعامل مع Excel برمجيًا، مما يفتح الأبواب أمام إمكانيات لا حصر لها لتخصيص التقارير وتصور البيانات والمزيد. يكمن جمال البرمجة في أنه يمكنك أتمتة المهام وإنشاء واجهات سهلة الاستخدام بسهولة نسبية - تخيل الإمكانات!
## الأسئلة الشائعة
### ما هو Aspose.Cells؟
Aspose.Cells عبارة عن مكتبة .NET لإدارة ملفات Excel، وتمكين مهام مثل القراءة والكتابة والتلاعب بجداول البيانات برمجيًا.
### هل أحتاج إلى خبرة في البرمجة لاستخدام Aspose.Cells؟
على الرغم من أن بعض المعرفة البرمجية مفيدة، فإن هذا البرنامج التعليمي يرشدك خلال الأساسيات، مما يجعله في متناول المبتدئين!
### هل يمكنني تخصيص مظهر مربعات المجموعة والأزرار؟
بالتأكيد! يوفر Aspose.Cells خيارات واسعة لتصميم الأشكال، بما في ذلك الألوان والأحجام والتأثيرات ثلاثية الأبعاد.
### هل هناك نسخة تجريبية مجانية متاحة لـ Aspose.Cells؟
 نعم! يمكنك تجربته مجانًا من خلال زيارة[نسخة تجريبية مجانية من Aspose](https://releases.aspose.com/).
### أين يمكنني العثور على المزيد من الموارد أو الدعم لـ Aspose.Cells؟
 ال[منتدى دعم Aspose](https://forum.aspose.com/c/cells/9) يعد مكانًا رائعًا لطلب المساعدة ومشاركة المعرفة مع المجتمع.