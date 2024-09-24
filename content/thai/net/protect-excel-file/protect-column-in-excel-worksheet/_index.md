---
title: ป้องกันคอลัมน์ในแผ่นงาน Excel
linktitle: ป้องกันคอลัมน์ในแผ่นงาน Excel
second_title: Aspose.Cells สำหรับการอ้างอิง .NET API
description: เรียนรู้วิธีป้องกันคอลัมน์เฉพาะใน Excel ด้วย Aspose.Cells for .NET รวมขั้นตอนโดยละเอียดและซอร์สโค้ด
type: docs
weight: 40
url: /th/net/protect-excel-file/protect-column-in-excel-worksheet/
---
Microsoft Excel เป็นแอปพลิเคชั่นยอดนิยมสำหรับจัดการและวิเคราะห์ข้อมูลในรูปแบบของสเปรดชีต การปกป้องข้อมูลที่ละเอียดอ่อนถือเป็นสิ่งสำคัญในการรับประกันความสมบูรณ์และการรักษาความลับของข้อมูล ในบทช่วยสอนนี้ เราจะแนะนำคุณทีละขั้นตอนในการปกป้องคอลัมน์เฉพาะในสเปรดชีต Excel โดยใช้ไลบรารี Aspose.Cells สำหรับ .NET Aspose.Cells สำหรับ .NET นำเสนอคุณสมบัติอันทรงพลังสำหรับการจัดการและการปกป้องไฟล์ Excel ทำตามขั้นตอนที่ให้ไว้เพื่อเรียนรู้วิธีปกป้องข้อมูลของคุณในคอลัมน์เฉพาะและรักษาความปลอดภัยสเปรดชีต Excel ของคุณ
## ขั้นตอนที่ 1: การตั้งค่าไดเรกทอรี

เริ่มต้นด้วยการกำหนดไดเร็กทอรีที่คุณต้องการบันทึกไฟล์ Excel ใช้รหัสต่อไปนี้:

```csharp
//เส้นทางไปยังไดเร็กทอรีเอกสาร
string dataDir = "YOUR DOCUMENTS DIRECTORY";
// สร้างไดเร็กทอรีหากไม่มีอยู่
bool exists = System.IO.Directory.Exists(dataDir);
if (! exists)
     System.IO.Directory.CreateDirectory(dataDir);
```

รหัสนี้จะตรวจสอบว่ามีไดเร็กทอรีอยู่แล้วหรือไม่ และสร้างใหม่หากไม่มี

## ขั้นตอนที่ 2: การสร้างสมุดงานใหม่

ต่อไป เราจะสร้างสมุดงาน Excel ใหม่และรับแผ่นงานแรก ใช้รหัสต่อไปนี้:

```csharp
// สร้างสมุดงานใหม่
Workbook workbook = new Workbook();
// สร้างวัตถุสเปรดชีตและรับแผ่นงานแรก
Worksheet sheet = workbook.Worksheets[0];
```

 รหัสนี้จะสร้างรหัสใหม่`Workbook` object และรับแผ่นงานแรกที่ใช้`Worksheets[0]`.

## ขั้นตอนที่ 3: ปลดล็อกคอลัมน์

เพื่อปลดล็อกคอลัมน์ทั้งหมดในเวิร์กชีต เราจะใช้การวนซ้ำเพื่อวนซ้ำคอลัมน์ทั้งหมดและใช้สไตล์การปลดล็อก ใช้รหัสต่อไปนี้:

```csharp
// ตั้งค่าวัตถุสไตล์
Styling styling;
// ตั้งค่าวัตถุ styleflag
StyleFlag flag;
// วนซ้ำคอลัมน์ทั้งหมดในเวิร์กชีตแล้วปลดล็อก
for (int i = 0; i <= 255; i++)
{
     style = sheet.Cells.Columns[(byte)i].Style;
     style. IsLocked = false;
     flag = new StyleFlag();
     flag. Locked = true;
     leaf.Cells.Columns[(byte)i].ApplyStyle(style, flag);
}
```

 โค้ดนี้จะวนซ้ำแต่ละคอลัมน์ในเวิร์กชีตและปลดล็อกสไตล์ตามการตั้งค่า`IsLocked` ถึง`false`.

## ขั้นตอนที่ 4: การล็อคคอลัมน์เฉพาะ

ตอนนี้เราจะล็อคคอลัมน์เฉพาะโดยใช้สไตล์ล็อค ใช้รหัสต่อไปนี้:

```csharp
// รับรูปแบบของคอลัมน์แรก
style = sheet.Cells.Columns[0].Style;
// ล็อคมัน.
style. IsLocked = true;
// สร้างอินสแตนซ์ของวัตถุแฟล็ก
flag = new StyleFlag();
// ตั้งค่าพารามิเตอร์การล็อค
flag. Locked = true;
// ใช้สไตล์กับคอลัมน์แรก
sheet.Cells.Columns[0].ApplyStyle(style, flag);
```

 รหัสนี้เลือกคอลัมน์แรกโดยใช้`Columns[0]` จากนั้นตั้งค่าสไตล์`IsLocked` ถึง`true` เพื่อล็อคคอลัมน์ สุดท้าย เราใช้สไตล์กับคอลัมน์แรกโดยใช้`ApplyStyle` วิธี.

