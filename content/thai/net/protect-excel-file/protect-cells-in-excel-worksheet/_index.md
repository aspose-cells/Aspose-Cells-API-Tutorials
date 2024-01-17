---
title: ปกป้องเซลล์ในแผ่นงาน Excel
linktitle: ปกป้องเซลล์ในแผ่นงาน Excel
second_title: Aspose.Cells สำหรับการอ้างอิง .NET API
description: เรียนรู้วิธีปกป้องเซลล์เฉพาะใน Excel ด้วย Aspose.Cells สำหรับ .NET บทช่วยสอนทีละขั้นตอนใน C#
type: docs
weight: 30
url: /th/net/protect-excel-file/protect-cells-in-excel-worksheet/
---
Microsoft Excel เป็นเครื่องมือที่ใช้กันอย่างแพร่หลายในการสร้างและจัดการสเปรดชีต หนึ่งในคุณสมบัติหลักของ Excel คือความสามารถในการปกป้องเซลล์บางเซลล์เพื่อรักษาความสมบูรณ์ของข้อมูล ในบทช่วยสอนนี้ เราจะแนะนำคุณทีละขั้นตอนในการปกป้องเซลล์เฉพาะในสเปรดชีต Excel โดยใช้ Aspose.Cells สำหรับ .NET Aspose.Cells for .NET เป็นไลบรารีการเขียนโปรแกรมอันทรงพลังที่ทำให้การจัดการไฟล์ Excel เป็นเรื่องง่ายด้วยความยืดหยุ่นและฟีเจอร์ขั้นสูง ทำตามขั้นตอนที่ให้ไว้เพื่อเรียนรู้วิธีปกป้องเซลล์สำคัญของคุณและรักษาข้อมูลของคุณให้ปลอดภัย

## ขั้นตอนที่ 1: การตั้งค่าสภาพแวดล้อม

ตรวจสอบให้แน่ใจว่าคุณได้ติดตั้ง Aspose.Cells สำหรับ .NET ในสภาพแวดล้อมการพัฒนาของคุณ ดาวน์โหลดไลบรารีจากเว็บไซต์อย่างเป็นทางการของ Aspose และตรวจสอบเอกสารประกอบเพื่อดูคำแนะนำในการติดตั้ง

## ขั้นตอนที่ 2: การเริ่มต้นสมุดงานและแผ่นงาน

ในการเริ่มต้น เราต้องสร้างเวิร์กบุคใหม่และรับการอ้างอิงไปยังเวิร์กชีทที่เราต้องการปกป้องเซลล์ ใช้รหัสต่อไปนี้:

```csharp
// พาธไปยังไดเร็กทอรีเอกสาร
string dataDir = "YOUR DOCUMENTS DIRECTORY";
// สร้างไดเร็กทอรีหากไม่มีอยู่
bool exists = System.IO.Directory.Exists(dataDir);
if (! exists)
     System.IO.Directory.CreateDirectory(dataDir);

// สร้างสมุดงานใหม่
Workbook workbook = new Workbook();

// รับแผ่นงานแรก
Worksheet sheet = workbook.Worksheets[0];
```

 ในข้อมูลโค้ดนี้ ขั้นแรกเราจะกำหนดเส้นทางไปยังไดเร็กทอรีที่จะบันทึกไฟล์ Excel ต่อไป เราจะสร้างอินสแตนซ์ใหม่ของ`Workbook` คลาสและรับการอ้างอิงไปยังแผ่นงานแรกโดยใช้`Worksheets` คุณสมบัติ.

## ขั้นตอนที่ 3: กำหนดสไตล์เซลล์

ตอนนี้เราจำเป็นต้องกำหนดสไตล์ของเซลล์ที่เราต้องการปกป้อง ใช้รหัสต่อไปนี้:

```csharp
// กำหนดวัตถุสไตล์
Styling styling;

// วนซ้ำคอลัมน์ทั้งหมดในเวิร์กชีตแล้วปลดล็อก
for (int i = 0; i <= 255; i++)
{
     style = sheet.Cells.Columns[(byte)i].Style;
     style. IsLocked = false;
     leaf.Cells.Columns[(byte)i].ApplyStyle(style, new StyleFlag { Locked = true });
}
```

 ในโค้ดนี้ เราใช้การวนซ้ำเพื่อวนซ้ำคอลัมน์ทั้งหมดในเวิร์กชีตและปลดล็อกเซลล์โดยการตั้งค่าสไตล์`IsLocked` ทรัพย์สินเพื่อ`false` . จากนั้นเราก็ใช้`ApplyStyle` วิธีการใช้สไตล์กับคอลัมน์ด้วย`StyleFlag` ตั้งค่าสถานะเพื่อล็อคเซลล์

## ขั้นตอนที่ 4: ปกป้องเซลล์เฉพาะ

ตอนนี้เราจะปกป้องเซลล์เฉพาะที่เราต้องการล็อค ใช้รหัสต่อไปนี้:

```csharp
// ล็อคสามเซลล์: A1, B1, C1
style = sheet.Cells["A1"].GetStyle();
style. IsLocked = true;
sheet.Cells["A1"].SetStyle(style);

style = sheet.Cells["B1"].GetStyle();
style. IsLocked = true;
sheet.Cells["B1"].SetStyle(style);

style = sheet.Cells["C1"].GetStyle();
style. IsLocked = true;
sheet.Cells["C1"].SetStyle(style);
```

 ในโค้ดนี้ เราได้รับสไตล์ของแต่ละเซลล์โดยใช้`GetStyle` วิธีการ แล้วเราก็ตั้งค่า`IsLocked` คุณสมบัติของสไตล์ถึง`true`เพื่อล็อคเซลล์ สุดท้าย เราจะนำสไตล์ที่อัปเดตไปใช้กับแต่ละเซลล์โดยใช้`SetStyle` วิธี.

