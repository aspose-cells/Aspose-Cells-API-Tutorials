---
title: ควบคุมปัจจัยการซูมของแผ่นงาน
linktitle: ควบคุมปัจจัยการซูมของแผ่นงาน
second_title: Aspose.Cells สำหรับการอ้างอิง .NET API
description: ควบคุมปัจจัยการซูมของแผ่นงาน Excel ด้วย Aspose.Cells สำหรับ .NET
type: docs
weight: 20
url: /th/net/excel-display-settings-csharp-tutorials/controll-zoom-factor-of-worksheet/
---
การควบคุมปัจจัยการซูมของเวิร์กชีทเป็นคุณสมบัติที่สำคัญเมื่อทำงานกับไฟล์ Excel โดยใช้ไลบรารี Aspose.Cells สำหรับ .NET ในคู่มือนี้ เราจะแสดงวิธีใช้ Aspose.Cells เพื่อควบคุมปัจจัยการซูมของเวิร์กชีตโดยใช้ซอร์สโค้ด C# ทีละขั้นตอน

## ขั้นตอนที่ 1: นำเข้าไลบรารีที่จำเป็น

ก่อนที่คุณจะเริ่มต้น ตรวจสอบให้แน่ใจว่าคุณได้ติดตั้งไลบรารี Aspose.Cells สำหรับ .NET และนำเข้าไลบรารีที่จำเป็นลงในโปรเจ็กต์ C# ของคุณ

```csharp
using System;
using System.IO;
using Aspose.Cells;
```

## ขั้นตอนที่ 2: ตั้งค่าเส้นทางไดเรกทอรีและเปิดไฟล์ Excel

 ในการเริ่มต้น ให้กำหนดเส้นทางไปยังไดเร็กทอรีที่มีไฟล์ Excel ของคุณ จากนั้นเปิดโดยใช้ไฟล์`FileStream` วัตถุและยกตัวอย่าง`Workbook` วัตถุเพื่อแสดงสมุดงาน Excel

```csharp
string dataDir = "YOUR DOCUMENTS DIRECTORY";
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
Workbook workbook = new Workbook(fstream);
```

## ขั้นตอนที่ 3: เข้าถึงสเปรดชีตและเปลี่ยนปัจจัยการซูม

ในขั้นตอนนี้ เราเข้าถึงแผ่นงานแรกของสมุดงาน Excel โดยใช้ดัชนี`0` และตั้งค่าปัจจัยการซูมเวิร์กชีทเป็น`75`.

```csharp
Worksheet worksheet = workbook.Worksheets[0];
worksheet. Zoom = 75;
```

## ขั้นตอนที่ 4: บันทึกการเปลี่ยนแปลงและปิดไฟล์

 เมื่อเราเปลี่ยนปัจจัยการซูมของเวิร์กชีต เราจะบันทึกการเปลี่ยนแปลงในไฟล์ Excel โดยใช้`Save` วิธีการของ`Workbook` วัตถุ. จากนั้นเราจะปิดสตรีมไฟล์เพื่อปล่อยทรัพยากรที่ใช้ทั้งหมด

```csharp
workbook.Save(dataDir + "output.xls");
fstream.Close();
```

### ซอร์สโค้ดตัวอย่างสำหรับการควบคุมปัจจัยการซูมของแผ่นงานโดยใช้ Aspose.Cells สำหรับ .NET 

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
// การตั้งค่าปัจจัยการซูมของแผ่นงานเป็น 75
worksheet.Zoom = 75;
// บันทึกไฟล์ Excel ที่แก้ไข
workbook.Save(dataDir + "output.xls");
// การปิดสตรีมไฟล์เพื่อเพิ่มทรัพยากรทั้งหมด
fstream.Close();
```

## บทสรุป

คำแนะนำทีละขั้นตอนนี้จะแสดงวิธีควบคุมปัจจัยการซูมของเวิร์กชีตโดยใช้ Aspose.Cells สำหรับ .NET ด้วยการใช้ซอร์สโค้ด C# ที่ให้มา คุณสามารถปรับปัจจัยการซูมของเวิร์กชีตในแอปพลิเคชัน .NET ของคุณได้อย่างง่ายดาย

### คำถามที่พบบ่อย (FAQ)

#### Aspose.Cells สำหรับ .NET คืออะไร

Aspose.Cells for .NET เป็นไลบรารีการจัดเก็บไฟล์ที่มีคุณสมบัติหลากหลายสำหรับการจัดการไฟล์ Excel ในแอปพลิเคชัน .NET

#### ฉันจะติดตั้ง Aspose.Cells สำหรับ .NET ได้อย่างไร

 หากต้องการติดตั้ง Aspose.Cells สำหรับ .NET คุณต้องดาวน์โหลดแพ็คเกจ NuGet ที่เกี่ยวข้องจาก[กำหนดเผยแพร่](https://releases/aspose.com/cells/net/) และเพิ่มลงในโครงการ .NET ของคุณ

#### Aspose.Cells สำหรับ .NET นำเสนอฟีเจอร์อะไรบ้าง

Aspose.Cells for .NET นำเสนอฟีเจอร์ต่างๆ เช่น การสร้าง การแก้ไข การแปลง และการจัดการไฟล์ Excel ขั้นสูง

#### Aspose.Cells สำหรับ .NET รองรับไฟล์รูปแบบใดบ้าง

Aspose.Cells สำหรับ .NET รองรับไฟล์ได้หลายรูปแบบ รวมถึง XLSX, XLSM, CSV, HTML, PDF และอื่นๆ อีกมากมาย
