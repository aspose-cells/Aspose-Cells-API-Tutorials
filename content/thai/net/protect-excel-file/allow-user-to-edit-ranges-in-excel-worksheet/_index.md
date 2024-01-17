---
title: อนุญาตให้ผู้ใช้แก้ไขช่วงในแผ่นงาน Excel
linktitle: อนุญาตให้ผู้ใช้แก้ไขช่วงในแผ่นงาน Excel
second_title: Aspose.Cells สำหรับการอ้างอิง .NET API
description: อนุญาตให้ผู้ใช้แก้ไขช่วงเฉพาะในสเปรดชีต Excel โดยใช้ Aspose.Cells สำหรับ .NET คำแนะนำทีละขั้นตอนพร้อมซอร์สโค้ดใน C#
type: docs
weight: 10
url: /th/net/protect-excel-file/allow-user-to-edit-ranges-in-excel-worksheet/
---
ในคู่มือนี้ เราจะอธิบายวิธีใช้ Aspose.Cells สำหรับ .NET เพื่อให้ผู้ใช้สามารถแก้ไขช่วงที่ต้องการในสเปรดชีต Excel ทำตามขั้นตอนด้านล่างเพื่อทำภารกิจนี้ให้สำเร็จ

## ขั้นตอนที่ 1: การตั้งค่าสภาพแวดล้อม

ตรวจสอบให้แน่ใจว่าคุณได้ตั้งค่าสภาพแวดล้อมการพัฒนาและติดตั้ง Aspose.Cells สำหรับ .NET แล้ว คุณสามารถดาวน์โหลดไลบรารีเวอร์ชันล่าสุดได้จากเว็บไซต์อย่างเป็นทางการของ Aspose

## ขั้นตอนที่ 2: นำเข้าเนมสเปซที่จำเป็น

ในโปรเจ็กต์ C# ของคุณ ให้นำเข้าเนมสเปซที่จำเป็นเพื่อทำงานกับ Aspose.Cells:

```csharp
using Aspose.Cells;
```

## ขั้นตอนที่ 3: การตั้งค่าเส้นทางไปยังไดเร็กทอรีเอกสาร

 ประกาศ ก`dataDir` ตัวแปรเพื่อระบุเส้นทางไปยังไดเร็กทอรีที่คุณต้องการบันทึกไฟล์ Excel ที่สร้างขึ้น:

```csharp
string dataDir = "YOUR_DIRECTORY_OF_DOCUMENTS";
```

 อย่าลืมเปลี่ยน`"YOUR_DOCUMENT_DIRECTORY"` ด้วยเส้นทางที่ถูกต้องในระบบของคุณ

## ขั้นตอนที่ 4: การสร้างวัตถุสมุดงาน

สร้างอินสแตนซ์ของวัตถุสมุดงานใหม่ที่แสดงถึงสมุดงาน Excel ที่คุณต้องการสร้าง:

```csharp
Workbook book = new Workbook();
```

## ขั้นตอนที่ 5: เข้าถึงแผ่นงานแรก

นำทางไปยังแผ่นงานแรกในสมุดงาน Excel โดยใช้รหัสต่อไปนี้:

```csharp
Worksheet sheet = book.Worksheets[0];
```

## ขั้นตอนที่ 6: การดึงช่วงการแก้ไขที่ได้รับอนุญาต

 รับคอลเลกชันของช่วงการแก้ไขที่อนุญาตโดยใช้`AllowEditRanges` คุณสมบัติ:

```csharp
ProtectedRangeCollection allowRanges = sheet.AllowEditRanges;
```

## ขั้นตอนที่ 7: กำหนดช่วงที่ได้รับการป้องกัน

 กำหนดช่วงที่มีการป้องกันโดยใช้`Add` วิธีการของ`AllowEditRanges` ของสะสม:

```csharp
int idx = allowRanges.Add("r2", 1, 1, 3, 3);
protectedRange protectedRange = allowRanges[idx];
```

ที่นี่เราได้สร้างช่วงที่มีการป้องกัน "r2" ซึ่งครอบคลุมตั้งแต่เซลล์ A1 ถึงเซลล์ C3

## ขั้นตอนที่ 8: การระบุรหัสผ่าน

 ระบุรหัสผ่านสำหรับช่วงที่ได้รับการป้องกันโดยใช้`Password` คุณสมบัติ:

