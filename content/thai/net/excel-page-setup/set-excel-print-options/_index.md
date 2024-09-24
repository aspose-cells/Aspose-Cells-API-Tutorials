---
title: ตั้งค่าตัวเลือกการพิมพ์ของ Excel
linktitle: ตั้งค่าตัวเลือกการพิมพ์ของ Excel
second_title: Aspose.Cells สำหรับการอ้างอิง .NET API
description: เรียนรู้วิธีจัดการไฟล์ Excel และปรับแต่งตัวเลือกการพิมพ์อย่างง่ายดายโดยใช้ Aspose.Cells สำหรับ .NET
type: docs
weight: 150
url: /th/net/excel-page-setup/set-excel-print-options/
---
ในคู่มือนี้ เราจะอธิบายวิธีการตั้งค่าตัวเลือกการพิมพ์สำหรับสมุดงาน Excel โดยใช้ Aspose.Cells for .NET เราจะนำคุณไปทีละขั้นตอนผ่านซอร์สโค้ด C# ที่ให้มาเพื่อทำงานนี้ให้สำเร็จ

## ขั้นตอนที่ 1: การตั้งค่าสภาพแวดล้อม

ก่อนที่คุณจะเริ่มต้น ตรวจสอบให้แน่ใจว่าคุณได้ตั้งค่าสภาพแวดล้อมการพัฒนาและติดตั้ง Aspose.Cells สำหรับ .NET แล้ว คุณสามารถดาวน์โหลดไลบรารีเวอร์ชันล่าสุดได้จากเว็บไซต์อย่างเป็นทางการของ Aspose

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

## ขั้นตอนที่ 5: รับการอ้างอิง PageSetup ของแผ่นงาน

ในการตั้งค่าตัวเลือกการพิมพ์ เราต้องได้รับการอ้างอิง PageSetup จากเวิร์กชีตก่อน ใช้รหัสต่อไปนี้เพื่อรับข้อมูลอ้างอิง:

```csharp
PageSetup pageSetup = workbook.Worksheets[0].PageSetup;
```

## ขั้นตอนที่ 6: เปิดใช้งานการพิมพ์เส้นตาราง

หากต้องการเปิดใช้งานเส้นตารางที่จะพิมพ์ ให้ใช้รหัสต่อไปนี้:

```csharp
pageSetup. PrintGridlines = true;
```

## ขั้นตอนที่ 7: เปิดใช้งานการพิมพ์ส่วนหัวของแถว/คอลัมน์

หากต้องการเปิดใช้งานการพิมพ์ส่วนหัวของแถวและคอลัมน์ ให้ใช้รหัสต่อไปนี้:

```csharp
pageSetup.PrintHeadings = true;
```

## ขั้นตอนที่ 8: เปิดใช้งานโหมดการพิมพ์ขาวดำ

หากต้องการเปิดใช้งานการพิมพ์แผ่นงานในโหมดขาวดำ ให้ใช้รหัสต่อไปนี้:

```csharp
pageSetup.BlackAndWhite = true;
```

## ขั้นตอนที่ 9: การเปิดใช้งานการพิมพ์คำติชม

หากต้องการอนุญาตให้พิมพ์ความคิดเห็นตามที่ปรากฏบนสเปรดชีต ให้ใช้รหัสต่อไปนี้:

```csharp
pageSetup.PrintComments = PrintCommentsType.PrintInPlace;
```

## ขั้นตอนที่ 10: เปิดใช้งานการพิมพ์โหมดร่าง

หากต้องการเปิดใช้งานการพิมพ์สเปรดชีตในโหมดร่าง ให้ใช้รหัสต่อไปนี้:

```csharp
pageSetup.PrintDraft = true;
```

## ขั้นตอนที่ 11: เปิดใช้งานข้อผิดพลาดในการพิมพ์เซลล์เป็น N/A

เพื่อให้เซลล์มีข้อผิดพลาดในการพิมพ์เป็น

  กว่า N/A ให้ใช้รหัสต่อไปนี้:

