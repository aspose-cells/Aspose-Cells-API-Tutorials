---
title: تعيين نوع شكل تسميات البيانات للرسم البياني
linktitle: تعيين نوع شكل تسميات البيانات للرسم البياني
second_title: واجهة برمجة تطبيقات معالجة Excel الخاصة بـ Aspose.Cells .NET
description: قم بتعزيز مخططات Excel الخاصة بك باستخدام أشكال تسميات البيانات المخصصة باستخدام Aspose.Cells for .NET. اتبع هذا الدليل خطوة بخطوة لرفع مستوى عرض البيانات لديك.
type: docs
weight: 14
url: /ar/net/advanced-chart-operations/set-shape-type-of-data-labels-of-chart/
---
## مقدمة

في عالم تصور البيانات، تعد المخططات البيانية طريقة أساسية لتقديم معلومات معقدة بطريقة سهلة الوصول. ومع ذلك، لا يتم إنشاء جميع تسميات البيانات على قدم المساواة! في بعض الأحيان، تحتاج إلى إبراز هذه التسميات، واستخدام أشكال مختلفة يمكن أن يحدث فرقًا كبيرًا. إذا كنت تتطلع إلى تحسين تسميات البيانات في مخططات Excel الخاصة بك باستخدام أشكال مخصصة، فقد وصلت إلى المكان الصحيح. سيرشدك هذا الدليل إلى كيفية تعيين نوع شكل تسميات البيانات في مخطط باستخدام Aspose.Cells لـ .NET. دعنا نتعمق في الأمر!

## المتطلبات الأساسية

قبل أن نبدأ في الترميز، دعنا نتأكد من إعداد كل شيء بشكل صحيح. إليك ما ستحتاج إليه:

