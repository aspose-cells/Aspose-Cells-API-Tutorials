---
title: รับความกว้างและความสูงของกระดาษแผ่นงาน
linktitle: รับความกว้างและความสูงของกระดาษแผ่นงาน
second_title: Aspose.Cells สำหรับการอ้างอิง .NET API
description: สร้างคำแนะนำทีละขั้นตอนเพื่ออธิบายซอร์สโค้ด C# ต่อไปนี้เพื่อรับความกว้างและความสูงของกระดาษของสเปรดชีตโดยใช้ Aspose.Cells สำหรับ .NET
type: docs
weight: 80
url: /th/net/excel-display-settings-csharp-tutorials/get-paper-width-and-height-of-worksheet/
---
ในบทช่วยสอนนี้ เราจะอธิบายทีละขั้นตอนเพื่ออธิบายซอร์สโค้ด C# ต่อไปนี้เพื่อรับความกว้างและความสูงของกระดาษของเวิร์กชีทโดยใช้ Aspose.Cells สำหรับ .NET ทำตามขั้นตอนด้านล่าง:

## ขั้นตอนที่ 1: สร้างสมุดงาน
 เริ่มต้นด้วยการสร้างสมุดงานใหม่โดยใช้`Workbook` ระดับ:

```csharp
Workbook wb = new Workbook();
```

## ขั้นตอนที่ 2: เข้าถึงแผ่นงานแรก
 จากนั้น นำทางไปยังแผ่นงานแรกในสมุดงานโดยใช้`Worksheet` ระดับ:

```csharp
Worksheet ws = wb.Worksheets[0];
```

## ขั้นตอนที่ 3: ตั้งค่าขนาดกระดาษเป็น A2 และแสดงความกว้างและความสูงของกระดาษเป็นนิ้ว
 ใช้`PaperSize` ทรัพย์สินของ`PageSetup` วัตถุเพื่อตั้งค่าขนาดกระดาษเป็น A2 จากนั้นใช้`PaperWidth` และ`PaperHeight` คุณสมบัติเพื่อให้ได้ความกว้างและความสูงของกระดาษตามลำดับ แสดงค่าเหล่านี้โดยใช้`Console.WriteLine` วิธี:

```csharp
ws.PageSetup.PaperSize = PaperSizeType.PaperA2;
Console.WriteLine("PaperA2: " + ws.PageSetup.PaperWidth + "x" + ws.PageSetup.PaperHeight);
```

## ขั้นตอนที่ 4: ทำซ้ำขั้นตอนสำหรับกระดาษขนาดอื่น
ทำซ้ำขั้นตอนก่อนหน้า เปลี่ยนขนาดกระดาษเป็น A3, A4 และ Letter จากนั้นแสดงค่าความกว้างและความสูงของกระดาษสำหรับแต่ละขนาด:

```csharp
ws.PageSetup.PaperSize = PaperSizeType.PaperA3;
Console.WriteLine("PaperA3: " + ws.PageSetup.PaperWidth + "x" + ws.PageSetup.PaperHeight);

ws.PageSetup.PaperSize = PaperSizeType.PaperA4;
Console.WriteLine("PaperA4: " + ws.PageSetup.PaperWidth + "x" + ws.PageSetup.PaperHeight);

ws.PageSetup.PaperSize = PaperSizeType.PaperLetter;
Console.WriteLine("PaperLetter: " + ws.PageSetup.PaperWidth + "x" + ws.PageSetup.PaperHeight);
```

### ซอร์สโค้ดตัวอย่างสำหรับรับความกว้างและความสูงของกระดาษแผ่นงานโดยใช้ Aspose.Cells สำหรับ .NET 

```csharp
//สร้างสมุดงาน
Workbook wb = new Workbook();
//เข้าถึงแผ่นงานแรก
Worksheet ws = wb.Worksheets[0];
//ตั้งค่าขนาดกระดาษเป็น A2 และพิมพ์ความกว้างและความสูงของกระดาษเป็นนิ้ว
ws.PageSetup.PaperSize = PaperSizeType.PaperA2;
Console.WriteLine("PaperA2: " + ws.PageSetup.PaperWidth + "x" + ws.PageSetup.PaperHeight);
//ตั้งค่าขนาดกระดาษเป็น A3 และพิมพ์ความกว้างและความสูงของกระดาษเป็นนิ้ว
ws.PageSetup.PaperSize = PaperSizeType.PaperA3;
Console.WriteLine("PaperA3: " + ws.PageSetup.PaperWidth + "x" + ws.PageSetup.PaperHeight);
//ตั้งค่าขนาดกระดาษเป็น A4 และพิมพ์ความกว้างและความสูงของกระดาษเป็นนิ้ว
ws.PageSetup.PaperSize = PaperSizeType.PaperA4;
Console.WriteLine("PaperA4: " + ws.PageSetup.PaperWidth + "x" + ws.PageSetup.PaperHeight);
//ตั้งค่าขนาดกระดาษเป็น Letter และพิมพ์ความกว้างและความสูงของกระดาษเป็นนิ้ว
ws.PageSetup.PaperSize = PaperSizeType.PaperLetter;
Console.WriteLine("PaperLetter: " + ws.PageSetup.PaperWidth + "x" + ws.PageSetup.PaperHeight);
```


## บทสรุป

คุณได้เรียนรู้วิธีใช้ Aspose.Cells สำหรับ .NET เพื่อรับความกว้างและความสูงของกระดาษของสเปรดชีต คุณลักษณะนี้มีประโยชน์สำหรับการกำหนดค่าและการจัดวางเอกสาร Excel ของคุณอย่างแม่นยำ

### คำถามที่พบบ่อย (FAQ)

#### Aspose.Cells สำหรับ .NET คืออะไร

Aspose.Cells for .NET เป็นไลบรารีที่มีประสิทธิภาพสำหรับจัดการและประมวลผลไฟล์ Excel ในแอปพลิเคชัน .NET มีคุณลักษณะมากมายสำหรับการสร้าง ปรับเปลี่ยน แปลง และวิเคราะห์ไฟล์ Excel

#### ฉันจะรับขนาดกระดาษของสเปรดชีตด้วย Aspose.Cells สำหรับ .NET ได้อย่างไร

 คุณสามารถใช้`PageSetup` ชั้นเรียนของ`Worksheet` วัตถุเพื่อเข้าถึงขนาดกระดาษ ใช้`PaperSize` คุณสมบัติเพื่อกำหนดขนาดกระดาษและ`PaperWidth` และ`PaperHeight` คุณสมบัติเพื่อให้ได้ความกว้างและความสูงของกระดาษตามลำดับ

#### Aspose.Cells for .NET รองรับกระดาษขนาดใดบ้าง

Aspose.Cells สำหรับ .NET รองรับขนาดกระดาษที่ใช้กันทั่วไปหลากหลายขนาด เช่น A2, A3, A4 และ Letter รวมถึงขนาดที่กำหนดเองอื่นๆ อีกมากมาย

#### ฉันสามารถกำหนดขนาดกระดาษของสเปรดชีตด้วย Aspose.Cells for .NET ได้หรือไม่

 ได้ คุณสามารถตั้งค่าขนาดกระดาษแบบกำหนดเองได้โดยการระบุขนาดความกว้างและความสูงที่แน่นอนโดยใช้`PaperWidth` และ`PaperHeight` คุณสมบัติของ`PageSetup` ระดับ.