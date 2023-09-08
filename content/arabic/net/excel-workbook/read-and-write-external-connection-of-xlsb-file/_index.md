---
title: قراءة وكتابة الاتصال الخارجي لملف XLSB
linktitle: قراءة وكتابة الاتصال الخارجي لملف XLSB
second_title: Aspose.Cells لمرجع .NET API
description: تعرف على كيفية قراءة وتعديل الاتصالات الخارجية لملف XLSB باستخدام Aspose.Cells لـ .NET.
type: docs
weight: 130
url: /ar/net/excel-workbook/read-and-write-external-connection-of-xlsb-file/
---
تعد قراءة وكتابة الاتصالات الخارجية بملف XLSB أمرًا ضروريًا لمعالجة البيانات من المصادر الخارجية في مصنفات Excel. باستخدام Aspose.Cells for .NET، يمكنك بسهولة قراءة الاتصالات الخارجية وكتابتها باستخدام الخطوات التالية:

## الخطوة 1: تحديد الدليل المصدر ودليل الإخراج

أولاً، يجب عليك تحديد الدليل المصدر حيث يوجد ملف XLSB الذي يحتوي على الاتصال الخارجي، بالإضافة إلى دليل الإخراج حيث تريد حفظ الملف المعدل. وإليك كيفية القيام بذلك باستخدام Aspose.Cells:

```csharp
// دليل المصدر
string sourceDir = RunExamples.Get_SourceDirectory();

// دليل الإخراج
string outputDir = RunExamples.Get_OutputDirectory();
```

## الخطوة 2: قم بتحميل ملف Excel XLSB المصدر

بعد ذلك، تحتاج إلى تحميل ملف Excel XLSB المصدر الذي تريد إجراء عمليات القراءة والكتابة للاتصال الخارجي عليه. هنا نموذج التعليمات البرمجية:

```csharp
// قم بتحميل ملف Excel XLSB المصدر
Workbook wb = new Workbook(sourceDir + "sampleExternalConnection_XLSB.xlsb");
```

## الخطوة 3: قراءة وتعديل الاتصال الخارجي

بعد تحميل الملف، يمكنك الوصول إلى الاتصال الخارجي الأول وهو في الواقع اتصال قاعدة البيانات. يمكنك قراءة وتعديل الخصائص المختلفة للاتصال الخارجي. إليك الطريقة:

```csharp
// اقرأ الاتصال الخارجي الأول وهو اتصال قاعدة البيانات
Aspose.Cells.ExternalConnections.DBConnection dbCon = wb.DataConnections[0] as Aspose.Cells.ExternalConnections.DBConnection;

// عرض اسم اتصال قاعدة البيانات والأمر ومعلومات الاتصال
Console.WriteLine("Connection name: " + dbCon.Name);
Console.WriteLine("Command: " + dbCon.Command);
Console.WriteLine("Connection Info: " + dbCon.ConnectionInfo);

// تعديل اسم الاتصال
dbCon.Name = "NewCustomer";
```

## الخطوة 4: احفظ ملف Excel XLSB الناتج

بمجرد إجراء التغييرات اللازمة، يمكنك حفظ ملف Excel XLSB المعدل في دليل الإخراج المحدد. هيريس كيفية القيام بذلك:

```csharp
// احفظ ملف Excel XLSB الناتج
wb.Save(outputDir + "outputExternalConnection_XLSB.xlsb");
Console.WriteLine("ReadAndWriteExternalConnectionOfXLSBFile executed successfully.\r\n");
```

### نموذج التعليمات البرمجية المصدر لقراءة وكتابة الاتصال الخارجي لملف XLSB باستخدام Aspose.Cells لـ .NET 
```csharp
//دليل المصدر
string sourceDir = RunExamples.Get_SourceDirectory();
//دليل الإخراج
string outputDir = RunExamples.Get_OutputDirectory();
//قم بتحميل ملف Excel Xlsb المصدر
Workbook wb = new Workbook(sourceDir + "sampleExternalConnection_XLSB.xlsb");
//اقرأ أول اتصال خارجي وهو في الواقع اتصال DB
Aspose.Cells.ExternalConnections.DBConnection dbCon = wb.DataConnections[0] as Aspose.Cells.ExternalConnections.DBConnection;
//اطبع الاسم والأمر ومعلومات الاتصال الخاصة باتصال DB
Console.WriteLine("Connection Name: " + dbCon.Name);
Console.WriteLine("Command: " + dbCon.Command);
Console.WriteLine("Connection Info: " + dbCon.ConnectionInfo);
//تعديل اسم الاتصال
dbCon.Name = "NewCust";
//احفظ ملف Excel XLSB
wb.Save(outputDir + "outputExternalConnection_XLSB.xlsb");
Console.WriteLine("ReadAndWriteExternalConnectionOfXLSBFile executed successfully.\r\n");
```

## خاتمة

تسمح لك قراءة وكتابة الاتصالات الخارجية بملف XLSB بمعالجة البيانات من مصادر خارجية في مصنفات Excel الخاصة بك. باستخدام Aspose.Cells for .NET، يمكنك بسهولة الوصول إلى الاتصالات الخارجية وقراءة معلومات الاتصال وتعديلها وحفظ التغييرات. قم بتجربة ملفات XLSB الخاصة بك واستفد من قوة الاتصالات الخارجية في تطبيقات Excel الخاصة بك.

### الأسئلة الشائعة

#### س: ما هو الاتصال الخارجي في ملف XLSB؟
    
ج: يشير الاتصال الخارجي في ملف XLSB إلى اتصال تم إنشاؤه باستخدام مصدر بيانات خارجي مثل قاعدة البيانات. يسمح لك باستيراد البيانات من هذا المصدر الخارجي إلى مصنف Excel.

#### س: هل يمكنني الحصول على اتصالات خارجية متعددة في ملف XLSB؟
     
ج: نعم، يمكن أن يكون لديك اتصالات خارجية متعددة في ملف XLSB. يمكنك إدارتها بشكل فردي عن طريق الوصول إلى كل كائن اتصال.

#### س: كيف يمكنني قراءة تفاصيل الاتصال الخارجي في ملف XLSB باستخدام Aspose.Cells؟
     
ج: يمكنك استخدام الوظيفة التي توفرها Aspose.Cells للوصول إلى خصائص الاتصال الخارجي، مثل اسم الاتصال والأمر المرتبط ومعلومات الاتصال.

#### س: هل من الممكن تعديل اتصال خارجي في ملف XLSB باستخدام Aspose.Cells؟
     
ج: نعم، يمكنك تعديل خصائص الاتصال الخارجي، مثل اسم الاتصال، لتلبية احتياجاتك الخاصة. يوفر Aspose.Cells طرقًا لإجراء هذه التغييرات.

#### س: كيف يمكنني حفظ التغييرات التي تم إجراؤها على اتصال خارجي بملف XLSB باستخدام Aspose.Cells؟
     
ج: بمجرد إجراء التغييرات اللازمة على الاتصال الخارجي، يمكنك ببساطة حفظ ملف Excel XLSB المعدل باستخدام الطريقة المناسبة التي يوفرها Aspose.Cells.