```csharp
protectedRange.Password = "YOUR_PASSWORD";
```

 อย่าลืมเปลี่ยน`"YOUR_PASSWORD"` ด้วยรหัสผ่านที่ต้องการ

## ขั้นตอนที่ 9: การปกป้องแผ่นงาน

 ป้องกันแผ่นงานโดยใช้`Protect` วิธีการของ`Worksheet` วัตถุ:

```csharp
sheet.Protect(ProtectionType.All);
```

วิธีนี้จะปกป้องสเปรดชีตโดยป้องกันการแก้ไขใดๆ ที่อยู่นอกช่วงที่อนุญาต

## ขั้นตอนที่ 10: การลงทะเบียน

  ไฟล์เอ็กเซล

 บันทึกไฟล์ Excel ที่สร้างขึ้นโดยใช้นามสกุล`Save` วิธีการของ`Workbook` วัตถุ:

```csharp
book.Save(dataDir + "protectedrange.out.xls");
```

อย่าลืมระบุชื่อไฟล์ที่ต้องการและเส้นทางที่ถูกต้อง

### ตัวอย่างซอร์สโค้ดสำหรับการอนุญาตให้ผู้ใช้แก้ไขช่วงในแผ่นงาน Excel โดยใช้ Aspose.Cells สำหรับ .NET 
```csharp
//เส้นทางไปยังไดเร็กทอรีเอกสาร
string dataDir = "YOUR DOCUMENT DIRECTORY";
// สร้างไดเร็กทอรีหากไม่มีอยู่
bool IsExists = System.IO.Directory.Exists(dataDir);
if (!IsExists)
    System.IO.Directory.CreateDirectory(dataDir);
// สร้างอินสแตนซ์ของสมุดงานใหม่
Workbook book = new Workbook();
// รับแผ่นงานแรก (ค่าเริ่มต้น)
Worksheet sheet = book.Worksheets[0];
// รับช่วงที่อนุญาตการแก้ไข
ProtectedRangeCollection allowRanges = sheet.AllowEditRanges;
// กำหนด ProtectedRange
ProtectedRange proteced_range;
// สร้างช่วง
int idx = allowRanges.Add("r2", 1, 1, 3, 3);
proteced_range = allowRanges[idx];
// ระบุรหัสผ่าน
proteced_range.Password = "123";
// ป้องกันแผ่น
sheet.Protect(ProtectionType.All);
// บันทึกไฟล์ Excel
book.Save(dataDir + "protectedrange.out.xls");
```

## บทสรุป

ตอนนี้คุณได้เรียนรู้วิธีใช้ Aspose.Cells สำหรับ .NET เพื่อให้ผู้ใช้สามารถแก้ไขช่วงเฉพาะในสเปรดชีต Excel ได้ สำรวจคุณสมบัติเพิ่มเติมที่ Aspose.Cells นำเสนอเพิ่มเติมได้ตามต้องการ เพื่อตอบสนองความต้องการเฉพาะของคุณ


### คำถามที่พบบ่อย

#### 1. จะอนุญาตให้ผู้ใช้แก้ไขช่วงเฉพาะในสเปรดชีต Excel ได้อย่างไร

 คุณสามารถใช้`ProtectedRangeCollection` คลาสเพื่อกำหนดช่วงการแก้ไขที่อนุญาต ใช้`Add` วิธีการสร้างช่วงการป้องกันใหม่ด้วยเซลล์ที่ต้องการ

#### 2. ฉันสามารถตั้งรหัสผ่านสำหรับช่วงการแก้ไขที่ได้รับอนุญาตได้หรือไม่?

 ใช่ คุณสามารถระบุรหัสผ่านโดยใช้`Password` ทรัพย์สินของ`ProtectedRange` วัตถุ. วิธีนี้จะจำกัดการเข้าถึงเฉพาะผู้ใช้ที่มีรหัสผ่านเท่านั้น

#### 3. ฉันจะป้องกันสเปรดชีตได้อย่างไรเมื่อตั้งค่าช่วงที่อนุญาตแล้ว

 ใช้`Protect` วิธีการของ`Worksheet` วัตถุเพื่อปกป้องแผ่นงาน วิธีนี้จะป้องกันการเปลี่ยนแปลงใดๆ ที่อยู่นอกช่วงที่อนุญาต ซึ่งอาจจำเป็นต้องใส่รหัสผ่านหากคุณระบุไว้