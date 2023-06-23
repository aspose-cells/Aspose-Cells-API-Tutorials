---
title: تحديث عنصر صيغة Power Query
linktitle: تحديث عنصر صيغة Power Query
second_title: Aspose.Cells لمرجع .NET API
description: تعرف على كيفية تحديث عناصر صيغة Power Query في ملفات Excel باستخدام Aspose.Cells for .NET.
type: docs
weight: 160
url: /ar/net/excel-workbook/update-power-query-formula-item/
---
يعد تحديث عنصر صيغة Power Query عملية شائعة عند العمل مع البيانات في ملفات Excel. باستخدام Aspose.Cells for .NET ، يمكنك بسهولة تحديث عنصر صيغة Power Query باتباع الخطوات التالية:

## الخطوة 1: حدد أدلة المصدر والمخرجات

أولاً ، تحتاج إلى تحديد دليل المصدر حيث يوجد ملف Excel الذي يحتوي على صيغ Power Query لتحديثها ، بالإضافة إلى دليل الإخراج حيث تريد حفظ الملف المعدل. إليك كيفية القيام بذلك باستخدام Aspose.Cells:

```csharp
// دليل المصدر
string SourceDir = RunExamples.Get_SourceDirectory();

// دليل الإخراج
string outputDir = RunExamples.Get_OutputDirectory();
```

## الخطوة 2: قم بتحميل مصنف Excel المصدر

بعد ذلك ، تحتاج إلى تحميل مصنف Excel المصدر الذي تريد تحديث عنصر صيغة Power Query عليه. هيريس كيفية القيام بذلك:

```csharp
// قم بتحميل مصنف Excel المصدر
Workbook workbook = new Workbook(SourceDir + "SamplePowerQueryFormula.xlsx");
```

## الخطوة 3: استعراض وتحديث عناصر صيغة Power Query

بعد تحميل المصنف ، يمكنك الانتقال إلى مجموعة صيغ Power Query واستعراض كل صيغة وعناصرها. في هذا المثال ، نبحث عن عنصر الصيغة باسم "Source" ونقوم بتحديث قيمته. فيما يلي نموذج للتعليمة البرمجية لتحديث عنصر صيغة Power Query:

```csharp
// قم بالوصول إلى مجموعة صيغ Power Query
DataMashup mashupData = workbook.DataMashup;

// تكرار عبر صيغ Power Query وعناصرها
foreach(PowerQueryFormula formula in mashupData.PowerQueryFormulas)
{
     foreach(PowerQueryFormulaItem item in formula.PowerQueryFormulaItems)
     {
         if (item.Name == "Source")
         {
             item.Value = "Excel.Workbook(File.Contents(\"" + SourceDir + "SamplePowerQueryFormulaSource.xlsx\"), null, true)";
         }
     }
}
```

## الخطوة 4: احفظ مصنف Excel الناتج

بمجرد تحديث عنصر صيغة Power Query ، يمكنك حفظ مصنف Excel المعدل في دليل الإخراج المحدد. هيريس كيفية القيام بذلك:

```csharp
// احفظ مصنف Excel الناتج
workbook.Save(outputDir + "SamplePowerQueryFormula_out.xlsx");
Console.WriteLine("UpdatePowerQueryFormulaItem executed successfully.\r\n");
```

### نموذج التعليمات البرمجية المصدر لتحديث عنصر صيغة Power Query باستخدام Aspose.Cells لـ .NET 
```csharp
// أدلة العمل
string SourceDir = RunExamples.Get_SourceDirectory();
string outputDir = RunExamples.Get_OutputDirectory();
Workbook workbook = new Workbook(SourceDir + "SamplePowerQueryFormula.xlsx");
DataMashup mashupData = workbook.DataMashup;
foreach (PowerQueryFormula formula in mashupData.PowerQueryFormulas)
{
	foreach (PowerQueryFormulaItem item in formula.PowerQueryFormulaItems)
	{
		if (item.Name == "Source")
		{
			item.Value = "Excel.Workbook(File.Contents(\"" + SourceDir + "SamplePowerQueryFormulaSource.xlsx\"), null, true)";
		}
	}
}
// احفظ مصنف الإخراج.
workbook.Save(outputDir + "SamplePowerQueryFormula_out.xlsx");
Console.WriteLine("UpdatePowerQueryFormulaItem executed successfully.");
```

## خاتمة

يعد تحديث عناصر صيغة Power Query عملية أساسية عند استخدام Aspose.Cells لمعالجة البيانات ومعالجتها في ملفات Excel. باتباع الخطوات المذكورة أعلاه ، يمكنك بسهولة تحديث عناصر الصيغة

### أسئلة وأجوبة

#### س: ما هو Power Query في Excel؟
     
ج: Power Query هي ميزة في Excel تساعد في تجميع البيانات وتحويلها وتحميلها من مصادر مختلفة. يوفر أدوات قوية لتنظيف البيانات ودمجها وإعادة تشكيلها قبل استيرادها إلى Excel.

#### س: كيف يمكنني معرفة ما إذا تم تحديث عنصر صيغة Power Query بنجاح؟
    A: After running the Power Query Formula Item Update, you can check if the operation was successful by viewing the output and ensuring that the output Excel file was created correctly.

#### س: هل يمكنني تحديث عدة عناصر صيغة Power Query مرة واحدة؟
    
ج: نعم ، يمكنك إجراء تكرار عبر مجموعة عناصر صيغة Power Query وتحديث عناصر متعددة في حلقة واحدة ، وفقًا لاحتياجاتك الخاصة.

#### س: هل هناك عمليات أخرى يمكنني إجراؤها على صيغ Power Query باستخدام Aspose.Cells؟
    
ج: نعم ، تقدم Aspose.Cells مجموعة كاملة من الميزات للعمل مع صيغ Power Query ، بما في ذلك إنشاء الصيغ وحذفها ونسخها والبحث عنها في مصنف Excel.