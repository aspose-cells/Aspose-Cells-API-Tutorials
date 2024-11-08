---
title: استخراج ملف Mol المضمن من المصنف
linktitle: استخراج ملف Mol المضمن من المصنف
second_title: واجهة برمجة تطبيقات معالجة Excel الخاصة بـ Aspose.Cells .NET
description: تعرف على كيفية استخراج ملفات MOL المضمنة من مصنفات Excel باستخدام Aspose.Cells لـ .NET في هذا البرنامج التعليمي المفصل خطوة بخطوة.
type: docs
weight: 18
url: /ar/net/workbook-operations/extract-embedded-mol-file/
---
## مقدمة
عندما يتعلق الأمر بإدارة البيانات داخل مصنفات Excel، قد تواجه أحيانًا كائنات مضمنة مختلفة ليست بتنسيق قياسي. أحد هذه التنسيقات هو MOL (ملف البنية الجزيئية)، والذي يُستخدم عادةً في الكيمياء لتمثيل المعلومات الجزيئية. إذا كنت تتطلع إلى استخراج ملفات MOL هذه من مصنف Excel باستخدام Aspose.Cells for .NET، فقد وصلت إلى الدليل الصحيح. في هذه المقالة، سنرشدك خلال العملية خطوة بخطوة، ونزيل الغموض عن كل جزء على طول الطريق.
## المتطلبات الأساسية
قبل التعمق في الكود، من الضروري التأكد من امتلاكك للمهارات والأدوات اللازمة. إليك ما ستحتاج إليه:
1. الفهم الأساسي لبرمجة .NET: يجب أن تكون على دراية بلغة C# وإطار عمل .NET.
2.  Aspose.Cells لـ .NET: تأكد من أن لديك مكتبة Aspose.Cells. يمكنك[تحميله هنا](https://releases.aspose.com/cells/net/).
3. IDE: يمكنك استخدام Visual Studio أو أي IDE آخر متوافق مع .NET.
4. مصنف Excel مع ملفات MOL المضمنة: لهذا البرنامج التعليمي، ستحتاج إلى ملف Excel يحتوي على كائنات MOL. يمكنك إنشاء ملفك الخاص أو استخدام أي ملف عينة.
## استيراد الحزم
للبدء، ستحتاج إلى استيراد مساحات الأسماء الضرورية في مشروعك. وهذا أمر بالغ الأهمية للوصول إلى وظائف Aspose.Cells. وإليك كيفية القيام بذلك:

```csharp
using Aspose.Cells.Drawing;
using Aspose.Cells.WebExtensions;
using System;
using System.IO;
```

ستسمح لك هذه المساحات الاسمية بالتعامل مع مصنفات العمل، والوصول إلى أوراق العمل، والعمل مع الملفات بشكل عام.
الآن بعد أن قمنا بترتيب المتطلبات الأساسية، دعنا نتعمق في الكود ونفهم كل خطوة متضمنة في استخراج ملفات MOL المضمنة من مصنف Excel. 
## الخطوة 1: إعداد الدلائل الخاصة بك
الخطوة الأولى هي تحديد مكان وجود مستند المصدر والمكان الذي تريد حفظ ملفات MOL المستخرجة فيه. دعنا ننشئ هذه الدلائل.
```csharp
string SourceDir = "Your Document Directory"; // استبدله بمسار الدليل الخاص بك
string outputDir = "Your Document Directory"; // استبدل بمسار الإخراج الخاص بك
```
 هنا، يمكنك استبدال`"Your Document Directory"`مع المسار إلى الدلائل الفعلية لديك. من المهم أن يكون كل من الدلائل المصدر والإخراج قابلة للوصول إلى تطبيقك.
## الخطوة 2: تحميل المصنف
بمجرد إعداد الدلائل، فإن المهمة التالية هي تحميل مصنف Excel. فلنفعل ذلك الآن.

```csharp
Workbook workbook = new Workbook(SourceDir + "EmbeddedMolSample.xlsx");
```

 نحن نقوم بإنشاء مثيل لـ`Workbook` الفئة وتمرير المسار إلى ملف Excel الخاص بنا المسمى`EmbeddedMolSample.xlsx`تؤدي هذه الخطوة إلى تهيئة المصنف، مما يسمح لك بالوصول إلى محتوياته.
## الخطوة 3: تكرار أوراق العمل
الآن بعد تحميل المصنف، يتعين عليك المرور عبر كل ورقة عمل داخل المصنف. يتيح لك هذا فحص كل ورقة بحثًا عن الكائنات المضمنة.

```csharp
var index = 1; // يستخدم لتسمية ملفات MOL المستخرجة
foreach (Worksheet sheet in workbook.Worksheets)
{
    OleObjectCollection oles = sheet.OleObjects;
    // مزيد من منطق الاستخراج يذهب هنا
}
```

 هنا، أنت تستخدم`foreach` حلقة للتنقل عبر أوراق العمل. لكل ورقة عمل، يمكنك الوصول إلى`OleObjects` المجموعة التي تحتوي على كافة الكائنات المضمنة.
## الخطوة 4: استخراج ملفات MOL
الآن يأتي الجزء الحاسم - استخراج ملفات MOL من كائنات OLE. يتطلب هذا حلقة أخرى داخل حلقة ورقة العمل.

```csharp
foreach (OleObject ole in oles)
{
    string fileName = outputDir + "OleObject" + index + ".mol ";
    FileStream fs = File.Create(fileName);
    fs.Write(ole.ObjectData, 0, ole.ObjectData.Length);
    fs.Close();
    index++;
}
```

 بالنسبة لكل كائن OLE تجده، فإنك تقوم بإنشاء ملف جديد في دليل الإخراج.`ObjectData` ممتلكات`OleObject` يحتفظ ببيانات الكائن المضمن، والتي تكتبها في ملف تم إنشاؤه حديثًا باستخدام`FileStream`. يتم تسمية الملف بشكل تسلسلي (`OleObject1.mol`, `OleObject2.mol` ، إلخ) بناءً على`index` عامل.
## الخطوة 5: تأكيد اكتمال العملية
أخيرًا، بمجرد استخراج كافة ملفات MOL، من الجيد إعلام المستخدم بأن العملية اكتملت بنجاح.

```csharp
Console.WriteLine("ExtractEmbeddedMolFile executed successfully.");
```

يقوم هذا السطر ببساطة بطباعة رسالة إلى وحدة التحكم لإعلامك بنجاح عملية الاستخراج. إنها لمسة لطيفة لملاحظات المستخدم.
## خاتمة
والآن، لقد نجحت في استخراج ملفات MOL المضمنة من مصنف Excel باستخدام Aspose.Cells for .NET. تدمج هذه العملية بضع خطوات أساسية، مما يضمن اتباع نهج منظم للتعامل مع الكائنات المضمنة. سواء كنت تعمل في مجال البحث العلمي أو التحليل الكيميائي أو تتعامل ببساطة مع مجموعات بيانات معقدة، فإن القدرة على استخراج هذه الأنواع من الملفات ومعالجتها يمكن أن تحدث فرقًا كبيرًا في كيفية إدارة معلوماتك. 
## الأسئلة الشائعة
### هل يمكنني استخراج أنواع ملفات أخرى غير MOL من Excel؟
نعم، يمكنك استخراج أنواع أخرى مختلفة من الملفات المضمنة باستخدام تقنيات مماثلة.
### هل استخدام Aspose.Cells مجاني؟
 Aspose.Cells هي مكتبة تجارية، ولكن يمكنك[جربه مجانًا لفترة محدودة](https://releases.aspose.com/).
### هل تعمل هذه الطريقة مع جميع إصدارات Excel؟
نعم، طالما أن تنسيق الملف مدعوم بواسطة Aspose.Cells.
### هل يمكنني أتمتة عملية الاستخراج هذه؟
بالتأكيد! يمكنك أتمتة هذه العملية عن طريق وضع الكود في مهمة مجدولة أو نص برمجي.
### أين يمكنني العثور على مزيد من الوثائق حول Aspose.Cells؟
 يمكنك التحقق من[توثيق Aspose.Cells](https://reference.aspose.com/cells/net/) لمزيد من التفاصيل والأمثلة.