---
title: รับขนาดหน้า
linktitle: รับขนาดหน้า
second_title: Aspose.Cells สำหรับการอ้างอิง .NET API
description: เรียนรู้วิธีดึงข้อมูลขนาดหน้าใน Excel โดยใช้ Aspose.Cells สำหรับ .NET คำแนะนำทีละขั้นตอนพร้อมซอร์สโค้ดใน C#
type: docs
weight: 40
url: /th/net/excel-page-setup/get-page-dimensions/
---
Aspose.Cells for .NET เป็นไลบรารีอันทรงพลังที่ช่วยให้นักพัฒนาสามารถทำงานกับไฟล์ Microsoft Excel โดยทางโปรแกรม มีคุณสมบัติมากมายสำหรับจัดการเอกสาร Excel รวมถึงความสามารถในการรับขนาดหน้า ในบทช่วยสอนนี้ เราจะแนะนำคุณตลอดขั้นตอนในการดึงข้อมูลขนาดหน้าโดยใช้ Aspose.Cells สำหรับ .NET

## ขั้นตอนที่ 1: สร้างอินสแตนซ์ของคลาสสมุดงาน

ในการเริ่มต้น เราต้องสร้างอินสแตนซ์ของคลาสสมุดงาน ซึ่งแสดงถึงสมุดงาน Excel สามารถทำได้โดยใช้รหัสต่อไปนี้:

```csharp
Workbook book = new Workbook();
```

## ขั้นตอนที่ 2: การเข้าถึงสเปรดชีต

ต่อไป เราจำเป็นต้องนำทางไปยังแผ่นงานในสมุดงานที่เราต้องการตั้งค่าขนาดหน้า ในตัวอย่างนี้ สมมติว่าเราต้องการทำงานกับแผ่นงานแรก เราสามารถเข้าถึงได้โดยใช้รหัสต่อไปนี้:

```csharp
Worksheet sheet = book.Worksheets[0];
```

## ขั้นตอนที่ 3: ตั้งค่าขนาดกระดาษเป็น A2 และพิมพ์ความกว้างและความสูงเป็นนิ้ว

ตอนนี้เราจะตั้งค่าขนาดกระดาษเป็น A2 และพิมพ์ความกว้างและความสูงของหน้าเป็นนิ้ว สามารถทำได้โดยใช้รหัสต่อไปนี้:

```csharp
sheet.PageSetup.PaperSize = PaperSizeType.PaperA2;
Console.WriteLine("A2: " + sheet.PageSetup.PaperWidth + "x" + sheet.PageSetup.PaperHeight);
```

## ขั้นตอนที่ 4: ตั้งค่าขนาดกระดาษเป็น A3 และพิมพ์ความกว้างและความสูงเป็นนิ้ว

ต่อไป เราจะตั้งค่าขนาดกระดาษเป็น A3 และพิมพ์ความกว้างและความสูงของหน้าเป็นนิ้ว นี่คือรหัสที่เกี่ยวข้อง:

```csharp
sheet.PageSetup.PaperSize = PaperSizeType.PaperA3;
Console.WriteLine("A3: " + sheet.PageSetup.PaperWidth + "x" + sheet.PageSetup.PaperHeight);
```

## ขั้นตอนที่ 5: ตั้งค่าขนาดกระดาษเป็น A4 และพิมพ์ความกว้างและความสูงเป็นนิ้ว

ตอนนี้เราจะตั้งค่าขนาดกระดาษเป็น A4 และพิมพ์ความกว้างและความสูงของหน้าเป็นนิ้ว นี่คือรหัส:

```csharp
sheet.PageSetup.PaperSize = PaperSizeType.PaperA4;
Console.WriteLine("A4: " + sheet.PageSetup.PaperWidth + "x" + sheet.PageSetup.PaperHeight);
```

## ขั้นตอนที่ 6: ตั้งค่าขนาดกระดาษเป็น Letter และพิมพ์ความกว้างและความสูงเป็นนิ้ว

สุดท้าย เราจะตั้งค่าขนาดกระดาษเป็น Letter และพิมพ์ความกว้างและความสูงของหน้าเป็นนิ้ว นี่คือรหัส:

```csharp
sheet.PageSetup.PaperSize = PaperSizeType.PaperLetter;
Console.WriteLine("Letter: " + sheet.PageSetup.PaperWidth + "x" + sheet.PageSetup.PaperHeight);
```

