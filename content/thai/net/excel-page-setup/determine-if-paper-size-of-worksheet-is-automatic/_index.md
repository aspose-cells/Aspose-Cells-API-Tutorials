---
title: ตรวจสอบว่าขนาดกระดาษของแผ่นงานเป็นแบบอัตโนมัติหรือไม่
linktitle: ตรวจสอบว่าขนาดกระดาษของแผ่นงานเป็นแบบอัตโนมัติหรือไม่
second_title: Aspose.Cells สำหรับการอ้างอิง .NET API
description: เรียนรู้วิธีตรวจสอบว่าขนาดกระดาษของสเปรดชีตเป็นแบบอัตโนมัติด้วย Aspose.Cells for .NET หรือไม่
type: docs
weight: 20
url: /th/net/excel-page-setup/determine-if-paper-size-of-worksheet-is-automatic/
---
ในบทความนี้ เราจะอธิบายทีละขั้นตอนเพื่ออธิบายซอร์สโค้ด C# ต่อไปนี้: ตรวจสอบว่าขนาดกระดาษของเวิร์กชีตเป็นแบบอัตโนมัติหรือไม่โดยใช้ Aspose.Cells สำหรับ .NET เราจะใช้ไลบรารี Aspose.Cells สำหรับ .NET เพื่อดำเนินการนี้ ทำตามขั้นตอนด้านล่างเพื่อตรวจสอบว่าขนาดกระดาษของเวิร์กชีตเป็นแบบอัตโนมัติหรือไม่

## ขั้นตอนที่ 1: กำลังโหลดสมุดงาน
ขั้นตอนแรกคือการโหลดสมุดงาน เราจะมีสมุดงานสองเล่ม: เล่มหนึ่งปิดใช้งานขนาดกระดาษอัตโนมัติ และอีกเล่มเปิดใช้งานขนาดกระดาษอัตโนมัติ นี่คือรหัสในการโหลดสมุดงาน:

```csharp
// ไดเรกทอรีต้นทาง
string sourceDir = "YOUR_SOURCE_DIR";
// ไดเร็กทอรีเอาต์พุต
string outputDir = "YOUR_OUTPUT_DIRECTORY";

// ใส่เวิร์กบุคแรกโดยปิดใช้งานขนาดกระดาษอัตโนมัติ
Workbook wb1 = new Workbook(sourceDir + "samplePageSetupIsAutomaticPaperSize-False.xlsx");

// โหลดสมุดงานที่สองโดยเปิดใช้งานขนาดกระดาษอัตโนมัติ
Workbook wb2 = new Workbook(sourceDir + "samplePageSetupIsAutomaticPaperSize-True.xlsx");
```

## ขั้นตอนที่ 2: การเข้าถึงสเปรดชีต
ตอนนี้เราได้โหลดสมุดงานแล้ว เราจำเป็นต้องเข้าถึงแผ่นงานเพื่อให้เราตรวจสอบขนาดกระดาษอัตโนมัติได้ เราจะไปที่แผ่นงานแรกของสมุดงานทั้งสองเล่ม นี่คือรหัสในการเข้าถึง:

```csharp
//ไปที่แผ่นงานแรกของสมุดงานแรก
Worksheet ws11 = wb1.Worksheets[0];

// ไปที่แผ่นงานแรกของสมุดงานที่สอง
Worksheet ws12 = wb2.Worksheets[0];
```

## ขั้นตอนที่ 3: ตรวจสอบขนาดกระดาษอัตโนมัติ
 ในขั้นตอนนี้ เราจะตรวจสอบว่าขนาดกระดาษเวิร์กชีทเป็นแบบอัตโนมัติหรือไม่ เราจะใช้`PageSetup.IsAutomaticPaperSize` คุณสมบัติเพื่อรับข้อมูลนี้ จากนั้นเราจะแสดงผล นี่คือรหัสสำหรับสิ่งนั้น:

```csharp
// แสดงคุณสมบัติ IsAutomaticPaperSize ของเวิร์กชีตแรกในเวิร์กบุ๊กแรก
Console.WriteLine("First worksheet in first workbook - IsAutomaticPaperSize: " + ws11.PageSetup.IsAutomaticPaperSize);

// แสดงคุณสมบัติ IsAutomaticPaperSize ของแผ่นงานแรกในสมุดงานที่สอง
Console.WriteLine("First worksheet of second workbook - IsAutomaticPaperSize: " + ws12.PageSetup.IsAutomaticPaperSize);

```

