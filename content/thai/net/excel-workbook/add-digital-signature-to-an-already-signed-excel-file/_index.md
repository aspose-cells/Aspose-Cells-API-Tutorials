---
title: เพิ่มลายเซ็นดิจิทัลลงในไฟล์ Excel ที่ลงนามแล้ว
linktitle: เพิ่มลายเซ็นดิจิทัลลงในไฟล์ Excel ที่ลงนามแล้ว
second_title: Aspose.Cells สำหรับการอ้างอิง .NET API
description: เพิ่มลายเซ็นดิจิทัลลงในไฟล์ Excel ที่มีอยู่ได้อย่างง่ายดายด้วย Aspose.Cells สำหรับ .NET
type: docs
weight: 30
url: /th/net/excel-workbook/add-digital-signature-to-an-already-signed-excel-file/
---
ในคำแนะนำทีละขั้นตอนนี้ เราจะอธิบายซอร์สโค้ด C# ที่ให้มาซึ่งจะช่วยให้คุณเพิ่มลายเซ็นดิจิทัลลงในไฟล์ Excel ที่ลงนามแล้วโดยใช้ Aspose.Cells สำหรับ .NET ทำตามขั้นตอนด้านล่างเพื่อเพิ่มลายเซ็นดิจิทัลใหม่ให้กับไฟล์ Excel ที่มีอยู่

## ขั้นตอนที่ 1: ตั้งค่าไดเร็กทอรีต้นทางและเอาต์พุต

```csharp
// ไดเรกทอรีต้นทาง
string sourceDir = RunExamples.Get_SourceDirectory();

// ไดเร็กทอรีเอาต์พุต
string outputDir = RunExamples.Get_OutputDirectory();
```

ในขั้นตอนแรกนี้ เรากำหนดไดเร็กทอรีต้นทางและเอาต์พุตที่จะใช้ในการโหลดไฟล์ Excel ที่มีอยู่และบันทึกไฟล์ด้วยลายเซ็นดิจิทัลใหม่

## ขั้นตอนที่ 2: โหลดไฟล์ Excel ที่มีอยู่

```csharp
// โหลดสมุดงาน Excel ที่ลงนามแล้ว
Aspose.Cells.Workbook workbook = new Aspose.Cells.Workbook(sourceDir + "sampleDigitallySignedByCells.xlsx");
```

 ที่นี่เราโหลดไฟล์ Excel ที่ลงนามแล้วโดยใช้ไฟล์`Workbook` คลาสของ Aspose.Cells

## ขั้นตอนที่ 3: สร้างคอลเลกชันของลายเซ็นดิจิทัล

```csharp
// สร้างคอลเลกชันของลายเซ็นดิจิทัล
Aspose.Cells.DigitalSignatures.DigitalSignatureCollection dsCollection = new Aspose.Cells.DigitalSignatures.DigitalSignatureCollection();
```

 เราสร้างคอลเลกชันลายเซ็นดิจิทัลใหม่โดยใช้`DigitalSignatureCollection` ระดับ.

## ขั้นตอนที่ 4: สร้างใบรับรองใหม่

```csharp
// สร้างใบรับรองใหม่
System.Security.Cryptography.X509Certificates.X509Certificate2 certificate = new System.Security.Cryptography.X509Certificates.X509Certificate2(certFileName, password);
```

ที่นี่เราสร้างใบรับรองใหม่จากไฟล์และรหัสผ่านที่ให้มา

## ขั้นตอนที่ 5: เพิ่มลายเซ็นดิจิทัลใหม่ให้กับคอลเลกชัน

```csharp
// สร้างลายเซ็นดิจิทัลใหม่
Aspose.Cells.DigitalSignatures.DigitalSignature signature = new Aspose.Cells.DigitalSignatures.DigitalSignature(certificate, "Aspose.Cells added a new digital signature to the already signed workbook.", DateTime.Now);

// เพิ่มลายเซ็นดิจิทัลลงในคอลเลกชัน
dsCollection.Add(signature);
```

 เราสร้างลายเซ็นดิจิทัลใหม่โดยใช้`DigitalSignature` และเพิ่มลงในคอลเลกชันลายเซ็นดิจิทัล

## ขั้นตอนที่ 6: เพิ่มคอลเลกชันของลายเซ็นดิจิทัลลงในสมุดงาน

```csharp
//เพิ่มคอลเลกชันของลายเซ็นดิจิทัลลงในเวิร์กบุ๊ก
workbook.AddDigitalSignature(dsCollection);
```

 เราเพิ่มคอลเลกชันของลายเซ็นดิจิทัลลงในสมุดงาน Excel ที่มีอยู่โดยใช้`AddDigitalSignature()` วิธี.

## ขั้นตอนที่ 7: บันทึกและปิดสมุดงาน

```csharp
// บันทึกสมุดงานและปิด
workbook.Save(outputDir + "outputDigitallySignedByCells.xlsx");
workbook.Dispose();
```

เราบันทึกสมุดงานด้วยลายเซ็นดิจิทัลใหม่ลงในไดเร็กทอรีเอาต์พุตที่ระบุ จากนั้นปิดและปล่อยทรัพยากรที่เกี่ยวข้อง

