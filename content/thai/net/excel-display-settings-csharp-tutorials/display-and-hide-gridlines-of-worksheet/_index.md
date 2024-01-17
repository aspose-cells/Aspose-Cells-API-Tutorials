---
title: แสดงและซ่อนเส้นตารางของแผ่นงาน
linktitle: แสดงและซ่อนเส้นตารางของแผ่นงาน
second_title: Aspose.Cells สำหรับการอ้างอิง .NET API
description: ควบคุมการแสดงเส้นตารางในแผ่นงาน Excel ด้วย Aspose.Cells for .NET
type: docs
weight: 30
url: /th/net/excel-display-settings-csharp-tutorials/display-and-hide-gridlines-of-worksheet/
---
ในบทช่วยสอนนี้ เราจะแสดงวิธีแสดงและซ่อนเส้นตารางในเวิร์กชีต Excel โดยใช้ซอร์สโค้ด C# กับ Aspose.Cells สำหรับ .NET ทำตามขั้นตอนด้านล่างเพื่อให้ได้ผลลัพธ์ที่ต้องการ

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

## ขั้นตอนที่ 3: ไปที่แผ่นงานแรกและซ่อนเส้นตาราง

 เข้าถึงแผ่นงานแรกในไฟล์ Excel โดยใช้นามสกุลไฟล์`Worksheets` ทรัพย์สินของ`Workbook` วัตถุ. จากนั้นใช้`IsGridlinesVisible` ทรัพย์สินของ`Worksheet` วัตถุเพื่อซ่อนเส้นตาราง

```csharp
Worksheet worksheet = workbook.Worksheets[0];
worksheet.IsGridlinesVisible = false;
```

## ขั้นตอนที่ 4: บันทึกการเปลี่ยนแปลง

 เมื่อคุณได้ทำการเปลี่ยนแปลงที่จำเป็นแล้ว ให้บันทึกไฟล์ Excel ที่แก้ไขโดยใช้นามสกุล`Save` วิธีการของ`Workbook` วัตถุ.

```csharp
workbook.Save(dataDir + "output.xls");
```

### ซอร์สโค้ดตัวอย่างสำหรับการแสดงและซ่อนเส้นตารางของแผ่นงานโดยใช้ Aspose.Cells สำหรับ .NET 

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
// การซ่อนเส้นตารางของแผ่นงานแรกของไฟล์ Excel
worksheet.IsGridlinesVisible = false;
// บันทึกไฟล์ Excel ที่แก้ไข
workbook.Save(dataDir + "output.xls");
// การปิดสตรีมไฟล์เพื่อเพิ่มทรัพยากรทั้งหมด
fstream.Close();
```

## บทสรุป

คำแนะนำทีละขั้นตอนนี้จะแสดงวิธีแสดงและซ่อนเส้นตารางในสเปรดชีต Excel โดยใช้ Aspose.Cells สำหรับ .NET ด้วยการใช้ซอร์สโค้ด C# ที่ให้มา คุณสามารถปรับแต่งการแสดงเส้นตารางในไฟล์ Excel ของคุณได้อย่างง่ายดาย

### คำถามที่พบบ่อย (FAQ)

#### Aspose.Cells สำหรับ .NET คืออะไร

Aspose.Cells for .NET เป็นไลบรารีที่มีประสิทธิภาพสำหรับจัดการไฟล์ Excel ในแอปพลิเคชัน .NET

#### ฉันจะติดตั้ง Aspose.Cells สำหรับ .NET ได้อย่างไร

 หากต้องการติดตั้ง Aspose.Cells สำหรับ .NET คุณต้องดาวน์โหลดแพ็คเกจที่เกี่ยวข้องจาก[กำหนดเผยแพร่](https://releases/aspose.com/cells/net/) และเพิ่มลงในโครงการ .NET ของคุณ

#### ฉันจะแสดงหรือซ่อนเส้นตารางในสเปรดชีต Excel ด้วย Aspose.Cells สำหรับ .NET ได้อย่างไร

 คุณสามารถใช้`IsGridlinesVisible` ทรัพย์สินของ`Worksheet` วัตถุเพื่อแสดงหรือซ่อนเส้นตาราง ตั้งเป็น`true` เพื่อแสดงให้พวกเขาเห็นและเพื่อ`false` เพื่อซ่อนพวกเขา

#### Aspose.Cells สำหรับ .NET รองรับไฟล์ Excel รูปแบบใดบ้าง

Aspose.Cells สำหรับ .NET รองรับไฟล์ Excel หลากหลายรูปแบบ เช่น XLS, XLSX, CSV, HTML, PDF และอื่นๆ อีกมากมาย

