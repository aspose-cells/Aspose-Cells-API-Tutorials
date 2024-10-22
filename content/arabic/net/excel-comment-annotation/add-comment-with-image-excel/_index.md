---
title: إضافة تعليق مع صورة في Excel
linktitle: إضافة تعليق مع صورة في Excel
second_title: واجهة برمجة تطبيقات معالجة Excel الخاصة بـ Aspose.Cells .NET
description: تعرف على كيفية إضافة تعليقات بالصور في Excel باستخدام Aspose.Cells for .NET. قم بتحسين جداول البيانات الخاصة بك باستخدام التعليقات التوضيحية المخصصة.
type: docs
weight: 10
url: /ar/net/excel-comment-annotation/add-comment-with-image-excel/
---
## مقدمة
يعد برنامج Excel أداة قوية لإدارة البيانات وتحليلها، ولكنك تحتاج أحيانًا إلى إضافة لمسة شخصية إلى جداول البيانات الخاصة بك، أليس كذلك؟ ربما تريد إضافة تعليقات توضيحية إلى البيانات أو تقديم ملاحظات أو حتى إضافة لمسة من الأناقة باستخدام الصور. وهنا تأتي أهمية التعليقات! في هذا البرنامج التعليمي، سنستكشف كيفية إضافة تعليق بصورة في برنامج Excel باستخدام مكتبة Aspose.Cells لـ .NET. يمكن أن يكون هذا النهج مفيدًا بشكل خاص لإنشاء جداول بيانات أكثر تفاعلية وجاذبية بصريًا.
## المتطلبات الأساسية
قبل أن نتعمق في التفاصيل الدقيقة لإضافة التعليقات مع الصور في Excel، دعنا نتأكد من أن لديك كل ما تحتاجه للبدء:
1. Visual Studio: تأكد من تثبيت Visual Studio على جهاز الكمبيوتر الخاص بك. هذا هو المكان الذي ستكتب فيه التعليمات البرمجية الخاصة بك وتنفذها.
2.  Aspose.Cells لـ .NET: يجب أن يكون لديك مكتبة Aspose.Cells. إذا لم تقم بتثبيتها بعد، يمكنك تنزيلها من[هنا](https://releases.aspose.com/cells/net/).
3. المعرفة الأساسية بلغة C#: ستساعدك المعرفة ببرمجة C# على فهم مقتطفات التعليمات البرمجية بشكل أفضل.
4. ملف صورة: قم بإعداد ملف صورة (مثل شعار) تريد تضمينه في تعليق Excel الخاص بك. في هذا البرنامج التعليمي، سنفترض أن لديك ملفًا باسم`logo.jpg`.
5. .NET Framework: تأكد من تثبيت .NET Framework، حيث يتطلب Aspose.Cells أن يعمل بشكل صحيح.
الآن بعد أن قمنا بتغطية المتطلبات الأساسية لدينا، دعنا ننتقل إلى الترميز الفعلي!
## استيراد الحزم
أولاً وقبل كل شيء، نحتاج إلى استيراد الحزم اللازمة. في مشروع C# الخاص بك، تأكد من إضافة مرجع إلى مكتبة Aspose.Cells. يمكنك القيام بذلك باستخدام NuGet Package Manager في Visual Studio. إليك الطريقة:
1. افتح Visual Studio.
2. إنشاء مشروع جديد أو فتح مشروع موجود.
3. انقر بزر الماوس الأيمن على مشروعك في مستكشف الحلول.
4. حدد إدارة حزم NuGet.
5. ابحث عن Aspose.Cells وقم بتثبيته.

```csharp
using System.IO;
using Aspose.Cells;
using System.Drawing;
```

بمجرد تثبيت المكتبة، يمكنك البدء في كتابة الكود الخاص بك. وإليك كيفية القيام بذلك خطوة بخطوة.
## الخطوة 1: إعداد دليل المستندات الخاص بك
للبدء، نحتاج إلى إنشاء دليل حيث يمكننا حفظ ملفات Excel الخاصة بنا. هذه خطوة بالغة الأهمية لأننا نريد الحفاظ على تنظيم عملنا.
```csharp
// المسار إلى دليل المستندات.
string dataDir = "Your Document Directory";
//إنشاء الدليل إذا لم يكن موجودًا بالفعل.
bool IsExists = System.IO.Directory.Exists(dataDir);
if (!IsExists)
    System.IO.Directory.CreateDirectory(dataDir);
```
-  dataDir: يحتوي هذا المتغير على المسار إلى دليل المستندات الخاص بك. استبدل`"Your Document Directory"` مع المسار الفعلي الذي تريد حفظ ملف Excel فيه.
- Directory.Exists: يتحقق هذا من وجود الدليل بالفعل.
- Directory.CreateDirectory: إذا لم يكن الدليل موجودًا، فسيتم إنشاءه.
## الخطوة 2: إنشاء مصنف
 بعد ذلك، نحتاج إلى إنشاء مثيل لـ`Workbook` هذه الفئة تمثل مصنف Excel في الذاكرة.
```csharp
//إنشاء مثيل لكتاب عمل
Workbook workbook = new Workbook();
```
- مصنف العمل: هذا هو الفصل الرئيسي في Aspose.Cells الذي يسمح لك بإنشاء ملفات Excel ومعالجتها. من خلال إنشائه، فإنك تقوم في الأساس بإنشاء مصنف عمل Excel جديد.
## الخطوة 3: الحصول على مجموعة التعليقات
الآن بعد أن أصبح لدينا مصنف العمل، فلننتقل إلى مجموعة التعليقات الموجودة في ورقة العمل الأولى.
```csharp
// احصل على مرجع لمجموعة التعليقات مع الورقة الأولى
CommentCollection comments = workbook.Worksheets[0].Comments;
```
- أوراق العمل[ 0]: يؤدي هذا إلى الوصول إلى ورقة العمل الأولى في المصنف. تذكر أن الفهرس يعتمد على الصفر، لذا`[0]` يشير إلى الورقة الأولى.
- التعليقات: تتيح لنا هذه الخاصية الوصول إلى مجموعة التعليقات الموجودة على ورقة العمل هذه.
## الخطوة 4: إضافة تعليق إلى خلية
لنقم بإضافة تعليق إلى خلية معينة. في هذه الحالة، سنضيف تعليقًا إلى الخلية A1.
```csharp
// أضف تعليقًا إلى الخلية A1
int commentIndex = comments.Add(0, 0);
Comment comment = comments[commentIndex];
comment.Note = "First note.";
comment.Font.Name = "Times New Roman";
```
- comments.Add(0, 0): تضيف هذه الطريقة تعليقًا إلى الخلية A1 (الصف 0، العمود 0).
- ملاحظة: هنا، قمنا بتعيين نص التعليق.
- comment.Font.Name: يحدد هذا الخط الخاص بنص التعليق.
## الخطوة 5: تحميل صورة إلى مجرى
 الآن حان الوقت لتحميل الصورة التي نريد تضمينها في تعليقنا. سنستخدم`MemoryStream` لحفظ بيانات الصورة.
```csharp
// تحميل صورة إلى الدفق
Bitmap bmp = new Bitmap(dataDir + "logo.jpg");
MemoryStream ms = new MemoryStream();
bmp.Save(ms, System.Drawing.Imaging.ImageFormat.Png);
```
- Bitmap: تُستخدم هذه الفئة لتحميل ملف الصورة. تأكد من صحة المسار.
- MemoryStream: هذا هو التدفق الذي سنستخدمه لحفظ الصورة في الذاكرة.
- bmp.Save: يؤدي هذا إلى حفظ صورة الخريطة النقطية في مجرى الذاكرة بتنسيق PNG.
## الخطوة 6: تعيين بيانات الصورة على شكل التعليق
الآن علينا تعيين بيانات الصورة إلى الشكل المرتبط بالتعليق الذي أنشأناه سابقًا.
```csharp
// تعيين بيانات الصورة إلى الشكل المرتبط بالتعليق
comment.CommentShape.Fill.ImageData = ms.ToArray();
```
-  comment.CommentShape.Fill.ImageData: تتيح لك هذه الخاصية تعيين الصورة لشكل التعليق. نقوم بتحويل`MemoryStream` إلى مجموعة بايتات باستخدام`ms.ToArray()`.
## الخطوة 7: احفظ المصنف
وأخيرًا، دعونا نحفظ مصنفنا مع التعليق والصورة المضمنين.
```csharp
// حفظ المصنف
workbook.Save(dataDir + "book1.out.xlsx", Aspose.Cells.SaveFormat.Xlsx);
```
- workbook.Save: تحفظ هذه الطريقة المصنف في المسار المحدد. نقوم بحفظه كملف XLSX.
## خاتمة
والآن، لقد نجحت في إضافة تعليق مع صورة إلى ملف Excel باستخدام Aspose.Cells for .NET. يمكن لهذه الميزة أن تجعل جداول البيانات الخاصة بك أكثر إفادة وجاذبية من الناحية البصرية. سواء كنت تقوم بتعليق البيانات أو تقديم الملاحظات أو ببساطة إضافة لمسة شخصية، يمكن للتعليقات مع الصور أن تعزز تجربة المستخدم بشكل كبير.
## الأسئلة الشائعة
### هل يمكنني إضافة تعليقات متعددة إلى نفس الخلية؟
لا، لا يسمح برنامج Excel بإضافة تعليقات متعددة إلى الخلية نفسها. يمكنك إضافة تعليق واحد فقط لكل خلية.
### ما هي تنسيقات الصور المدعومة؟
يدعم Aspose.Cells تنسيقات الصور المختلفة، بما في ذلك PNG وJPEG وBMP.
### هل أحتاج إلى ترخيص لاستخدام Aspose.Cells؟
يقدم Aspose.Cells نسخة تجريبية مجانية، ولكن للحصول على الوظائف الكاملة، ستحتاج إلى شراء ترخيص.
### هل يمكنني تخصيص مظهر التعليق؟
نعم، يمكنك تخصيص الخط وحجم ولون نص التعليق، ويمكنك أيضًا تغيير شكل وحجم التعليق نفسه.
### أين يمكنني العثور على مزيد من الوثائق حول Aspose.Cells؟
 يمكنك العثور على وثائق شاملة على Aspose.Cells[هنا](https://reference.aspose.com/cells/net/).