### ตัวอย่างซอร์สโค้ดสำหรับเพิ่มลายเซ็นดิจิทัลลงในไฟล์ Excel ที่ลงนามแล้วโดยใช้ Aspose.Cells สำหรับ .NET 
```csharp
//ไดเรกทอรีต้นทาง
string sourceDir = RunExamples.Get_SourceDirectory();
//ไดเร็กทอรีเอาต์พุต
string outputDir = RunExamples.Get_OutputDirectory();
//ไฟล์ใบรับรองและรหัสผ่าน
string certFileName = sourceDir + "AsposeDemo.pfx";
string password = "aspose";
//โหลดเวิร์กบุ๊กที่มีการเซ็นชื่อแบบดิจิทัลแล้วเพื่อเพิ่มลายเซ็นดิจิทัลใหม่
Aspose.Cells.Workbook workbook = new Aspose.Cells.Workbook(sourceDir + "sampleDigitallySignedByCells.xlsx");
//สร้างคอลเลกชันลายเซ็นดิจิทัล
Aspose.Cells.DigitalSignatures.DigitalSignatureCollection dsCollection = new Aspose.Cells.DigitalSignatures.DigitalSignatureCollection();
//สร้างใบรับรองใหม่
System.Security.Cryptography.X509Certificates.X509Certificate2 certificate = new System.Security.Cryptography.X509Certificates.X509Certificate2(certFileName, password);
//สร้างลายเซ็นดิจิทัลใหม่และเพิ่มลงในคอลเลกชันลายเซ็นดิจิทัล
Aspose.Cells.DigitalSignatures.DigitalSignature signature = new Aspose.Cells.DigitalSignatures.DigitalSignature(certificate, "Aspose.Cells added new digital signature in existing digitally signed workbook.", DateTime.Now);
dsCollection.Add(signature);
//เพิ่มคอลเลกชันลายเซ็นดิจิทัลภายในสมุดงาน
workbook.AddDigitalSignature(dsCollection);
//บันทึกสมุดงานและกำจัดทิ้ง
workbook.Save(outputDir + "outputDigitallySignedByCells.xlsx");
workbook.Dispose();
Console.WriteLine("AddDigitalSignatureToAnAlreadySignedExcelFile executed successfully.\r\n");
```

## บทสรุป

ขอแสดงความยินดี! ตอนนี้คุณได้เรียนรู้วิธีเพิ่มลายเซ็นดิจิทัลลงในไฟล์ Excel ที่ลงนามแล้วโดยใช้ Aspose.Cells สำหรับ .NET ลายเซ็นดิจิทัลช่วยเพิ่มความปลอดภัยอีกชั้นให้กับไฟล์ Excel ของคุณ ทำให้มั่นใจถึงความถูกต้องและความสมบูรณ์ของไฟล์

### คำถามที่พบบ่อย

#### ถาม: Aspose.Cells สำหรับ .NET คืออะไร

ตอบ: Aspose.Cells for .NET เป็นไลบรารีคลาสที่มีประสิทธิภาพซึ่งช่วยให้นักพัฒนา .NET สามารถสร้าง แก้ไข แปลง และจัดการไฟล์ Excel ได้อย่างง่ายดาย

#### ถาม: ลายเซ็นดิจิทัลในไฟล์ Excel คืออะไร

ตอบ: ลายเซ็นดิจิทัลในไฟล์ Excel คือเครื่องหมายอิเล็กทรอนิกส์ที่รับประกันความถูกต้อง ความสมบูรณ์ และที่มาของเอกสาร ใช้เพื่อตรวจสอบว่าไฟล์ไม่ได้รับการแก้ไขนับตั้งแต่ลงนามและมาจากแหล่งที่เชื่อถือได้

#### ถาม: การเพิ่มลายเซ็นดิจิทัลลงในไฟล์ Excel มีประโยชน์อย่างไร

ตอบ: การเพิ่มลายเซ็นดิจิทัลลงในไฟล์ Excel ให้ประโยชน์หลายประการ รวมถึงการป้องกันการเปลี่ยนแปลงที่ไม่ได้รับอนุญาต การรับรองความสมบูรณ์ของข้อมูล การรับรองความถูกต้องของผู้เขียนเอกสาร และการให้ความมั่นใจในข้อมูลที่มีอยู่

#### ถาม: ฉันสามารถเพิ่มลายเซ็นดิจิทัลหลายรายการลงในไฟล์ Excel ได้หรือไม่

ตอบ: ได้ Aspose.Cells ช่วยให้คุณสามารถเพิ่มลายเซ็นดิจิทัลหลายรายการลงในไฟล์ Excel ได้ คุณสามารถสร้างคอลเลกชันของลายเซ็นดิจิทัลและเพิ่มลงในไฟล์ได้ในการดำเนินการครั้งเดียว

#### ถาม: ข้อกำหนดในการเพิ่มลายเซ็นดิจิทัลลงในไฟล์ Excel มีอะไรบ้าง

ตอบ: หากต้องการเพิ่มลายเซ็นดิจิทัลลงในไฟล์ Excel คุณต้องมีใบรับรองดิจิทัลที่ถูกต้องซึ่งจะใช้ในการลงนามในเอกสาร ตรวจสอบให้แน่ใจว่าคุณมีใบรับรองและรหัสผ่านที่ถูกต้องก่อนที่จะเพิ่มลายเซ็นดิจิทัล