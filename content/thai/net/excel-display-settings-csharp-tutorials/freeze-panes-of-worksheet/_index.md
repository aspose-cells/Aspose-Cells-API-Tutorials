---
title: ตรึงบานหน้าต่างของแผ่นงาน
linktitle: ตรึงบานหน้าต่างของแผ่นงาน
second_title: Aspose.Cells สำหรับการอ้างอิง .NET API
description: จัดการบานหน้าต่างตรึงของแผ่นงาน Excel ได้อย่างง่ายดายด้วย Aspose.Cells สำหรับ .NET
type: docs
weight: 70
url: /th/net/excel-display-settings-csharp-tutorials/freeze-panes-of-worksheet/
---
ในบทช่วยสอนนี้ เราจะแสดงวิธีล็อกบานหน้าต่างในเวิร์กชีต Excel โดยใช้ซอร์สโค้ด C# กับ Aspose.Cells สำหรับ .NET ทำตามขั้นตอนด้านล่างเพื่อให้ได้ผลลัพธ์ที่ต้องการ

## ขั้นตอนที่ 1: นำเข้าไลบรารีที่จำเป็น

ตรวจสอบให้แน่ใจว่าคุณได้ติดตั้งไลบรารี Aspose.Cells สำหรับ .NET และนำเข้าไลบรารีที่จำเป็นลงในโปรเจ็กต์ C# ของคุณ

```csharp
using Aspose.Cells;
```

## ขั้นตอนที่ 2: ตั้งค่าเส้นทางไดเรกทอรีและเปิดไฟล์ Excel

 กำหนดเส้นทางไปยังไดเร็กทอรีที่มีไฟล์ Excel ของคุณ จากนั้นเปิดไฟล์โดยสร้างอินสแตนซ์ a`Workbook` วัตถุ.

```csharp
string dataDir = "YOUR DOCUMENTS DIRECTORY";
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
Workbook workbook = new Workbook(fstream);
```

## ขั้นตอนที่ 3: ไปที่สเปรดชีตและใช้การตั้งค่าการล็อคบานหน้าต่าง

 นำทางไปยังแผ่นงานแรกในไฟล์ Excel โดยใช้นามสกุล`Worksheet` วัตถุ. จากนั้นใช้`FreezePanes` วิธีการใช้การตั้งค่าการล็อคบานหน้าต่าง

```csharp
Worksheet worksheet = workbook.Worksheets[0];
worksheet. FreezePanes(3, 2, 3, 2);
```

ในตัวอย่างข้างต้น บานหน้าต่างจะล็อกอยู่กับเซลล์ในแถวที่ 3 และคอลัมน์ 2

## ขั้นตอนที่ 4: บันทึกการเปลี่ยนแปลง

 เมื่อคุณได้ทำการเปลี่ยนแปลงที่จำเป็นแล้ว ให้บันทึกไฟล์ Excel ที่แก้ไขโดยใช้นามสกุล`Save` วิธีการของ`Workbook` วัตถุ.

```csharp
workbook.Save(dataDir + "output.xls");
```

### ตัวอย่างซอร์สโค้ดสำหรับการตรึง Panes Of Worksheet โดยใช้ Aspose.Cells สำหรับ .NET 

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
// การใช้การตั้งค่าบานหน้าต่างตรึง
worksheet.FreezePanes(3, 2, 3, 2);
// บันทึกไฟล์ Excel ที่แก้ไข
workbook.Save(dataDir + "output.xls");
// การปิดสตรีมไฟล์เพื่อเพิ่มทรัพยากรทั้งหมด
fstream.Close();
```

## บทสรุป

คำแนะนำทีละขั้นตอนนี้แสดงวิธีล็อคบานหน้าต่างในสเปรดชีต Excel โดยใช้ Aspose.Cells สำหรับ .NET ด้วยการใช้ซอร์สโค้ด C# ที่ให้มา คุณสามารถปรับแต่งการตั้งค่าการล็อคบานหน้าต่างได้อย่างง่ายดาย เพื่อจัดระเบียบและแสดงภาพข้อมูลของคุณในไฟล์ Excel ได้ดียิ่งขึ้น

### คำถามที่พบบ่อย (FAQ)

#### Aspose.Cells สำหรับ .NET คืออะไร

Aspose.Cells for .NET เป็นไลบรารีที่มีประสิทธิภาพสำหรับจัดการไฟล์ Excel ในแอปพลิเคชัน .NET

#### ฉันจะติดตั้ง Aspose.Cells สำหรับ .NET ได้อย่างไร

 หากต้องการติดตั้ง Aspose.Cells สำหรับ .NET คุณต้องดาวน์โหลดแพ็คเกจที่เกี่ยวข้องจาก[กำหนดเผยแพร่](https://releases/aspose.com/cells/net/) และเพิ่มลงในโครงการ .NET ของคุณ

#### วิธีล็อคบานหน้าต่างในแผ่นงาน Excel โดยใช้ Aspose.Cells สำหรับ .NET

 คุณสามารถใช้`FreezePanes` วิธีการของ`Worksheet` วัตถุเพื่อล็อคบานหน้าต่างของแผ่นงาน ระบุเซลล์ที่จะล็อคโดยระบุดัชนีแถวและคอลัมน์

#### ฉันสามารถปรับแต่งการตั้งค่าการล็อคบานหน้าต่างด้วย Aspose.Cells สำหรับ .NET ได้หรือไม่

 ใช่แล้ว โดยใช้.`FreezePanes` คุณสามารถระบุเซลล์ที่จะล็อคได้ตามต้องการ โดยระบุดัชนีแถวและคอลัมน์ที่เหมาะสม
