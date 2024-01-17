---
title: การสนับสนุนลายเซ็น Xades
linktitle: การสนับสนุนลายเซ็น Xades
second_title: Aspose.Cells สำหรับการอ้างอิง .NET API
description: เรียนรู้วิธีเพิ่มลายเซ็น Xades ลงในไฟล์ Excel โดยใช้ Aspose.Cells สำหรับ .NET
type: docs
weight: 190
url: /th/net/excel-workbook/xades-signature-support/
---
ในบทความนี้ เราจะอธิบายทีละขั้นตอนเพื่ออธิบายซอร์สโค้ด C# ด้านล่าง ซึ่งเกี่ยวกับการสนับสนุนลายเซ็น Xades โดยใช้ไลบรารี Aspose.Cells สำหรับ .NET คุณจะพบวิธีใช้ไลบรารีนี้เพื่อเพิ่มลายเซ็นดิจิทัล Xades ลงในไฟล์ Excel นอกจากนี้เรายังจะให้ภาพรวมของกระบวนการลงนามและการดำเนินการแก่คุณอีกด้วย ทำตามขั้นตอนด้านล่างเพื่อรับผลลัพธ์ที่สรุปได้

## ขั้นตอนที่ 1: กำหนดไดเร็กทอรีต้นทางและเอาต์พุต
ในการเริ่มต้น เราต้องกำหนดไดเร็กทอรีต้นทางและเอาต์พุตในโค้ดของเรา ไดเร็กทอรีเหล่านี้ระบุตำแหน่งของไฟล์ต้นฉบับและตำแหน่งที่ไฟล์เอาต์พุตจะถูกบันทึก นี่คือรหัสที่เกี่ยวข้อง:

```csharp
// ไดเรกทอรีต้นทาง
string sourceDir = RunExamples.Get_SourceDirectory();
// ไดเร็กทอรีเอาต์พุต
string outputDir = RunExamples.Get_OutputDirectory();
```

อย่าลืมปรับเส้นทางไดเรกทอรีตามความจำเป็น

## ขั้นตอนที่ 2: กำลังโหลดสมุดงาน Excel
ขั้นตอนต่อไปคือการโหลดสมุดงาน Excel ที่เราต้องการเพิ่มลายเซ็นดิจิทัล Xades นี่คือรหัสในการโหลดสมุดงาน:

```csharp
Workbook workbook = new Workbook(sourceDir + "sourceFile.xlsx");
```

ตรวจสอบให้แน่ใจว่าได้ระบุชื่อไฟล์ต้นฉบับในโค้ดอย่างถูกต้อง

## ขั้นตอนที่ 3: การกำหนดค่าลายเซ็นดิจิทัล
ตอนนี้เราจะกำหนดค่าลายเซ็นดิจิทัล Xades โดยให้ข้อมูลที่จำเป็น เราต้องระบุไฟล์ PFX ที่มีใบรับรองดิจิทัลและรหัสผ่านที่เกี่ยวข้อง นี่คือรหัสที่เกี่ยวข้อง:

```csharp
string password = "pfxPassword";
string pfx = "pfxFile";
DigitalSignature signature = new DigitalSignature(File.ReadAllBytes(pfx), password, "testXAdES", DateTime.Now);
signature.XAdESType = XAdESType.XAdES;
```

อย่าลืมแทนที่ "pfxPassword" ด้วยรหัสผ่านจริงของคุณ และ "pfxFile" ด้วยเส้นทางไปยังไฟล์ PFX

## ขั้นตอนที่ 4: การเพิ่มลายเซ็นดิจิทัล
หลังจากที่เราได้กำหนดค่าลายเซ็นดิจิทัลแล้ว เราก็สามารถเพิ่มลงในสมุดงาน Excel ได้ นี่คือรหัสที่เกี่ยวข้อง:

```csharp
DigitalSignatureCollection dsCollection = new DigitalSignatureCollection();
dsCollection.Add(signature);
workbook.SetDigitalSignature(dsCollection);
```

ขั้นตอนนี้จะเพิ่มลายเซ็นดิจิทัล Xades ลงในสมุดงาน Excel

## ขั้นตอนที่ 5: บันทึกสมุดงานพร้อมลายเซ็น
สุดท้าย เราจะบันทึกเวิร์กบุ๊ก Excel ด้วยการเพิ่มลายเซ็นดิจิทัล นี่คือรหัสที่เกี่ยวข้อง:

```csharp
workbook.Save(outputDir + "XAdESSignatureSupport_out.xlsx");
```

ตรวจสอบให้แน่ใจว่าได้ปรับชื่อของไฟล์เอาต์พุตตามความต้องการของคุณ

### ตัวอย่างซอร์สโค้ดสำหรับ Xades Signature Support โดยใช้ Aspose.Cells สำหรับ .NET 
```csharp
//ไดเรกทอรีต้นทาง
string sourceDir = RunExamples.Get_SourceDirectory();
//ไดเร็กทอรีเอาต์พุต
string outputDir = RunExamples.Get_OutputDirectory();
Workbook workbook = new Workbook(sourceDir + "sourceFile.xlsx");
string password = "pfxPassword";
string pfx = "pfxFile";
DigitalSignature signature = new DigitalSignature(File.ReadAllBytes(pfx), password, "testXAdES", DateTime.Now);
signature.XAdESType = XAdESType.XAdES;
DigitalSignatureCollection dsCollection = new DigitalSignatureCollection();
dsCollection.Add(signature);
workbook.SetDigitalSignature(dsCollection);
workbook.Save(outputDir + "XAdESSignatureSupport_out.xlsx");
Console.WriteLine("XAdESSignatureSupport executed successfully.");
```

## บทสรุป
ขอแสดงความยินดี! คุณได้เรียนรู้วิธีใช้ไลบรารี Aspose.Cells สำหรับ .NET เพื่อเพิ่มลายเซ็นดิจิทัล Xades ลงในไฟล์ Excel โดยทำตามขั้นตอนที่ให้ไว้ในบทความนี้ คุณจะสามารถใช้ฟังก์ชันนี้ในโครงการของคุณเองได้ รู้สึกอิสระที่จะทดลองเพิ่มเติมกับห้องสมุดและค้นพบคุณสมบัติอันทรงพลังอื่น ๆ ที่มีให้

### คำถามที่พบบ่อย

#### ถาม: Xades คืออะไร

ตอบ: Xades เป็นมาตรฐานลายเซ็นอิเล็กทรอนิกส์ขั้นสูงที่ใช้เพื่อรับรองความสมบูรณ์และความถูกต้องของเอกสารดิจิทัล

#### ถาม: ฉันสามารถใช้ลายเซ็นดิจิทัลประเภทอื่นกับ Aspose.Cells ได้หรือไม่

ตอบ: ใช่ Aspose.Cells ยังรองรับลายเซ็นดิจิทัลประเภทอื่นๆ ด้วย เช่น ลายเซ็น XMLDSig และลายเซ็น PKCS#7

#### ถาม: ฉันสามารถใช้ลายเซ็นกับไฟล์ประเภทอื่นนอกเหนือจากไฟล์ Excel ได้หรือไม่
 
ตอบ: ได้ Aspose.Cells ยังอนุญาตให้ใช้ลายเซ็นดิจิทัลกับไฟล์ประเภทอื่นที่รองรับ เช่น ไฟล์ Word, PDF และ PowerPoint