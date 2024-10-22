---
title: ورقة عمل لتحويل الصورة إلى .NET
linktitle: ورقة عمل لتحويل الصورة إلى .NET
second_title: واجهة برمجة تطبيقات معالجة Excel الخاصة بـ Aspose.Cells .NET
description: تعرف على كيفية تحويل أوراق عمل Excel إلى صور في .NET باستخدام Aspose.Cells من خلال دليلنا خطوة بخطوة. قم بتبسيط تصور البيانات.
type: docs
weight: 11
url: /ar/net/image-and-chart-operations/worksheet-to-image-conversion/
---
## مقدمة
عندما يتعلق الأمر بالتعامل مع ملفات Excel في .NET، تبرز Aspose.Cells كمكتبة موثوقة وقوية. إحدى المهام المتكررة التي قد تواجهها هي تحويل ورقة عمل Excel إلى صورة. سواء كنت تريد عرض الورقة على صفحة ويب أو تضمينها في تقرير أو مشاركة البيانات بصريًا، فإن هذا الدليل خطوة بخطوة سيرشدك خلال العملية بأكملها. في النهاية، ستكون مجهزًا بكل ما تحتاجه لتحويل أوراق العمل إلى صور بسلاسة. لذا فلنبدأ!
## المتطلبات الأساسية
قبل أن نبدأ عملية التحويل، من الضروري التأكد من إعداد كل شيء بشكل صحيح. فيما يلي المتطلبات الأساسية التي ستحتاج إليها:
1. Visual Studio: تأكد من تثبيت Visual Studio على جهاز الكمبيوتر الخاص بك. فهو عبارة عن بيئة تطوير متكاملة تساعدك على تشغيل مشاريع .NET بسلاسة.
2. مكتبة Aspose.Cells لـ .NET: تحتاج إلى الحصول على هذه المكتبة. يمكنك[تحميله هنا](https://releases.aspose.com/cells/net/) أو ابدأ بـ[نسخة تجريبية مجانية](https://releases.aspose.com/).
3. المعرفة الأساسية بلغة C#: ستكون المعرفة ببرمجة C# مفيدة، حيث سيتم كتابة أمثلتنا وشروحاتنا بهذه اللغة.
4.  ملف Excel نموذجي: للتوضيح، قم بإنشاء ملف Excel أو تنزيله. احفظه باسم`MyTestBook1.xls` في دليل مشروعك.
5. الفهم الأساسي لمشاريع .NET: إن معرفة كيفية إنشاء مشروع .NET بسيط سيجعل هذا الأمر أسهل، ولكن لا تقلق - سنرشدك خلال الخطوات.
## استيراد الحزم
الخطوة الأولى في رحلتنا هي استيراد حزم Aspose.Cells الضرورية إلى مشروعنا. وهذا أمر ضروري لأنه يسمح لنا بالاستفادة من جميع الوظائف التي يوفرها Aspose.Cells.
## الخطوة 1: إنشاء مشروع جديد 
للبدء، قم بإنشاء مشروع .NET جديد في Visual Studio:
- افتح Visual Studio.
- انقر فوق "إنشاء مشروع جديد".
- حدد "تطبيق وحدة التحكم (.NET Framework)" أو "تطبيق وحدة التحكم (.NET Core)" وفقًا لتفضيلاتك.
- قم بتسمية مشروعك (على سبيل المثال، WorksheetToImage) وانقر فوق "إنشاء".
## الخطوة 2: إضافة مرجع Aspose.Cells
الآن بعد أن أصبح لدينا مشروعنا، نحتاج إلى إضافة Aspose.Cells:
- انقر بزر الماوس الأيمن على مشروعك في مستكشف الحلول.
- حدد "إدارة حزم NuGet".
- ابحث عن “Aspose.Cells” وقم بتثبيت الإصدار الأحدث.
```csharp
using System.IO;
using System.Drawing;
using Aspose.Cells;
using Aspose.Cells.Rendering;
```
أنت جاهز تمامًا للجزء المتعلق بالترميز!

الآن، دعنا نستعرض عملية التحويل الفعلية خطوة بخطوة. سنستخدم برنامج C# بسيطًا يفتح ملف Excel ويحول ورقة عمل إلى صورة ويحفظ تلك الصورة في دليل محدد.
## الخطوة 3: إعداد البيئة
أولاً، قم بإعداد بيئتك عن طريق تحديد المسار إلى دليل المستندات الخاص بك:
```csharp
// المسار إلى دليل المستندات.
string dataDir = "Your Document Directory";
```
 هنا، نقوم بتعريف متغير يسمى`dataDir` الذي يحمل المسار إلى الدليل الذي سيتم تخزين ملفاتنا فيه. استبدل`"Your Document Directory"` مع المسار الفعلي على نظامك (على سبيل المثال، "C:\\ملفاتي\").
## الخطوة 4: افتح مصنف Excel
 بعد ذلك، سنفتح ملف Excel باستخدام`Workbook` الفئة من Aspose.Cells:
```csharp
// افتح ملف قالب Excel.
Workbook book = new Workbook(dataDir + "MyTestBook1.xls");
```
 في هذه الخطوة، نقوم بإنشاء مثيل لـ`Workbook`الفئة وتمرير المسار إلى ملف Excel الخاص بنا. يتيح لنا هذا التفاعل مع محتويات الملف برمجيًا.
## الخطوة 5: الوصول إلى ورقة العمل
الآن بعد أن فتحنا المصنف، فلننتقل إلى ورقة العمل الأولى:
```csharp
// احصل على ورقة العمل الأولى.
Worksheet sheet = book.Worksheets[0];
```
 هنا، نسترد ورقة العمل الأولى (الفهرس`0` ) من المصنف. يتم فهرسة مصفوفات Aspose.Cells إلى الصفر، مما يعني أن الورقة الأولى هي`0`.
## الخطوة 6: تحديد خيارات الصورة أو الطباعة
 قبل أن نقوم بعرض الصورة، نحتاج إلى تحديد الشكل الذي نريد أن تبدو عليه باستخدام`ImageOrPrintOptions`:
```csharp
// تحديد خيارات الصورة أو الطباعة
ImageOrPrintOptions imgOptions = new ImageOrPrintOptions();
// حدد تنسيق الصورة
imgOptions.ImageType = Drawing.ImageType.Jpeg;
// سيتم عرض صفحة واحدة فقط للورقة بأكملها
imgOptions.OnePagePerSheet = true;
```
 في هذه الخطوة، نقوم بإنشاء مثيل لـ`ImageOrPrintOptions` نحدد أننا نريد حفظ الناتج كصورة JPEG ونضبط`OnePagePerSheet` ل`true` للتأكد من التقاط الورقة بأكملها في صورة واحدة.
## الخطوة 7: عرض ورقة العمل
مع توفر الخيارات، يمكننا الآن عرض ورقة العمل:
```csharp
// عرض الورقة فيما يتعلق بخيارات الصورة/الطباعة المحددة
SheetRender sr = new SheetRender(sheet, imgOptions);
// تقديم الصورة للورقة
Bitmap bitmap = sr.ToImage(0);
```
 ال`SheetRender`تساعد الفئة في تحويل ورقة العمل إلى صورة نقطية. نطلق عليها`ToImage(0)` لتحويل الصفحة صفر (صفحتنا الأولى) إلى خريطة نقطية.
## الخطوة 8: حفظ الصورة
بعد العرض، نحتاج إلى حفظ الصورة في الدليل المحدد:
```csharp
// احفظ ملف الصورة مع تحديد تنسيق الصورة.
bitmap.Save(dataDir + "SheetImage.out.jpg");
```
 هنا، نقوم بحفظ صورة الخريطة النقطية التي قمنا بإنشائها. يكتب هذا السطر الصورة إلى`dataDir` الموقع مع اسم الملف`SheetImage.out.jpg`.
## الخطوة 9: إشعار الإكمال
للتأكد من اكتمال العملية، دعنا نضيف رسالة وحدة تحكم بسيطة:
```csharp
// عرض النتيجة حتى يتمكن المستخدم من معرفة أن المعالجة قد انتهت.
System.Console.WriteLine("Conversion to Image(s) completed.");
```
يقوم هذا السطر بإخراج رسالة تأكيد إلى وحدة التحكم، لإعلام المستخدم بنجاح التحويل.
## خاتمة
والآن، لقد انتهيت! في بضع خطوات بسيطة، تعلمت كيفية تحويل ورقة عمل Excel إلى صورة باستخدام Aspose.Cells for .NET. هذه العملية ليست سريعة فحسب، بل إنها قوية أيضًا، حيث تمكنك من إنشاء تمثيلات مرئية لبيانات جدول البيانات الخاص بك دون عناء.
## الأسئلة الشائعة
### ما هو Aspose.Cells؟
Aspose.Cells هي مكتبة .NET تتيح للمطورين إنشاء ملفات Excel ومعالجتها وتحويلها وبرمجتها.
### هل يمكنني استخدام Aspose.Cells مجانًا؟
 نعم، يمكنك البدء في استخدام Aspose.Cells عن طريق تنزيل نسخة تجريبية مجانية من موقعهم[موقع إلكتروني](https://releases.aspose.com/).
### ما هي تنسيقات الصور التي يدعمها Aspose.Cells للتصدير؟
يدعم Aspose.Cells تنسيقات الصور المختلفة، بما في ذلك JPEG، PNG، BMP، وGIF.
### أين يمكنني العثور على الدعم الإضافي لـ Aspose.Cells؟
 يمكنك الوصول إلى منتدى الدعم لـ Aspose.Cells[هنا](https://forum.aspose.com/c/cells/9).
### كيف يمكنني الحصول على ترخيص مؤقت لـ Aspose.Cells؟
 يمكن الحصول على ترخيص مؤقت من خلال زيارة موقعهم[صفحة الترخيص المؤقت](https://purchase.aspose.com/temporary-license/).