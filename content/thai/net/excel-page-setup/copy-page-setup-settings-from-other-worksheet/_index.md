---
title: คัดลอกการตั้งค่าการตั้งค่าหน้าจากแผ่นงานอื่น
linktitle: คัดลอกการตั้งค่าการตั้งค่าหน้าจากแผ่นงานอื่น
second_title: Aspose.Cells สำหรับการอ้างอิง .NET API
description: เรียนรู้วิธีคัดลอกการตั้งค่าการกำหนดค่าเพจจากสเปรดชีตหนึ่งไปยังอีกสเปรดชีตโดยใช้ Aspose.Cells สำหรับ .NET คำแนะนำทีละขั้นตอนเพื่อเพิ่มประสิทธิภาพการใช้ไลบรารีนี้
type: docs
weight: 10
url: /th/net/excel-page-setup/copy-page-setup-settings-from-other-worksheet/
---
ในบทความนี้ เราจะอธิบายทีละขั้นตอนเพื่ออธิบายซอร์สโค้ด C# ต่อไปนี้: คัดลอกการตั้งค่าการกำหนดค่าเพจจากสเปรดชีตอื่นโดยใช้ Aspose.Cells สำหรับ .NET เราจะใช้ไลบรารี Aspose.Cells สำหรับ .NET เพื่อดำเนินการนี้ หากคุณต้องการคัดลอกการตั้งค่าการตั้งค่าหน้าจากแผ่นงานหนึ่งไปยังอีกแผ่นงาน ให้ทำตามขั้นตอนด้านล่าง

## ขั้นตอนที่ 1: การสร้างสมุดงาน
ขั้นตอนแรกคือการสร้างสมุดงาน ในกรณีของเรา เราจะใช้คลาส Workbook ที่จัดทำโดยไลบรารี Aspose.Cells นี่คือรหัสในการสร้างสมุดงาน:

```csharp
Workbook wb = new Workbook();
```

## ขั้นตอนที่ 2: การเพิ่มแผ่นงานทดสอบ
หลังจากสร้างสมุดงานแล้ว เราจำเป็นต้องเพิ่มแผ่นงานทดสอบ ในตัวอย่างนี้ เราจะเพิ่มแผ่นงานสองแผ่น นี่คือโค้ดสำหรับเพิ่มสองแผ่นงาน:

```csharp
wb.Worksheets.Add("TestSheet1");
wb.Worksheets.Add("TestSheet2");
```

## ขั้นตอนที่ 3: การเข้าถึงแผ่นงาน
ตอนนี้เราได้เพิ่มเวิร์กชีตแล้ว เราจำเป็นต้องเข้าถึงเวิร์กชีตจึงจะสามารถเปลี่ยนการตั้งค่าได้ เราจะเข้าถึงแผ่นงาน "TestSheet1" และ "TestSheet2" โดยใช้ชื่อ นี่คือรหัสในการเข้าถึง:

```csharp
Worksheet TestSheet1 = wb. Worksheets["TestSheet1"];
Worksheet TestSheet2 = wb. Worksheets["TestSheet2"];
```

## ขั้นตอนที่ 4: การตั้งค่าขนาดกระดาษ
 ในขั้นตอนนี้ เราจะตั้งค่าขนาดกระดาษของแผ่นงาน "TestSheet1" เราจะใช้`PageSetup.PaperSize` คุณสมบัติสำหรับกำหนดขนาดกระดาษ ตัวอย่างเช่น เราจะตั้งค่าขนาดกระดาษเป็น "PaperA3ExtraTransverse" นี่คือรหัสสำหรับสิ่งนั้น:

```csharp
TestSheet1.PageSetup.PaperSize = PaperSizeType.PaperA3ExtraTransverse;
```

## ขั้นตอนที่ 5: การคัดลอกการตั้งค่าการตั้งค่าหน้า
ตอนนี้เราจะคัดลอกการตั้งค่าการกำหนดค่าหน้าจากแผ่นงาน "TestSheet1" ไปที่ "TestSheet2" เราจะใช้`PageSetup.Copy` วิธีดำเนินการนี้ นี่คือรหัสสำหรับสิ่งนั้น:

```csharp
TestSheet2.PageSetup.Copy(TestSheet1.PageSetup, new CopyOptions());
```

## ขั้นตอนที่ 6: การพิมพ์ขนาดกระดาษ
 หลังจากคัดลอกการตั้งค่าการตั้งค่าหน้าแล้ว เราจะพิมพ์ขนาดกระดาษของทั้งสองแผ่นงาน เราจะใช้`Console.WriteLine` เพื่อแสดงขนาดกระดาษ นี่คือรหัสสำหรับสิ่งนั้น:

```csharp
Console.WriteLine("Before Paper Size: " + TestSheet1.PageSetup.PaperSize);
Console.WriteLine("Before Paper Size: " + TestSheet2.PageSetup.PaperSize);
```