### ซอร์สโค้ดตัวอย่างสำหรับการพิจารณาว่าขนาดกระดาษของแผ่นงานเป็นแบบอัตโนมัติหรือไม่โดยใช้ Aspose.Cells สำหรับ .NET 
```csharp
//ไดเรกทอรีต้นทาง
string sourceDir = "YOUR_SOURCE_DIRECTORY";
//ไดเร็กทอรีเอาต์พุต
string outputDir = "YOUR_OUTPUT_DIRECTORY";
//โหลดสมุดงานแรกที่มีขนาดกระดาษอัตโนมัติเป็นเท็จ
Workbook wb1 = new Workbook(sourceDir + "samplePageSetupIsAutomaticPaperSize-False.xlsx");
//ใส่สมุดงานที่สองโดยให้มีขนาดกระดาษอัตโนมัติเป็นจริง
Workbook wb2 = new Workbook(sourceDir + "samplePageSetupIsAutomaticPaperSize-True.xlsx");
//เข้าถึงแผ่นงานแรกของทั้งสองสมุดงาน
Worksheet ws11 = wb1.Worksheets[0];
Worksheet ws12 = wb2.Worksheets[0];
//พิมพ์คุณสมบัติ PageSetup.IsAutomaticPaperSize ของแผ่นงานทั้งสอง
Console.WriteLine("First Worksheet of First Workbook - IsAutomaticPaperSize: " + ws11.PageSetup.IsAutomaticPaperSize);
Console.WriteLine("First Worksheet of Second Workbook - IsAutomaticPaperSize: " + ws12.PageSetup.IsAutomaticPaperSize);
Console.WriteLine();
Console.WriteLine("DetermineIfPaperSizeOfWorksheetIsAutomatic executed successfully.\r\n");
```


## บทสรุป
ในบทความนี้ เราได้เรียนรู้วิธีตรวจสอบว่าขนาดกระดาษของเวิร์กชีตเป็นแบบอัตโนมัติหรือไม่โดยใช้ Aspose.Cells สำหรับ .NET เราทำตามขั้นตอนต่อไปนี้: การโหลดสมุดงาน

เข้าถึงสเปรดชีตและการตรวจสอบขนาดกระดาษอัตโนมัติ ตอนนี้คุณสามารถใช้ความรู้นี้เพื่อพิจารณาว่าขนาดกระดาษของสเปรดชีตของคุณเป็นแบบอัตโนมัติหรือไม่

### คำถามที่พบบ่อย

#### ถาม: ฉันจะโหลดสมุดงานด้วย Aspose.Cells สำหรับ .NET ได้อย่างไร

ตอบ: คุณสามารถโหลดสมุดงานโดยใช้คลาสสมุดงานจากไลบรารี Aspose.Cells ใช้วิธีWorkbook.Loadเพื่อโหลดสมุดงานจากไฟล์

#### ถาม: ฉันสามารถตรวจสอบขนาดกระดาษอัตโนมัติสำหรับสเปรดชีตอื่นได้หรือไม่

ตอบ: ได้ คุณสามารถตรวจสอบขนาดกระดาษอัตโนมัติสำหรับเวิร์กชีทใดๆ ได้โดยเข้าไปที่คุณสมบัติ PageSetup.IsAutomaticPaperSize ของออบเจ็กต์ Worksheet ที่เกี่ยวข้อง

#### ถาม: ฉันจะเปลี่ยนขนาดกระดาษอัตโนมัติของสเปรดชีตได้อย่างไร

ตอบ: เมื่อต้องการเปลี่ยนขนาดกระดาษอัตโนมัติของเวิร์กชีต คุณสามารถใช้คุณสมบัติ PageSetup.IsAutomaticPaperSize และตั้งค่าให้เป็นค่าที่ต้องการ (จริงหรือเท็จ)

#### ถาม: Aspose.Cells สำหรับ .NET มีคุณสมบัติอื่นใดอีกบ้าง

ตอบ: Aspose.Cells for .NET นำเสนอคุณสมบัติมากมายสำหรับการทำงานกับสเปรดชีต เช่น การสร้าง การแก้ไข และการแปลงเวิร์กบุ๊ก รวมถึงการจัดการข้อมูล สูตร และการจัดรูปแบบ