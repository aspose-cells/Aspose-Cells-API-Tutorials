---
title: ตั้งค่าตัวคูณมาตราส่วน Excel
linktitle: ตั้งค่าตัวคูณมาตราส่วน Excel
second_title: Aspose.Cells สำหรับการอ้างอิง .NET API
description: เรียนรู้การจัดการไฟล์ Excel อย่างง่ายดายและปรับแต่งปัจจัยการปรับขนาดโดยใช้ Aspose.Cells สำหรับ .NET
type: docs
weight: 180
url: /th/net/excel-page-setup/set-excel-scaling-factor/
---
ในคู่มือนี้ เราจะอธิบายวิธีการตั้งค่าตัวคูณมาตราส่วนในสเปรดชีต Excel โดยใช้ Aspose.Cells สำหรับ .NET ทำตามขั้นตอนด้านล่างเพื่อทำภารกิจนี้ให้สำเร็จ

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

สร้างอินสแตนซ์ของวัตถุสมุดงานที่แสดงถึงสมุดงาน Excel ที่คุณต้องการสร้าง:

```csharp
Workbook workbook = new Workbook();
```

## ขั้นตอนที่ 5: เข้าถึงแผ่นงานแรก

นำทางไปยังแผ่นงานแรกในสมุดงาน Excel โดยใช้รหัสต่อไปนี้:

```csharp
Worksheet worksheet = workbook.Worksheets[0];
```

## ขั้นตอนที่ 6: ตั้งค่าปัจจัยสเกล

ตั้งค่าปัจจัยมาตราส่วนโดยใช้รหัสต่อไปนี้:

```csharp
worksheet.PageSetup.Zoom = 100;
```

ที่นี่เราได้ตั้งค่าปัจจัยมาตราส่วนเป็น 100 ซึ่งหมายความว่าสเปรดชีตจะแสดงที่ 100% ของขนาดปกติเมื่อพิมพ์

## ขั้นตอนที่ 7: บันทึกสมุดงาน Excel

 หากต้องการบันทึกเวิร์กบุ๊ก Excel ด้วยปัจจัยมาตราส่วนที่กำหนดไว้ ให้ใช้`Save` วิธีการของวัตถุสมุดงาน:

```csharp
workbook.Save(dataDir + "ScalingFactor_out.xls");
```

ซึ่งจะบันทึกเวิร์กบุ๊ก Excel ที่มีชื่อไฟล์ "ScalingFactor_out.xls" ในไดเร็กทอรีที่ระบุ

### ตัวอย่างซอร์สโค้ดสำหรับตั้งค่า Excel Scaling Factor โดยใช้ Aspose.Cells สำหรับ .NET 
```csharp
//เส้นทางไปยังไดเร็กทอรีเอกสาร
string dataDir = "YOUR DOCUMENT DIRECTORY";
// การสร้างอินสแตนซ์วัตถุสมุดงาน
Workbook workbook = new Workbook();
// การเข้าถึงแผ่นงานแรกในไฟล์ Excel
Worksheet worksheet = workbook.Worksheets[0];
// การตั้งค่าตัวคูณมาตราส่วนเป็น 100
worksheet.PageSetup.Zoom = 100;
// บันทึกสมุดงาน
workbook.Save(dataDir + "ScalingFactor_out.xls");
```

## บทสรุป

ขอแสดงความยินดี! คุณได้เรียนรู้วิธีตั้งค่าตัวคูณมาตราส่วนในสเปรดชีต Excel โดยใช้ Aspose.Cells สำหรับ .NET ปัจจัยการปรับขนาดช่วยให้คุณปรับขนาดของสเปรดชีตเมื่อพิมพ์เพื่อการแสดงผลที่เหมาะสมที่สุด

### คำถามที่พบบ่อย

#### 1. จะตั้งค่าตัวคูณมาตราส่วนในสเปรดชีต Excel ด้วย Aspose.Cells สำหรับ .NET ได้อย่างไร

 ใช้`Zoom` ทรัพย์สินของ`PageSetup`วัตถุเพื่อตั้งค่าปัจจัยการปรับขนาด ตัวอย่างเช่น,`worksheet.PageSetup.Zoom = 100;` จะตั้งค่าปัจจัยการปรับขนาดเป็น 100%

#### 2. ฉันสามารถปรับแต่งปัจจัยการปรับขนาดตามความต้องการของฉันได้หรือไม่?

 ใช่ คุณสามารถปรับปัจจัยการปรับขนาดได้โดยการเปลี่ยนค่าที่กำหนดให้กับ`Zoom` คุณสมบัติ. ตัวอย่างเช่น,`worksheet.PageSetup.Zoom = 75;` จะตั้งค่าปัจจัยการปรับขนาดเป็น 75%

#### 3. เป็นไปได้หรือไม่ที่จะบันทึกเวิร์กบุ๊ก Excel ด้วยตัวคูณมาตราส่วนที่กำหนดไว้

 ใช่ คุณสามารถใช้`Save` วิธีการของ`Workbook` วัตถุเพื่อบันทึกสมุดงาน Excel ด้วยปัจจัยมาตราส่วนที่กำหนดไว้