### ตัวอย่างซอร์สโค้ดสำหรับการตั้งค่าการคัดลอกเพจจากแผ่นงานอื่นโดยใช้ Aspose.Cells สำหรับ .NET 
```csharp
//สร้างสมุดงาน
Workbook wb = new Workbook();
//เพิ่มแผ่นงานทดสอบสองแผ่น
wb.Worksheets.Add("TestSheet1");
wb.Worksheets.Add("TestSheet2");
//เข้าถึงทั้งแผ่นงานเป็น TestSheet1 และ TestSheet2
Worksheet TestSheet1 = wb.Worksheets["TestSheet1"];
Worksheet TestSheet2 = wb.Worksheets["TestSheet2"];
//ตั้งค่าขนาดกระดาษของ TestSheet1 เป็น PaperA3ExtraTransverse
TestSheet1.PageSetup.PaperSize = PaperSizeType.PaperA3ExtraTransverse;
//พิมพ์ขนาดกระดาษของทั้งสองแผ่นงาน
Console.WriteLine("Before Paper Size: " + TestSheet1.PageSetup.PaperSize);
Console.WriteLine("Before Paper Size: " + TestSheet2.PageSetup.PaperSize);
Console.WriteLine();
//คัดลอก PageSetup จาก TestSheet1 ไปยัง TestSheet2
TestSheet2.PageSetup.Copy(TestSheet1.PageSetup, new CopyOptions());
//พิมพ์ขนาดกระดาษของทั้งสองแผ่นงาน
Console.WriteLine("After Paper Size: " + TestSheet1.PageSetup.PaperSize);
Console.WriteLine("After Paper Size: " + TestSheet2.PageSetup.PaperSize);
Console.WriteLine();
Console.WriteLine("CopyPageSetupSettingsFromSourceWorksheetToDestinationWorksheet executed successfully.\r\n");
```

## บทสรุป
ในบทความนี้ เราได้เรียนรู้วิธีคัดลอกการตั้งค่าการกำหนดค่าเพจจากเวิร์กชีตหนึ่งไปยังอีกเวิร์กชีตโดยใช้ Aspose.Cells สำหรับ .NET เราทำตามขั้นตอนต่อไปนี้: การสร้างสมุดงาน การเพิ่มแผ่นงานทดสอบ การเข้าถึงแผ่นงาน การตั้งค่าขนาดกระดาษ การคัดลอกการตั้งค่าการตั้งค่าหน้า และการพิมพ์ขนาดกระดาษ ตอนนี้คุณสามารถใช้ความรู้นี้เพื่อคัดลอกการตั้งค่าการกำหนดค่าเพจไปยังโปรเจ็กต์ของคุณเองได้

### คำถามที่พบบ่อย

#### ถาม: ฉันสามารถคัดลอกการตั้งค่าการกำหนดค่าหน้าระหว่างอินสแตนซ์สมุดงานต่างๆ ได้หรือไม่

 ตอบ: ได้ คุณสามารถคัดลอกการตั้งค่าการตั้งค่าหน้าระหว่างอินสแตนซ์สมุดงานต่างๆ ได้โดยใช้`PageSetup.Copy` วิธีการของไลบรารี Aspose.Cells

#### ถาม: ฉันสามารถคัดลอกการตั้งค่าการตั้งค่าหน้าอื่นๆ เช่น การวางแนวหรือระยะขอบได้หรือไม่

 ตอบ: ได้ คุณสามารถคัดลอกการตั้งค่าการตั้งค่าหน้าอื่นๆ ได้โดยใช้`PageSetup.Copy` วิธีการพร้อมตัวเลือกที่เหมาะสม ตัวอย่างเช่น คุณสามารถคัดลอกการวางแนวโดยใช้`CopyOptions.Orientation` และระยะขอบโดยใช้`CopyOptions.Margins`.

#### ถาม: ฉันจะทราบได้อย่างไรว่ามีตัวเลือกใดบ้างสำหรับขนาดกระดาษ

ตอบ: คุณสามารถตรวจสอบการอ้างอิง API ไลบรารี Aspose.Cells เพื่อดูตัวเลือกขนาดกระดาษที่ใช้ได้ มีการแจงนับที่เรียกว่า`PaperSizeType` ซึ่งแสดงรายการขนาดกระดาษต่างๆ ที่รองรับ

#### ถาม: ฉันจะดาวน์โหลดไลบรารี Aspose.Cells สำหรับ .NET ได้อย่างไร

 ตอบ: คุณสามารถดาวน์โหลดไลบรารี Aspose.Cells สำหรับ .NET ได้จาก[กำหนดเผยแพร่](https://releases.aspose.com/cells/net). มีเวอร์ชันทดลองใช้งานฟรี รวมถึงใบอนุญาตแบบชำระเงินสำหรับการใช้งานเชิงพาณิชย์

#### ถาม: ไลบรารี Aspose.Cells รองรับภาษาการเขียนโปรแกรมอื่นๆ หรือไม่

ตอบ: ใช่ ไลบรารี Aspose.Cells รองรับภาษาการเขียนโปรแกรมหลายภาษา รวมถึง C#, Java, Python และอื่นๆ อีกมากมาย