## ขั้นตอนที่ 5: การปกป้องแผ่นงาน

ตอนนี้เราได้กำหนดเซลล์ที่จะป้องกันแล้ว เราก็สามารถป้องกันเวิร์กชีตได้ ใช้รหัสต่อไปนี้:

```csharp
// ป้องกันแผ่นงาน
leaf.Protect(ProtectionType.All);
```

 รหัสนี้ใช้`Protect` วิธีการป้องกันแผ่นงานด้วยประเภทการป้องกันที่ระบุ ในกรณีนี้`ProtectionType.All` ซึ่งปกป้องรายการทั้งหมดในเวิร์กชีต

## ขั้นตอนที่ 6: บันทึกไฟล์ Excel

สุดท้าย เราจะบันทึกไฟล์ Excel เมื่อมีการเปลี่ยนแปลง ใช้รหัสต่อไปนี้:

```csharp
// บันทึกไฟล์ Excel
workbook.Save(dataDir + "output.xls", SaveFormat.Excel97To2003);
```

 ในโค้ดนี้เราใช้`Save` วิธีการบันทึกสมุดงานในไดเร็กทอรีที่ระบุด้วย`Excel97To2003` รูปแบบ.

### ตัวอย่างซอร์สโค้ดสำหรับการป้องกันเซลล์ในแผ่นงาน Excel โดยใช้ Aspose.Cells สำหรับ .NET 
```csharp
//เส้นทางไปยังไดเร็กทอรีเอกสาร
string dataDir = "YOUR DOCUMENT DIRECTORY";
// สร้างไดเร็กทอรีหากไม่มีอยู่
bool IsExists = System.IO.Directory.Exists(dataDir);
if (!IsExists)
    System.IO.Directory.CreateDirectory(dataDir);
// สร้างสมุดงานใหม่
Workbook wb = new Workbook();
// สร้างวัตถุแผ่นงานและรับแผ่นงานแรก
Worksheet sheet = wb.Worksheets[0];
// กำหนดวัตถุสไตล์
Style style;
// กำหนดวัตถุ styleflag
StyleFlag styleflag;
// วนซ้ำคอลัมน์ทั้งหมดในแผ่นงานและปลดล็อค
for (int i = 0; i <= 255; i++)
{
    style = sheet.Cells.Columns[(byte)i].Style;
    style.IsLocked = false;
    styleflag = new StyleFlag();
    styleflag.Locked = true;
    sheet.Cells.Columns[(byte)i].ApplyStyle(style, styleflag);
}
// ล็อคสามเซลล์...เช่น A1, B1, C1
style = sheet.Cells["A1"].GetStyle();
style.IsLocked = true;
sheet.Cells["A1"].SetStyle(style);
style = sheet.Cells["B1"].GetStyle();
style.IsLocked = true;
sheet.Cells["B1"].SetStyle(style);
style = sheet.Cells["C1"].GetStyle();
style.IsLocked = true;
sheet.Cells["C1"].SetStyle(style);
// สุดท้ายนี้ ปกป้องแผ่นตอนนี้เลย
sheet.Protect(ProtectionType.All);
// บันทึกไฟล์ Excel
wb.Save(dataDir + "output.xls", SaveFormat.Excel97To2003);
```

## บทสรุป

ขอแสดงความยินดี! คุณได้เรียนรู้วิธีการปกป้องเซลล์เฉพาะในสเปรดชีต Excel โดยใช้ Aspose.Cells สำหรับ .NET ตอนนี้คุณสามารถใช้เทคนิคนี้ในโครงการของคุณเองและปรับปรุงความปลอดภัยของไฟล์ Excel ของคุณได้


### คำถามที่พบบ่อย

#### ถาม: เหตุใดฉันจึงควรใช้ Aspose.Cells สำหรับ .NET เพื่อปกป้องเซลล์ในสเปรดชีต Excel

ตอบ: Aspose.Cells for .NET เป็นไลบรารีที่มีประสิทธิภาพซึ่งช่วยให้ทำงานกับไฟล์ Excel ได้อย่างง่ายดาย มันนำเสนอคุณสมบัติขั้นสูงเพื่อปกป้องเซลล์ ระยะการปลดล็อค ฯลฯ

#### ถาม: สามารถป้องกันช่วงของเซลล์แทนแต่ละเซลล์ได้หรือไม่

 ตอบ: ได้ คุณสามารถกำหนดช่วงเซลล์เฉพาะเพื่อป้องกันโดยใช้`ApplyStyle` ด้วยวิธีการที่เหมาะสม`StyleFlag`.

#### ถาม: ฉันจะเปิดไฟล์ Excel ที่ได้รับการป้องกันหลังจากบันทึกได้อย่างไร

ตอบ: เมื่อคุณเปิดไฟล์ Excel ที่มีการป้องกัน คุณจะต้องระบุรหัสผ่านที่ระบุเมื่อป้องกันเวิร์กชีต

#### ถาม: มีการป้องกันประเภทอื่นๆ ที่ฉันสามารถนำไปใช้กับสเปรดชีต Excel ได้หรือไม่

ตอบ: ใช่ Aspose.Cells สำหรับ .NET รองรับการป้องกันหลายประเภท เช่น การป้องกันโครงสร้าง การป้องกันหน้าต่าง ฯลฯ คุณสามารถเลือกประเภทการป้องกันที่เหมาะสมได้ตามความต้องการของคุณ