### ตัวอย่างซอร์สโค้ดสำหรับรับขนาดหน้าโดยใช้ Aspose.Cells สำหรับ .NET 
```csharp
// สร้างอินสแตนซ์ของคลาสสมุดงาน
Workbook book = new Workbook();
// เข้าถึงแผ่นงานแรก
Worksheet sheet = book.Worksheets[0];
// ตั้งค่าขนาดกระดาษเป็น A2 และพิมพ์ความกว้างและความสูงของกระดาษเป็นนิ้ว
sheet.PageSetup.PaperSize = PaperSizeType.PaperA2;
Console.WriteLine("PaperA2: " + sheet.PageSetup.PaperWidth + "x" + sheet.PageSetup.PaperHeight);
// ตั้งค่าขนาดกระดาษเป็น A3 และพิมพ์ความกว้างและความสูงของกระดาษเป็นนิ้ว
sheet.PageSetup.PaperSize = PaperSizeType.PaperA3;
Console.WriteLine("PaperA3: " + sheet.PageSetup.PaperWidth + "x" + sheet.PageSetup.PaperHeight);
// ตั้งค่าขนาดกระดาษเป็น A4 และพิมพ์ความกว้างและความสูงของกระดาษเป็นนิ้ว
sheet.PageSetup.PaperSize = PaperSizeType.PaperA4;
Console.WriteLine("PaperA4: " + sheet.PageSetup.PaperWidth + "x" + sheet.PageSetup.PaperHeight);
// ตั้งค่าขนาดกระดาษเป็น Letter และพิมพ์ความกว้างและความสูงของกระดาษเป็นนิ้ว
sheet.PageSetup.PaperSize = PaperSizeType.PaperLetter;
Console.WriteLine("PaperLetter: " + sheet.PageSetup.PaperWidth + "x" + sheet.PageSetup.PaperHeight);
Console.WriteLine("GetPageDimensions executed successfully.\r\n");
```

## บทสรุป

ขอแสดงความยินดี! คุณได้เรียนรู้วิธีดึงข้อมูลขนาดหน้าโดยใช้ Aspose.Cells สำหรับ .NET คุณลักษณะนี้จะมีประโยชน์เมื่อคุณต้องการดำเนินการเฉพาะตามขนาดหน้าในไฟล์ Excel ของคุณ

อย่าลืมสำรวจเอกสารประกอบของ Aspose.Cells เพิ่มเติมเพื่อค้นพบคุณสมบัติอันทรงพลังทั้งหมดที่มีให้

### คำถามที่พบบ่อย

#### 1. Aspose.Cells for .NET รองรับกระดาษขนาดใดอีกบ้าง

Aspose.Cells สำหรับ .NET รองรับกระดาษหลากหลายขนาด รวมถึง A1, A5, B4, B5, Executive, Legal, Letter และอื่นๆ อีกมากมาย คุณสามารถตรวจสอบเอกสารเพื่อดูรายการขนาดกระดาษที่รองรับทั้งหมด

#### 2. ฉันสามารถกำหนดขนาดเพจแบบกำหนดเองด้วย Aspose.Cells สำหรับ .NET ได้หรือไม่

ได้ คุณสามารถกำหนดขนาดหน้าเองได้โดยการระบุความกว้างและความสูงที่ต้องการ Aspose.Cells มอบความยืดหยุ่นอย่างเต็มที่ในการปรับแต่งขนาดหน้าตามความต้องการของคุณ

#### 3. ฉันสามารถรับขนาดหน้าเป็นหน่วยอื่นที่ไม่ใช่นิ้วได้หรือไม่

ใช่ Aspose.Cells สำหรับ .NET ช่วยให้คุณรับขนาดหน้าในหน่วยต่างๆ รวมถึงนิ้ว เซนติเมตร มิลลิเมตร และจุด

#### 4. Aspose.Cells for .NET รองรับคุณสมบัติการแก้ไขการตั้งค่าเพจอื่นๆ หรือไม่

ใช่ Aspose.Cells นำเสนอคุณสมบัติเต็มรูปแบบสำหรับการแก้ไขการตั้งค่าหน้า รวมถึงการตั้งค่าระยะขอบ การวางแนว ส่วนหัวและส่วนท้าย ฯลฯ