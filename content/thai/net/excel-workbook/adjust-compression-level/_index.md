---
title: ปรับระดับการบีบอัด
linktitle: ปรับระดับการบีบอัด
second_title: Aspose.Cells สำหรับการอ้างอิง .NET API
description: ลดขนาดของสมุดงาน Excel ของคุณโดยการปรับระดับการบีบอัดด้วย Aspose.Cells สำหรับ .NET
type: docs
weight: 50
url: /th/net/excel-workbook/adjust-compression-level/
---
ในบทช่วยสอนทีละขั้นตอนนี้ เราจะอธิบายซอร์สโค้ด C# ที่ให้มาซึ่งจะช่วยให้คุณสามารถปรับระดับการบีบอัดโดยใช้ Aspose.Cells สำหรับ .NET ทำตามขั้นตอนด้านล่างเพื่อปรับระดับการบีบอัดในสมุดงาน Excel ของคุณ

## ขั้นตอนที่ 1: ตั้งค่าไดเร็กทอรีต้นทางและเอาต์พุต

```csharp
// ไดเรกทอรีต้นทาง
string sourceDir = RunExamples.Get_SourceDirectory();
// ไดเร็กทอรีเอาต์พุต
string outDir = RunExamples.Get_OutputDirectory();
```

ในขั้นตอนแรกนี้ เราจะกำหนดไดเร็กทอรีต้นทางและเอาต์พุตสำหรับไฟล์ Excel

## ขั้นตอนที่ 2: โหลดสมุดงาน Excel

```csharp
// โหลดสมุดงาน Excel
Workbook workbook = new Workbook(sourceDir + "LargeSampleFile.xlsx");
```

เราโหลดสมุดงาน Excel จากไฟล์ที่ระบุโดยใช้`Workbook` คลาสจาก Aspose.Cells

## ขั้นตอนที่ 3: ตั้งค่าตัวเลือกการสำรองข้อมูล

```csharp
// กำหนดตัวเลือกการสำรองข้อมูล
XlsbSaveOptions options = new XlsbSaveOptions();
```

 เราสร้างอินสแตนซ์ของ`XlsbSaveOptions` คลาสเพื่อตั้งค่าตัวเลือกการบันทึก

## ขั้นตอนที่ 4: ปรับระดับการบีบอัด (ระดับ 1)

```csharp
// ปรับระดับการบีบอัด (ระดับ 1)
options.CompressionType = OoxmlCompressionType.Level1;
var watch = System.Diagnostics.Stopwatch.StartNew();
workbook.Save(outDir + "LargeSampleFile_level_1_out.xlsb", options);
watch.Stop();
let elapsedMs = watch.ElapsedMilliseconds;
Console.WriteLine("Elapsed time (Level 1): " + elapsedMs);
```

 เราปรับระดับการบีบอัดตามการตั้งค่า`CompressionType` ถึง`Level1`. จากนั้นเราจะบันทึกสมุดงาน Excel โดยระบุตัวเลือกการบีบอัดนี้

## ขั้นตอนที่ 5: ปรับระดับการบีบอัด (ระดับ 6)

```csharp
// ปรับระดับการบีบอัด (ระดับ 6)
options.CompressionType = OoxmlCompressionType.Level6;
watch = System.Diagnostics.Stopwatch.StartNew();
workbook.Save(outDir + "LargeSampleFile_level_6_out.xlsb", options);
watch.Stop();
elapsedMs = watch. ElapsedMilliseconds;
Console.WriteLine("Elapsed time (Level 6): " + elapsedMs);
```

 เราทำซ้ำขั้นตอนเพื่อปรับระดับการบีบอัดเป็น`Level6` และบันทึกสมุดงาน Excel ด้วยตัวเลือกนี้

## ขั้นตอนที่ 6: ปรับระดับการบีบอัด (ระดับ 9)

```csharp
// ปรับระดับการบีบอัด (ระดับ 9)
options.CompressionType = OoxmlCompressionType.Level9;
watch = System.Diagnostics.Stopwatch.StartNew();
workbook.Save(outDir + "LargeSampleFile_level_9_out.xlsb", options);
watch.Stop();
elapsedMs = watch. ElapsedMilliseconds;
Console.WriteLine("Elapsed time (Level 9): " + elapsedMs);
```

 เราทำซ้ำขั้นตอนนี้เป็นครั้งสุดท้ายเพื่อปรับระดับการบีบอัด`Level9` และบันทึกสมุดงาน Excel ด้วยตัวเลือกนี้

