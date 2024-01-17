---
title: แสดงแท็บสเปรดชีต
linktitle: แสดงแท็บสเปรดชีต
second_title: Aspose.Cells สำหรับการอ้างอิง .NET API
description: แสดงแท็บสเปรดชีต Excel โดยใช้ Aspose.Cells สำหรับ .NET
type: docs
weight: 60
url: /th/net/excel-display-settings-csharp-tutorials/display-tab-of-spreadsheet/
---
ในบทช่วยสอนนี้ เราจะแสดงวิธีแสดงแท็บของแผ่นงาน Excel โดยใช้ซอร์สโค้ด C# กับ Aspose.Cells สำหรับ .NET ทำตามขั้นตอนด้านล่างเพื่อให้ได้ผลลัพธ์ที่ต้องการ

## ขั้นตอนที่ 1: นำเข้าไลบรารีที่จำเป็น

ตรวจสอบให้แน่ใจว่าคุณได้ติดตั้งไลบรารี Aspose.Cells สำหรับ .NET และนำเข้าไลบรารีที่จำเป็นลงในโปรเจ็กต์ C# ของคุณ

```csharp
using Aspose.Cells;
```

## ขั้นตอนที่ 2: ตั้งค่าเส้นทางไดเรกทอรีและเปิดไฟล์ Excel

 กำหนดเส้นทางไปยังไดเร็กทอรีที่มีไฟล์ Excel ของคุณ จากนั้นเปิดไฟล์โดยสร้างอินสแตนซ์ a`Workbook` วัตถุ.

```csharp
string dataDir = "YOUR DOCUMENTS DIRECTORY";
Workbook workbook = new Workbook(dataDir + "book1.xls");
```

## ขั้นตอนที่ 3: แสดงแท็บแผ่นงาน

 ใช้`ShowTabs` ทรัพย์สินของ`Workbook.Settings` วัตถุเพื่อแสดงแท็บแผ่นงาน Excel

```csharp
workbook.Settings.ShowTabs = true;
```

## ขั้นตอนที่ 4: บันทึกการเปลี่ยนแปลง

 เมื่อคุณได้ทำการเปลี่ยนแปลงที่จำเป็นแล้ว ให้บันทึกไฟล์ Excel ที่แก้ไขโดยใช้นามสกุล`Save` วิธีการของ`Workbook` วัตถุ.

```csharp
workbook.Save(dataDir + "output.xls");
```

### ตัวอย่างซอร์สโค้ดสำหรับแท็บแสดงสเปรดชีตโดยใช้ Aspose.Cells สำหรับ .NET 

```csharp
//เส้นทางไปยังไดเร็กทอรีเอกสาร
string dataDir = "YOUR DOCUMENT DIRECTORY";
// การสร้างอินสแตนซ์วัตถุสมุดงาน
// กำลังเปิดไฟล์ Excel
Workbook workbook = new Workbook(dataDir + "book1.xls");
// การซ่อนแท็บของไฟล์ Excel
workbook.Settings.ShowTabs = true;
// บันทึกไฟล์ Excel ที่แก้ไข
workbook.Save(dataDir + "output.xls");
```

### บทสรุป

คำแนะนำทีละขั้นตอนนี้จะแสดงวิธีแสดงแท็บของสเปรดชีต Excel โดยใช้ Aspose.Cells สำหรับ .NET ด้วยการใช้ซอร์สโค้ด C# ที่ให้มา คุณสามารถปรับแต่งการแสดงแท็บในไฟล์ Excel ของคุณได้อย่างง่ายดาย

### คำถามที่พบบ่อย (FAQ)

#### Aspose.Cells สำหรับ .NET คืออะไร

Aspose.Cells for .NET เป็นไลบรารีที่มีประสิทธิภาพสำหรับจัดการไฟล์ Excel ในแอปพลิเคชัน .NET

#### ฉันจะติดตั้ง Aspose.Cells สำหรับ .NET ได้อย่างไร

 หากต้องการติดตั้ง Aspose.Cells สำหรับ .NET คุณต้องดาวน์โหลดแพ็คเกจที่เกี่ยวข้องจาก[กำหนดเผยแพร่](https://releases/aspose.com/cells/net/) และเพิ่มลงในโครงการ .NET ของคุณ

#### จะแสดงแท็บของสเปรดชีต Excel โดยใช้ Aspose.Cells สำหรับ .NET ได้อย่างไร

 คุณสามารถใช้`ShowTabs` ทรัพย์สินของ`Workbook.Settings` วัตถุและตั้งค่าเป็น`true` เพื่อแสดงแท็บแผ่นงาน

#### Aspose.Cells สำหรับ .NET รองรับไฟล์ Excel รูปแบบใดบ้าง

Aspose.Cells สำหรับ .NET รองรับไฟล์ Excel หลากหลายรูปแบบ เช่น XLS, XLSX, CSV, HTML, PDF เป็นต้น