## ขั้นตอนที่ 5: การปกป้องแผ่นงาน

ตอนนี้เราได้ล็อกคอลัมน์เฉพาะแล้ว เราจึงสามารถป้องกันเวิร์กชีตได้ ใช้รหัสต่อไปนี้:



```csharp
// ป้องกันแผ่นงาน
leaf.Protect(ProtectionType.All);
```

 รหัสนี้ใช้`Protect` วิธีการป้องกันแผ่นงานโดยการระบุประเภทการป้องกัน

## ขั้นตอนที่ 6: บันทึกไฟล์ Excel

สุดท้าย เราจะบันทึกไฟล์ Excel โดยใช้เส้นทางไดเร็กทอรีและชื่อไฟล์ที่ต้องการ ใช้รหัสต่อไปนี้:

```csharp
// บันทึกไฟล์ Excel
workbook.Save(dataDir + "output.out.xls", SaveFormat.Excel97To2003);
```

 รหัสนี้ใช้`Save` วิธีการของ`Workbook` วัตถุเพื่อบันทึกไฟล์ Excel ด้วยชื่อและรูปแบบไฟล์ที่ระบุ

### ตัวอย่างซอร์สโค้ดสำหรับป้องกันคอลัมน์ในแผ่นงาน Excel โดยใช้ Aspose.Cells สำหรับ .NET 
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
StyleFlag flag;
// วนซ้ำคอลัมน์ทั้งหมดในแผ่นงานและปลดล็อค
for (int i = 0; i <= 255; i++)
{
    style = sheet.Cells.Columns[(byte)i].Style;
    style.IsLocked = false;
    flag = new StyleFlag();
    flag.Locked = true;
    sheet.Cells.Columns[(byte)i].ApplyStyle(style, flag);
}
// รับรูปแบบคอลัมน์แรก
style = sheet.Cells.Columns[0].Style;
// ล็อคมัน.
style.IsLocked = true;
//ยกตัวอย่างธง
flag = new StyleFlag();
// ตั้งค่าการล็อค
flag.Locked = true;
// ใช้สไตล์กับคอลัมน์แรก
sheet.Cells.Columns[0].ApplyStyle(style, flag);
// ป้องกันแผ่น
sheet.Protect(ProtectionType.All);
// บันทึกไฟล์ Excel
wb.Save(dataDir + "output.out.xls", SaveFormat.Excel97To2003);
```

## บทสรุป

คุณได้ปฏิบัติตามบทช่วยสอนทีละขั้นตอนเพื่อปกป้องคอลัมน์ในสเปรดชีต Excel โดยใช้ Aspose.Cells สำหรับ .NET คุณได้เรียนรู้วิธีปลดล็อกคอลัมน์ทั้งหมด ล็อกคอลัมน์เฉพาะ และปกป้องเวิร์กชีตเอง ตอนนี้คุณสามารถใช้แนวคิดเหล่านี้กับโครงการของคุณเองและรักษาความปลอดภัยข้อมูล Excel ของคุณได้

## คำถามที่พบบ่อย

#### ถาม: เหตุใดการปกป้องคอลัมน์เฉพาะในสเปรดชีต Excel จึงมีความสำคัญ

ตอบ: การปกป้องคอลัมน์เฉพาะในสเปรดชีต Excel ช่วยจำกัดการเข้าถึงและการแก้ไขข้อมูลที่ละเอียดอ่อน จึงรับประกันความสมบูรณ์ของข้อมูลและการรักษาความลับ

#### ถาม: Aspose.Cells for .NET รองรับคุณสมบัติอื่นๆ ในการจัดการไฟล์ Excel หรือไม่

ตอบ: ใช่ Aspose.Cells สำหรับ .NET นำเสนอคุณสมบัติที่หลากหลาย รวมถึงการสร้าง การแก้ไข การแปลง และการรายงานไฟล์ Excel

#### ถาม: ฉันจะปลดล็อกคอลัมน์ทั้งหมดในสเปรดชีต Excel ได้อย่างไร

ตอบ: ใน Aspose.Cells สำหรับ .NET คุณสามารถใช้การวนซ้ำเพื่อวนซ้ำคอลัมน์ทั้งหมดและตั้งค่ารูปแบบการล็อกเป็น "false" เพื่อปลดล็อกคอลัมน์ทั้งหมด

#### ถาม: ฉันจะป้องกันสเปรดชีต Excel โดยใช้ Aspose.Cells for .NET ได้อย่างไร

 ตอบ: คุณสามารถใช้`Protect` วิธีการใช้ออบเจ็กต์เวิร์กชีทในการป้องกันชีตด้วยระดับการป้องกันที่แตกต่างกัน เช่น การป้องกันโครงสร้าง การป้องกันเซลล์ เป็นต้น

#### ถาม: ฉันสามารถใช้แนวคิดการป้องกันคอลัมน์เหล่านี้กับไฟล์ Excel ประเภทอื่นได้หรือไม่

ตอบ: ใช่ แนวคิดการป้องกันคอลัมน์ใน Aspose.Cells สำหรับ .NET สามารถใช้ได้กับไฟล์ Excel ทุกประเภท เช่น ไฟล์ Excel 97-2003 (.xls) และไฟล์ Excel รุ่นใหม่ (.xlsx)