1.  Aspose.Cells لـ .NET: إذا لم تقم بتنزيله بالفعل، فقم بتنزيله من[موقع اسبوس](https://releases.aspose.com/cells/net/)تتيح لك هذه المكتبة إجراء كافة أنواع التلاعبات بمستندات Excel.
2. Visual Studio: يجب أن يكون مثبتًا على نظامك لكتابة وتشغيل تطبيقات .NET. تأكد من أن الإصدار يدعم .NET Framework أو .NET Core وفقًا لاحتياجات مشروعك.
3. فهم أساسي للغة C#: إن الإلمام بمفاهيم البرمجة الأساسية وقواعد لغة C# سيساعدك بالتأكيد على فهم مقتطفات التعليمات البرمجية بشكل أفضل.
4. ملف Excel: ستحتاج أيضًا إلى مصنف Excel نموذجي للعمل عليه. يمكنك إنشاء مصنفك الخاص أو استخدام أي مصنف موجود.

الآن بعد أن حصلنا على المتطلبات الأساسية، فلننتقل مباشرة إلى الموضوع!

## استيراد الحزم

قبل أن تتمكن من البدء في الترميز، تحتاج إلى استيراد مساحات الأسماء ذات الصلة في Aspose.Cells. سيمنحك هذا إمكانية الوصول إلى الوظائف الغنية التي تقدمها المكتبة. وإليك كيفية القيام بذلك:

### استيراد Aspose.Cells

افتح مشروع Visual Studio الخاص بك، وأضف التوجيه التالي باستخدام إلى أعلى ملف C# الخاص بك:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;

using Aspose.Cells.Charts;
using Aspose.Cells.Drawing;
```

ستتيح لك هذه المساحات الاسمية إنشاء المصنفات وأوراق العمل والمخططات ومعالجتها بسهولة.

الآن بعد أن قمنا بإعداد كل شيء، فلننتقل إلى الجزء المتعلق بالترميز! سنقوم بتقسيمه خطوة بخطوة من أجل التوضيح.

## الخطوة 1: قم بتحديد الدلائل الخاصة بك

أولاً وقبل كل شيء، دعنا نحدد مكان وجود ملفاتك - ملف المصدر ومجلد الوجهة الذي تريد حفظ الملف المعدل فيه.

```csharp
// دليل المصدر
string sourceDir = "Your Document Directory";

// دليل الإخراج
string outputDir = "Your Output Directory";
```

 يستبدل`"Your Document Directory"` و`"Your Output Directory"` مع المسارات الفعلية على جهازك.

## الخطوة 2: تحميل ملف Excel المصدر

بعد ذلك، ستحتاج إلى تحميل ملف Excel الذي تريد العمل به. وهنا تبدأ السحر!

```csharp
// تحميل ملف Excel المصدر
Workbook wb = new Workbook(sourceDir + "sampleSetShapeTypeOfDataLabelsOfChart.xlsx");
```

 هذا الخط ينشئ خطًا جديدًا`Workbook` الكائن ويشير إليه بالملف الموجود لديك. تأكد من أن مسار الملف صحيح!

## الخطوة 3: الوصول إلى ورقة العمل الأولى

الآن بعد أن أصبح لدينا المصنف، نحتاج إلى الوصول إلى ورقة العمل التي تحتوي على الرسم البياني الذي نريد تخصيصه.

```csharp
// الوصول إلى ورقة العمل الأولى
Worksheet ws = wb.Worksheets[0];
```

 هنا، نقوم بالوصول إلى ورقة العمل الأولى (الفهرس`0`). اضبط الفهرس إذا كان الرسم البياني الخاص بك موجودًا على ورقة مختلفة.

## الخطوة 4: الوصول إلى الرسم البياني الأول

بمجرد حصولك على ورقة العمل، حان الوقت للوصول إلى المخطط. يمكن أن تحتوي كل ورقة عمل على مخططات متعددة، ولكن من أجل التبسيط، سنلتزم بالمخطط الأول هنا.

```csharp
// الوصول إلى الرسم البياني الأول
Chart ch = ws.Charts[0];
```

مرة أخرى، إذا لم يكن الرسم البياني المطلوب هو الرسم الأول، فما عليك سوى تغيير المؤشر وفقًا لذلك.

## الخطوة 5: الوصول إلى سلسلة المخططات

مع إمكانية الوصول إلى الرسم البياني الآن، يتعين عليك التعمق أكثر لتعديل تسميات البيانات. تمثل السلسلة نقاط البيانات في الرسم البياني الخاص بك.

```csharp
// الوصول إلى السلسلة الأولى
Series srs = ch.NSeries[0];
```

نحن نستهدف السلسلة الأولى هنا، والتي تحتوي عادةً على العلامات التي قد ترغب في تعديلها.

## الخطوة 6: تعيين نوع شكل تسميات البيانات

الآن حان الوقت للجزء الحاسم! فلنقم بتعيين نوع شكل تسميات البيانات. يدعم Aspose.Cells أشكالاً مختلفة، وفي هذا المثال، سنختار شكل فقاعة كلام بيضاوية لإضفاء لمسة مرحة.

```csharp
// تعيين نوع شكل تسميات البيانات، أي فقاعة الكلام البيضاوية
srs.DataLabels.ShapeType = DataLabelShapeType.WedgeEllipseCallout;
```

 لا تتردد في تجربة أنواع مختلفة من الأشكال عن طريق التغيير`DataLabelShapeType.WedgeEllipseCallout` إلى الخيارات الأخرى المتاحة!

## الخطوة 7: احفظ ملف Excel الناتج

لقد قمت بالعمل الشاق، والآن حان وقت حفظ عملك. دعنا نضع شكل تسمية البيانات المعدلة مرة أخرى في ملف Excel.

```csharp
// حفظ ملف Excel الناتج
wb.Save(outputDir + "outputSetShapeTypeOfDataLabelsOfChart.xlsx");
```

سيؤدي هذا إلى حفظ المصنف المعدل في دليل الإخراج المحدد.

## الخطوة 8: التنفيذ والتأكيد

أخيرًا، حان وقت تشغيل البرنامج. بعد التنفيذ، يجب أن ترى الرسالة التي تؤكد أن كل شيء سار بسلاسة!

```csharp
Console.WriteLine("SetShapeTypeOfDataLabelsOfChart executed successfully.");
```

بمجرد رؤية هذه الرسالة، انتقل إلى دليل الإخراج للتحقق من ملف Excel الجديد. افتحه وأطلق العنان لإبداعك باستخدام تسميات البيانات ذات الشكل الجديد!

## خاتمة

والآن لديك دليل واضح لتحسين تسميات البيانات في مخططات Excel باستخدام Aspose.Cells لـ .NET! إن تخصيص أنواع الأشكال لا يجعل مخططاتك أكثر جاذبية بصريًا فحسب، بل يساعد أيضًا في نقل قصة بياناتك بشكل أكثر فعالية. تذكر أن تصور البيانات يتعلق بالوضوح والمشاركة. لذا، لا تتردد في اللعب بأشكال وأنماط مختلفة - ففي النهاية، تستحق بياناتك أفضل عرض.

## الأسئلة الشائعة

### ما هو Aspose.Cells؟  
Aspose.Cells عبارة عن مكتبة .NET قوية تتيح للمطورين التعامل مع ملفات Excel برمجيًا.

### هل يمكنني تغيير جوانب مختلفة من مخطط Excel باستخدام Aspose؟  
بالتأكيد! يوفر Aspose.Cells وظائف واسعة النطاق لتعديل المخططات، بما في ذلك سلاسل البيانات، والعلامات، والأنماط، والمزيد.

### ما هي لغات البرمجة التي يمكنني استخدامها مع Aspose.Cells؟  
في حين تركز هذه المقالة على .NET، فإن Aspose.Cells يدعم أيضًا Java وPHP وPython والمزيد عبر واجهات برمجة التطبيقات REST.

### هل أحتاج إلى الدفع مقابل Aspose.Cells؟  
Aspose.Cells هو منتج تجاري، لكنه يقدم نسخة تجريبية مجانية، والتي يمكنك العثور عليها[هنا](https://releases.aspose.com/).

### أين يمكنني الحصول على المساعدة إذا واجهت مشاكل مع Aspose.Cells؟  
 إذا واجهت أي مشاكل،[منتدى الدعم](https://forum.aspose.com/c/cells/9) يعد مصدرًا رائعًا للحصول على المساعدة من الخبراء.