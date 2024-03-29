---
title: Excel ล้างตัวแบ่งหน้าทั้งหมด
linktitle: Excel ล้างตัวแบ่งหน้าทั้งหมด
second_title: Aspose.Cells สำหรับการอ้างอิง .NET API
description: เรียนรู้วิธีลบตัวแบ่งหน้าทั้งหมดใน Excel ด้วย Aspose.Cells สำหรับ .NET บทช่วยสอนทีละขั้นตอนเพื่อล้างไฟล์ Excel ของคุณ
type: docs
weight: 20
url: /th/net/excel-page-breaks/excel-clear-all-page-breaks/
---

การลบตัวแบ่งหน้าในไฟล์ Excel เป็นขั้นตอนสำคัญในการจัดการรายงานหรือสเปรดชีต ในบทช่วยสอนนี้ เราจะแนะนำคุณทีละขั้นตอนเพื่อทำความเข้าใจและใช้งานซอร์สโค้ด C# ที่ให้มาเพื่อลบตัวแบ่งหน้าทั้งหมดในไฟล์ Excel โดยใช้ไลบรารี Aspose.Cells สำหรับ .NET

## ขั้นตอนที่ 1: การเตรียมสภาพแวดล้อม

 ก่อนที่คุณจะเริ่มต้น ตรวจสอบให้แน่ใจว่าคุณได้ติดตั้ง Aspose.Cells สำหรับ .NET บนเครื่องของคุณแล้ว คุณสามารถดาวน์โหลดห้องสมุดได้จาก[กำหนดเผยแพร่](https://releases.aspose.com/cells/net)และติดตั้งโดยทำตามคำแนะนำที่ให้ไว้

เมื่อการติดตั้งเสร็จสมบูรณ์ ให้สร้างโปรเจ็กต์ C# ใหม่ในสภาพแวดล้อมการพัฒนาแบบรวม (IDE) ที่คุณต้องการ และนำเข้าไลบรารี Aspose.Cells สำหรับ .NET

## ขั้นตอนที่ 2: การกำหนดค่าเส้นทางไดเรกทอรีเอกสาร

 ในซอร์สโค้ดที่ให้มา คุณต้องระบุเส้นทางไดเร็กทอรีที่คุณต้องการบันทึกไฟล์ Excel ที่สร้างขึ้น ปรับเปลี่ยน`dataDir` ตัวแปรโดยการแทนที่ "ไดเรกทอรีเอกสารของคุณ" ด้วยเส้นทางที่แน่นอนของไดเรกทอรีบนเครื่องของคุณ

```csharp
//เส้นทางไปยังไดเร็กทอรีเอกสาร
string dataDir = "PATH TO YOUR DOCUMENTS DIRECTORY";
```

## ขั้นตอนที่ 3: การสร้างวัตถุสมุดงาน

ในการเริ่มต้น เราต้องสร้างวัตถุสมุดงานที่แสดงถึงไฟล์ Excel ของเรา ซึ่งสามารถทำได้โดยใช้คลาสสมุดงานที่ Aspose.Cells จัดเตรียมไว้

```csharp
// การสร้างอินสแตนซ์วัตถุสมุดงาน
Workbook workbook = new Workbook();
```

## ขั้นตอนที่ 4: ลบตัวแบ่งหน้า

 ตอนนี้เราจะลบตัวแบ่งหน้าทั้งหมดในแผ่นงาน Excel ของเรา ในโค้ดตัวอย่าง เราใช้`Clear()` วิธีการแบ่งหน้าแนวนอนและแนวตั้งเพื่อลบออกทั้งหมด

```csharp
workbook.Worksheets[0].HorizontalPageBreaks.Clear();
workbook.Worksheets[0].VerticalPageBreaks.Clear();
```

## ขั้นตอนที่ 5: บันทึกไฟล์ Excel

 เมื่อลบตัวแบ่งหน้าทั้งหมดแล้ว เราก็สามารถบันทึกไฟล์ Excel สุดท้ายได้ ใช้`Save()` วิธีการระบุเส้นทางแบบเต็มของไฟล์ที่ส่งออก

```csharp
// บันทึกไฟล์ Excel
workbook.Save(dataDir + "ClearingPageBreaks_out.xls");
```

### ตัวอย่างซอร์สโค้ดสำหรับ Excel ล้างตัวแบ่งหน้าทั้งหมดโดยใช้ Aspose.Cells สำหรับ .NET 

```csharp

//เส้นทางไปยังไดเร็กทอรีเอกสาร
string dataDir = "YOUR DOCUMENT DIRECTORY";
// การสร้างอินสแตนซ์วัตถุสมุดงาน
Workbook workbook = new Workbook();
// การล้างตัวแบ่งหน้าทั้งหมด
workbook.Worksheets[0].HorizontalPageBreaks.Clear();
workbook.Worksheets[0].VerticalPageBreaks.Clear();
// บันทึกไฟล์ Excel
workbook.Save(dataDir + "ClearAllPageBreaks_out.xls");

```

## บทสรุป

ในบทช่วยสอนนี้ เราได้เรียนรู้วิธีลบตัวแบ่งหน้าทั้งหมดในไฟล์ Excel โดยใช้ Aspose.Cells สำหรับ .NET ด้วยการทำตามขั้นตอนที่ให้ไว้ คุณสามารถจัดการและล้างตัวแบ่งหน้าที่ไม่ต้องการในไฟล์ Excel ที่สร้างขึ้นแบบไดนามิกของคุณได้อย่างง่ายดาย สำรวจคุณสมบัติเพิ่มเติมที่ Aspose.Cells นำเสนอเพิ่มเติมได้ตามสบายเพื่อการทำงานขั้นสูงยิ่งขึ้น

### คำถามที่พบบ่อย

#### ถาม: Aspose.Cells สำหรับ .NET เป็นไลบรารีฟรีหรือไม่

ตอบ: Aspose.Cells for .NET เป็นไลบรารีเชิงพาณิชย์ แต่มีเวอร์ชันทดลองใช้ฟรีที่คุณสามารถใช้เพื่อประเมินการทำงานของไลบรารีได้

#### ถาม: การลบตัวแบ่งหน้าส่งผลต่อองค์ประกอบแผ่นงานอื่นๆ หรือไม่

ตอบ: ไม่ การลบตัวแบ่งหน้าจะเปลี่ยนแปลงเฉพาะตัวแบ่งหน้าเท่านั้น และไม่ส่งผลต่อข้อมูลหรือการจัดรูปแบบอื่นๆ ในเวิร์กชีต

#### ถาม: ฉันสามารถลบตัวแบ่งหน้าบางส่วนใน Excel ได้หรือไม่

ตอบ: ได้ ด้วย Aspose.Cells คุณสามารถเข้าถึงตัวแบ่งหน้าแต่ละหน้าแยกกันและลบออกได้หากจำเป็นโดยใช้วิธีการที่เหมาะสม

#### ถาม: Aspose.Cells สำหรับ .NET รองรับไฟล์ Excel รูปแบบใดบ้าง

ตอบ: Aspose.Cells สำหรับ .NET รองรับไฟล์ Excel หลากหลายรูปแบบ เช่น XLSX, XLSM, CSV, HTML, PDF เป็นต้น

