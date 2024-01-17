---
title: การแสดงตัวอย่างตัวแบ่งหน้าของแผ่นงาน
linktitle: การแสดงตัวอย่างตัวแบ่งหน้าของแผ่นงาน
second_title: Aspose.Cells สำหรับการอ้างอิง .NET API
description: คำแนะนำทีละขั้นตอนเพื่อแสดงตัวอย่างตัวแบ่งหน้าของแผ่นงานโดยใช้ Aspose.Cells สำหรับ .NET
type: docs
weight: 110
url: /th/net/excel-display-settings-csharp-tutorials/page-break-preview-of-worksheet/
---
ในบทช่วยสอนนี้ เราจะอธิบายวิธีการแสดงตัวอย่างตัวแบ่งหน้าของเวิร์กชีตโดยใช้ Aspose.Cells สำหรับ .NET ทำตามขั้นตอนเหล่านี้เพื่อให้ได้ผลลัพธ์ที่ต้องการ:

## ขั้นตอนที่ 1: การตั้งค่าสภาพแวดล้อม

ตรวจสอบให้แน่ใจว่าคุณได้ติดตั้ง Aspose.Cells สำหรับ .NET และตั้งค่าสภาพแวดล้อมการพัฒนาของคุณ นอกจากนี้ ตรวจสอบให้แน่ใจว่าคุณมีสำเนาของไฟล์ Excel ที่คุณต้องการแสดงตัวอย่างตัวแบ่งหน้า

## ขั้นตอนที่ 2: นำเข้าการอ้างอิงที่จำเป็น

เพิ่มคำสั่งที่จำเป็นเพื่อใช้คลาสจาก Aspose.Cells:

```csharp
using Aspose.Cells;
using System.IO;
```

## ขั้นตอนที่ 3: การเริ่มต้นรหัส

เริ่มต้นด้วยการเริ่มต้นเส้นทางไปยังไดเร็กทอรีที่มีเอกสาร Excel ของคุณ:

```csharp
string dataDir = "YOUR DOCUMENTS DIRECTORY";
```

## ขั้นตอนที่ 4: การเปิดไฟล์ Excel

 สร้างก`FileStream` วัตถุที่มีไฟล์ Excel ที่จะเปิด:

```csharp
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
```

 ยกตัวอย่าง`Workbook` วัตถุและเปิดไฟล์ Excel โดยใช้สตรีมไฟล์:

```csharp
Workbook workbook = new Workbook(fstream);
```

## ขั้นตอนที่ 5: การเข้าถึงสเปรดชีต

นำทางไปยังแผ่นงานแรกในไฟล์ Excel:

```csharp
Worksheet worksheet = workbook.Worksheets[0];
```

## ขั้นตอนที่ 6: การแสดงทีละหน้าตัวอย่าง

เปิดใช้งานการแสดงตัวอย่างทีละหน้าสำหรับสเปรดชีต:

```csharp
worksheet. IsPageBreakPreview = true;
```

## ขั้นตอนที่ 7: บันทึกการเปลี่ยนแปลง

บันทึกการเปลี่ยนแปลงที่ทำกับไฟล์ Excel:

```csharp
workbook.Save(dataDir + "output.xls");
```

## ขั้นตอนที่ 8: ปิดสตรีมไฟล์

ปิดสตรีมไฟล์เพื่อเผยแพร่ทรัพยากรทั้งหมด:

```csharp
fstream.Close();
```

### ตัวอย่างซอร์สโค้ดสำหรับการแสดงตัวอย่างตัวแบ่งหน้าของแผ่นงานโดยใช้ Aspose.Cells สำหรับ .NET 
```csharp
//เส้นทางไปยังไดเร็กทอรีเอกสาร
string dataDir = "YOUR DOCUMENT DIRECTORY";
// การสร้างสตรีมไฟล์ที่มีไฟล์ Excel ที่จะเปิด
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
// การสร้างอินสแตนซ์วัตถุสมุดงาน
// การเปิดไฟล์ Excel ผ่านการสตรีมไฟล์
Workbook workbook = new Workbook(fstream);
// การเข้าถึงแผ่นงานแรกในไฟล์ Excel
Worksheet worksheet = workbook.Worksheets[0];
// การแสดงแผ่นงานในการดูตัวอย่างตัวแบ่งหน้า
worksheet.IsPageBreakPreview = true;
// บันทึกไฟล์ Excel ที่แก้ไข
workbook.Save(dataDir + "output.xls");
// การปิดสตรีมไฟล์เพื่อเพิ่มทรัพยากรทั้งหมด
fstream.Close();
```

## บทสรุป

ในบทช่วยสอนนี้ คุณได้เรียนรู้วิธีแสดงตัวอย่างตัวแบ่งหน้าของเวิร์กชีตโดยใช้ Aspose.Cells สำหรับ .NET ด้วยการทำตามขั้นตอนที่อธิบายไว้ คุณจะสามารถควบคุมลักษณะที่ปรากฏและเค้าโครงของไฟล์ Excel ของคุณได้อย่างง่ายดาย

### คำถามที่พบบ่อย (FAQ)

#### Aspose.Cells สำหรับ .NET คืออะไร

Aspose.Cells for .NET เป็นไลบรารีซอฟต์แวร์ยอดนิยมสำหรับจัดการไฟล์ Excel ในแอปพลิเคชัน .NET

#### ฉันสามารถแสดงตัวอย่างทีละหน้าสำหรับแผ่นงานเฉพาะแทนแผ่นงานทั้งหมดได้หรือไม่

ใช่ การใช้ Aspose.Cells คุณสามารถเปิดใช้งานการแสดงตัวอย่างตัวแบ่งหน้าสำหรับเวิร์กชีทเฉพาะได้โดยการเข้าถึงออบเจ็กต์เวิร์กชีตที่เกี่ยวข้อง

#### Aspose.Cells รองรับฟีเจอร์การแก้ไขไฟล์ Excel อื่นๆ หรือไม่

ใช่ Aspose.Cells นำเสนอคุณสมบัติที่หลากหลายสำหรับการแก้ไขและจัดการไฟล์ Excel เช่น การเพิ่มข้อมูล การจัดรูปแบบ การสร้างแผนภูมิ ฯลฯ

#### Aspose.Cells ใช้งานได้กับไฟล์ Excel ในรูปแบบ .xls เท่านั้นหรือไม่

ไม่ Aspose.Cells รองรับไฟล์ Excel หลากหลายรูปแบบ รวมถึง .xls และ .xlsx
	