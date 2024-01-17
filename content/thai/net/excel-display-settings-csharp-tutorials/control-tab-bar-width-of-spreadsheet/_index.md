---
title: ควบคุมความกว้างของแถบแท็บของสเปรดชีต
linktitle: ควบคุมความกว้างของแถบแท็บของสเปรดชีต
second_title: Aspose.Cells สำหรับการอ้างอิง .NET API
description: ควบคุมความกว้างของแถบแท็บของสเปรดชีต Excel ด้วย Aspose.Cells สำหรับ .NET
type: docs
weight: 10
url: /th/net/excel-display-settings-csharp-tutorials/control-tab-bar-width-of-spreadsheet/
---
ในบทช่วยสอนนี้ เราจะแสดงวิธีควบคุมความกว้างของแถบแท็บของแผ่นงาน Excel โดยใช้ซอร์สโค้ด C# ด้วย Aspose.Cells สำหรับ .NET ทำตามขั้นตอนด้านล่างเพื่อให้ได้ผลลัพธ์ที่ต้องการ

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

## ขั้นตอนที่ 3: ซ่อนแท็บแผ่นงาน

 หากต้องการซ่อนแท็บแผ่นงาน คุณสามารถใช้ไฟล์`ShowTabs` ทรัพย์สินของ`Settings` วัตถุของ`Workbook` ระดับ. ตั้งเป็น`false` เพื่อซ่อนแท็บ

```csharp
workbook.Settings.ShowTabs = false;
```

## ขั้นตอนที่ 4: ปรับความกว้างของแถบแท็บ

 หากต้องการปรับความกว้างของแถบแท็บแผ่นงาน คุณสามารถใช้`SheetTabBarWidth` ทรัพย์สินของ`Settings` วัตถุของ`Workbook` ระดับ. ตั้งค่าเป็นค่าที่ต้องการ (เป็นพอยต์) เพื่อกำหนดความกว้าง

```csharp
workbook.Settings.SheetTabBarWidth = 800;
```

## ขั้นตอนที่ 5: บันทึกการเปลี่ยนแปลง

 เมื่อคุณได้ทำการเปลี่ยนแปลงที่จำเป็นแล้ว ให้บันทึกไฟล์ Excel ที่แก้ไขโดยใช้นามสกุล`Save` วิธีการของ`Workbook` วัตถุ.

```csharp
workbook.Save(dataDir + "output.xls");
```

### ตัวอย่างซอร์สโค้ดสำหรับความกว้างของแถบแท็บควบคุมของสเปรดชีตโดยใช้ Aspose.Cells สำหรับ .NET 
```csharp
//เส้นทางไปยังไดเร็กทอรีเอกสาร
string dataDir = "YOUR DOCUMENT DIRECTORY";
// การสร้างอินสแตนซ์วัตถุสมุดงาน
// กำลังเปิดไฟล์ Excel
Workbook workbook = new Workbook(dataDir + "book1.xls");
// การซ่อนแท็บของไฟล์ Excel
workbook.Settings.ShowTabs = true;
// การปรับความกว้างของแถบแท็บแผ่นงาน
workbook.Settings.SheetTabBarWidth = 800;
// บันทึกไฟล์ Excel ที่แก้ไข
workbook.Save(dataDir + "output.xls");
```

## บทสรุป

คำแนะนำทีละขั้นตอนนี้จะแสดงวิธีควบคุมความกว้างของแถบแท็บของเวิร์กชีต Excel โดยใช้ Aspose.Cells สำหรับ .NET เมื่อใช้ซอร์สโค้ด C# ที่ให้มา คุณสามารถปรับแต่งความกว้างของแถบแท็บในไฟล์ Excel ของคุณได้อย่างง่ายดาย

## คำถามที่พบบ่อย (FAQ)

#### Aspose.Cells สำหรับ .NET คืออะไร

Aspose.Cells for .NET เป็นไลบรารีที่มีประสิทธิภาพสำหรับจัดการไฟล์ Excel ในแอปพลิเคชัน .NET

#### ฉันจะติดตั้ง Aspose.Cells สำหรับ .NET ได้อย่างไร

 หากต้องการติดตั้ง Aspose.Cells สำหรับ .NET คุณต้องดาวน์โหลดแพ็คเกจที่เกี่ยวข้องจาก[กำหนดเผยแพร่](https://releases/aspose.com/cells/net/) และเพิ่มลงในโครงการ .NET ของคุณ

#### Aspose.Cells สำหรับ .NET นำเสนอฟีเจอร์อะไรบ้าง

Aspose.Cells for .NET นำเสนอคุณสมบัติมากมาย เช่น การสร้าง การแก้ไข การแปลง และการจัดการไฟล์ Excel

#### จะซ่อนแท็บในสเปรดชีต Excel ด้วย Aspose.Cells สำหรับ .NET ได้อย่างไร

 คุณสามารถซ่อนแท็บของแผ่นงานได้โดยใช้`ShowTabs` ทรัพย์สินของ`Settings` วัตถุของ`Workbook` คลาสและตั้งค่าเป็น`false`.

#### จะปรับความกว้างของแถบแท็บด้วย Aspose.Cells สำหรับ .NET ได้อย่างไร

คุณสามารถปรับความกว้างของแถบแท็บได้โดยใช้`SheetTabBarWidth` ทรัพย์สินของ`Settings` วัตถุของ`Workbook` คลาสและกำหนดค่าตัวเลขเป็นคะแนน