```csharp
pageSetup.PrintErrors = PrintErrorsType.PrintErrorsNA;
```

## ขั้นตอนที่ 12: บันทึกสมุดงาน Excel

 หากต้องการบันทึกเวิร์กบุ๊ก Excel ด้วยการตั้งค่าตัวเลือกการพิมพ์ ให้ใช้`Save` วิธีการของวัตถุสมุดงาน:

```csharp
workbook.Save(dataDir + "OtherPrintOptions_out.xls");
```

ซึ่งจะบันทึกสมุดงาน Excel ที่มีชื่อไฟล์ "OtherPrintOptions_out.xls" ในไดเร็กทอรีที่ระบุ

### ตัวอย่างซอร์สโค้ดสำหรับตั้งค่าตัวเลือกการพิมพ์ของ Excel โดยใช้ Aspose.Cells สำหรับ .NET 
```csharp
//เส้นทางไปยังไดเร็กทอรีเอกสาร
string dataDir = "YOUR DOCUMENT DIRECTORY";
// การสร้างอินสแตนซ์วัตถุสมุดงาน
Workbook workbook = new Workbook();
// การรับการอ้างอิงของ PageSetup ของแผ่นงาน
PageSetup pageSetup = workbook.Worksheets[0].PageSetup;
// อนุญาตให้พิมพ์เส้นตาราง
pageSetup.PrintGridlines = true;
// อนุญาตให้พิมพ์ส่วนหัวของแถว/คอลัมน์
pageSetup.PrintHeadings = true;
// อนุญาตให้พิมพ์แผ่นงานในโหมดขาวดำ
pageSetup.BlackAndWhite = true;
// อนุญาตให้พิมพ์ความคิดเห็นตามที่แสดงบนแผ่นงาน
pageSetup.PrintComments = PrintCommentsType.PrintInPlace;
// ช่วยให้สามารถพิมพ์แผ่นงานที่มีคุณภาพแบบร่างได้
pageSetup.PrintDraft = true;
// อนุญาตให้พิมพ์ข้อผิดพลาดของเซลล์เป็น N/A
pageSetup.PrintErrors = PrintErrorsType.PrintErrorsNA;
// บันทึกสมุดงาน
workbook.Save(dataDir + "OtherPrintOptions_out.xls");
```
## บทสรุป

ตอนนี้ คุณได้เรียนรู้วิธีตั้งค่าตัวเลือกการพิมพ์สำหรับสมุดงาน Excel โดยใช้ Aspose.Cells for .NET แล้ว ไลบรารีที่ทรงพลังและใช้งานง่ายนี้ช่วยให้คุณปรับแต่งการตั้งค่าการพิมพ์ของเวิร์กบุ๊ก Excel ของคุณได้อย่างง่ายดายและมีประสิทธิภาพ

### คำถามที่พบบ่อย


#### 1. ฉันสามารถปรับแต่งตัวเลือกการพิมพ์เพิ่มเติม เช่น ระยะขอบหรือการวางแนวหน้าได้หรือไม่

ใช่ Aspose.Cells สำหรับ .NET มีตัวเลือกการพิมพ์ที่ปรับแต่งได้มากมาย เช่น ระยะขอบ การวางแนวหน้า มาตราส่วน ฯลฯ

#### 2. Aspose.Cells สำหรับ .NET รองรับไฟล์ Excel รูปแบบอื่นหรือไม่

ใช่ Aspose.Cells สำหรับ .NET รองรับรูปแบบไฟล์ Excel ที่หลากหลาย เช่น XLSX, XLS, CSV, HTML, PDF เป็นต้น

#### 3. Aspose.Cells สำหรับ .NET เข้ากันได้กับ .NET Framework ทุกเวอร์ชันหรือไม่

Aspose.Cells สำหรับ .NET เข้ากันได้กับ .NET Framework 2.0 หรือใหม่กว่า รวมถึงเวอร์ชัน 3.5, 4.0, 4.5, 4.6 เป็นต้น