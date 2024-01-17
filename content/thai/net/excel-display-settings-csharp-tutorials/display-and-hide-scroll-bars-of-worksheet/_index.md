---
title: แสดงและซ่อนแถบเลื่อนของแผ่นงาน
linktitle: แสดงและซ่อนแถบเลื่อนของแผ่นงาน
second_title: Aspose.Cells สำหรับการอ้างอิง .NET API
description: แสดงหรือซ่อนแถบเลื่อนในแผ่นงาน Excel โดยใช้ Aspose.Cells สำหรับ .NET
type: docs
weight: 50
url: /th/net/excel-display-settings-csharp-tutorials/display-and-hide-scroll-bars-of-worksheet/
---
ในบทช่วยสอนนี้ เราจะแสดงวิธีแสดงหรือซ่อนแถบเลื่อนแนวตั้งและแนวนอนในเวิร์กชีต Excel โดยใช้ซอร์สโค้ด C# พร้อม Aspose.Cells สำหรับ .NET ทำตามขั้นตอนด้านล่างเพื่อให้ได้ผลลัพธ์ที่ต้องการ

## ขั้นตอนที่ 1: นำเข้าไลบรารีที่จำเป็น

ตรวจสอบให้แน่ใจว่าคุณได้ติดตั้งไลบรารี Aspose.Cells สำหรับ .NET และนำเข้าไลบรารีที่จำเป็นลงในโปรเจ็กต์ C# ของคุณ

```csharp
using Aspose.Cells;
using System.IO;
```

## ขั้นตอนที่ 2: ตั้งค่าเส้นทางไดเรกทอรีและเปิดไฟล์ Excel

 กำหนดเส้นทางไปยังไดเร็กทอรีที่มีไฟล์ Excel ของคุณ จากนั้นเปิดไฟล์โดยสร้างสตรีมไฟล์และสร้างอินสแตนซ์`Workbook` วัตถุ.

```csharp
string dataDir = "YOUR DOCUMENTS DIRECTORY";
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
Workbook workbook = new Workbook(fstream);
```

## ขั้นตอนที่ 3: ซ่อนแถบเลื่อน

 ใช้`IsVScrollBarVisible` และ`IsHScrollBarVisible` คุณสมบัติของ`Workbook.Settings` วัตถุเพื่อซ่อนแถบเลื่อนแนวตั้งและแนวนอนของแผ่นงาน

```csharp
workbook.Settings.IsVScrollBarVisible = false;
workbook.Settings.IsHScrollBarVisible = false;
```

## ขั้นตอนที่ 4: บันทึกการเปลี่ยนแปลง

 เมื่อคุณได้ทำการเปลี่ยนแปลงที่จำเป็นแล้ว ให้บันทึกไฟล์ Excel ที่แก้ไขโดยใช้นามสกุล`Save` วิธีการของ`Workbook` วัตถุ.

```csharp
workbook.Save(dataDir + "output.xls");
```

### ตัวอย่างซอร์สโค้ดสำหรับการแสดงและซ่อนแถบเลื่อนของแผ่นงานโดยใช้ Aspose.Cells สำหรับ .NET 

```csharp
//เส้นทางไปยังไดเร็กทอรีเอกสาร
string dataDir = "YOUR DOCUMENT DIRECTORY";
// การสร้างสตรีมไฟล์ที่มีไฟล์ Excel ที่จะเปิด
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
// การสร้างอินสแตนซ์วัตถุสมุดงาน
// การเปิดไฟล์ Excel ผ่านการสตรีมไฟล์
Workbook workbook = new Workbook(fstream);
// การซ่อนแถบเลื่อนแนวตั้งของไฟล์ Excel
workbook.Settings.IsVScrollBarVisible = false;
// การซ่อนแถบเลื่อนแนวนอนของไฟล์ Excel
workbook.Settings.IsHScrollBarVisible = false;
// บันทึกไฟล์ Excel ที่แก้ไข
workbook.Save(dataDir + "output.xls");
// การปิดสตรีมไฟล์เพื่อเพิ่มทรัพยากรทั้งหมด
fstream.Close();
```

### บทสรุป

คำแนะนำทีละขั้นตอนนี้แสดงวิธีการแสดงหรือซ่อนแถบเลื่อนแนวตั้งและแนวนอนในสเปรดชีต Excel โดยใช้ Aspose.Cells สำหรับ .NET การใช้ซอร์สโค้ด C# ที่ให้มา คุณสามารถปรับแต่งการแสดงแถบเลื่อนในไฟล์ Excel ของคุณได้อย่างง่ายดาย

### คำถามที่พบบ่อย (FAQ)

#### Aspose.Cells สำหรับ .NET คืออะไร

Aspose.Cells for .NET เป็นไลบรารีที่มีประสิทธิภาพสำหรับจัดการไฟล์ Excel ในแอปพลิเคชัน .NET

#### ฉันจะติดตั้ง Aspose.Cells สำหรับ .NET ได้อย่างไร

 หากต้องการติดตั้ง Aspose.Cells สำหรับ .NET คุณต้องดาวน์โหลดแพ็คเกจที่เกี่ยวข้องจาก[กำหนดเผยแพร่](https://releases/aspose.com/cells/net/) และเพิ่มลงในโครงการ .NET ของคุณ

#### ฉันจะแสดงหรือซ่อนแถบเลื่อนในสเปรดชีต Excel ด้วย Aspose.Cells สำหรับ .NET ได้อย่างไร

 คุณสามารถใช้`IsVScrollBarVisible` และ`IsHScrollBarVisible` คุณสมบัติของ`Workbook.Settings` วัตถุเพื่อแสดงหรือซ่อนแถบเลื่อนแนวตั้งและแนวนอนตามลำดับในแผ่นงาน Excel

#### Aspose.Cells สำหรับ .NET รองรับไฟล์ Excel รูปแบบใดบ้าง

Aspose.Cells สำหรับ .NET รองรับไฟล์ Excel หลากหลายรูปแบบ เช่น XLS, XLSX, CSV, HTML, PDF เป็นต้น