### ตัวอย่างซอร์สโค้ดสำหรับการปรับระดับการบีบอัดโดยใช้ Aspose.Cells สำหรับ .NET 
```csharp
//ไดเรกทอรีต้นทาง
string sourceDir = RunExamples.Get_SourceDirectory();
string outDir = RunExamples.Get_OutputDirectory();
Workbook workbook = new Workbook(sourceDir + "LargeSampleFile.xlsx");
XlsbSaveOptions options = new XlsbSaveOptions();
options.CompressionType = OoxmlCompressionType.Level1;
var watch = System.Diagnostics.Stopwatch.StartNew();
workbook.Save(outDir + "LargeSampleFile_level_1_out.xlsb", options);
watch.Stop();
var elapsedMs = watch.ElapsedMilliseconds;
Console.WriteLine("Level 1 Elapsed Time: " + elapsedMs);
watch = System.Diagnostics.Stopwatch.StartNew();
options.CompressionType = OoxmlCompressionType.Level6;
workbook.Save(outDir + "LargeSampleFile_level_6_out.xlsb", options);
watch.Stop();
elapsedMs = watch.ElapsedMilliseconds;
Console.WriteLine("Level 6 Elapsed Time: " + elapsedMs);
watch = System.Diagnostics.Stopwatch.StartNew();
options.CompressionType = OoxmlCompressionType.Level9;
workbook.Save(outDir + "LargeSampleFile_level_9_out.xlsb", options);
watch.Stop();
elapsedMs = watch.ElapsedMilliseconds;
Console.WriteLine("Level 9 Elapsed Time: " + elapsedMs);
Console.WriteLine("AdjustCompressionLevel executed successfully.");
```

## บทสรุป

ขอแสดงความยินดี! คุณได้เรียนรู้วิธีปรับระดับการบีบอัดในสมุดงาน Excel โดยใช้ Aspose.Cells for .NET ทดลองใช้การบีบอัดในระดับต่างๆ เพื่อค้นหาการบีบอัดที่เหมาะกับความต้องการของคุณมากที่สุด

### คำถามที่พบบ่อย

#### ถาม: การบีบอัดในสมุดงาน Excel คืออะไร

ตอบ: การบีบอัดในเวิร์กบุ๊ก Excel เป็นกระบวนการลดขนาดไฟล์โดยใช้อัลกอริทึมการบีบอัด ซึ่งจะช่วยลดพื้นที่จัดเก็บข้อมูลที่จำเป็นและปรับปรุงประสิทธิภาพเมื่อโหลดและจัดการไฟล์

#### ถาม: Aspose.Cells มีการบีบอัดระดับใดบ้าง

ตอบ: ด้วย Aspose.Cells คุณสามารถปรับระดับการบีบอัดได้ตั้งแต่ 1 ถึง 9 ยิ่งระดับการบีบอัดสูง ขนาดไฟล์ก็จะเล็กลง แต่ก็อาจเพิ่มเวลาการประมวลผลได้เช่นกัน

#### ถาม: ฉันจะเลือกระดับการบีบอัดที่เหมาะสมสำหรับสมุดงาน Excel ของฉันได้อย่างไร

ตอบ: การเลือกระดับแรงอัดขึ้นอยู่กับความต้องการเฉพาะของคุณ หากคุณต้องการให้การบีบอัดสูงสุดและเวลาในการประมวลผลไม่เป็นปัญหา คุณสามารถไปที่ระดับ 9 ได้ หากคุณต้องการลดขนาดไฟล์และเวลาในการประมวลผล คุณสามารถเลือกระดับกลางได้

#### ถาม: การบีบอัดส่งผลต่อคุณภาพของข้อมูลในเวิร์กบุ๊ก Excel หรือไม่

ตอบ: ไม่ การบีบอัดจะไม่ส่งผลต่อคุณภาพข้อมูลในสมุดงาน Excel เพียงลดขนาดไฟล์โดยใช้เทคนิคการบีบอัดโดยไม่ต้องเปลี่ยนแปลงข้อมูล

#### ถาม: ฉันสามารถปรับระดับการบีบอัดหลังจากบันทึกไฟล์ Excel ได้หรือไม่

ตอบ: ไม่ เมื่อคุณบันทึกไฟล์ Excel ด้วยระดับการบีบอัดที่กำหนด คุณจะไม่สามารถปรับระดับการบีบอัดในภายหลังได้ คุณจะต้องบันทึกไฟล์อีกครั้งด้วยระดับการบีบอัดใหม่หากคุณต้องการแก้ไข