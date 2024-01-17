---
title: ป้องกันแถวเฉพาะในแผ่นงาน Excel
linktitle: ป้องกันแถวเฉพาะในแผ่นงาน Excel
second_title: Aspose.Cells สำหรับการอ้างอิง .NET API
description: ปกป้องแถวเฉพาะใน Excel ด้วย Aspose.Cells สำหรับ .NET คำแนะนำทีละขั้นตอนเพื่อรักษาความปลอดภัยข้อมูลที่เป็นความลับของคุณ
type: docs
weight: 90
url: /th/net/protect-excel-file/protect-specific-row-in-excel-worksheet/
---
การปกป้องข้อมูลที่เป็นความลับในสเปรดชีต Excel ถือเป็นสิ่งสำคัญในการรับรองความปลอดภัยของข้อมูล Aspose.Cells for .NET นำเสนอโซลูชันที่มีประสิทธิภาพในการปกป้องแถวเฉพาะในสเปรดชีต Excel คู่มือนี้จะแนะนำวิธีป้องกันแถวเฉพาะในแผ่นงาน Excel โดยใช้ซอร์สโค้ด C# ที่ให้มา ทำตามขั้นตอนง่ายๆ เหล่านี้เพื่อตั้งค่าการป้องกันแถวในไฟล์ Excel ของคุณ

## ขั้นตอนที่ 1: นำเข้าไลบรารีที่จำเป็น

ในการเริ่มต้น ตรวจสอบให้แน่ใจว่าคุณได้ติดตั้ง Aspose.Cells สำหรับ .NET บนระบบของคุณแล้ว คุณต้องเพิ่มข้อมูลอ้างอิงที่เหมาะสมในโปรเจ็กต์ C# ของคุณเพื่อให้สามารถใช้ฟังก์ชันการทำงานของ Aspose.Cells ได้ นี่คือโค้ดสำหรับนำเข้าไลบรารีที่จำเป็น:

```csharp
// เพิ่มข้อมูลอ้างอิงที่จำเป็น
using Aspose.Cells;
```

## ขั้นตอนที่ 2: การสร้างสมุดงาน Excel และสเปรดชีต

หลังจากนำเข้าไลบรารีที่จำเป็นแล้ว คุณสามารถสร้างสมุดงาน Excel ใหม่และแผ่นงานใหม่ได้ ต่อไปนี้เป็นวิธีดำเนินการ:

```csharp
//เส้นทางไปยังไดเร็กทอรีเอกสาร
string dataDir = "YOUR DOCUMENTS DIRECTORY";

// สร้างไดเร็กทอรีหากไม่มีอยู่
bool IsExists = System.IO.Directory.Exists(dataDir);
if (!IsExists)
     System.IO.Directory.CreateDirectory(dataDir);

// สร้างสมุดงานใหม่
Workbook wb = new Workbook();

// สร้างวัตถุสเปรดชีตและรับแผ่นงานแรก
Worksheet sheet = wb.Worksheets[0];
```

## ขั้นตอนที่ 3: การตั้งค่าสไตล์และแฟล็กสไตล์

ตอนนี้เราจะตั้งค่าสไตล์เซลล์และแฟล็กสไตล์เพื่อปลดล็อกคอลัมน์ทั้งหมดในแผ่นงาน นี่คือรหัสที่จำเป็น:

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
     sheet.Cells.Columns[(byte)i].ApplyStyle(style, flag);
}
```

## ขั้นตอนที่ 4: ป้องกันเส้นเฉพาะ

ตอนนี้เราจะปกป้องแถวเฉพาะในแผ่นงาน เราจะล็อคแถวแรกเพื่อป้องกันการแก้ไขใดๆ มีวิธีดังนี้:

```csharp
// รับสไตล์ของบรรทัดแรก
style = sheet.Cells.Rows[0].Style;

// ล็อคมัน.
style. IsLocked = true;

//ยกตัวอย่างธง
flag = new StyleFlag();

// ตั้งค่าพารามิเตอร์การล็อค
flag. Locked = true;

// ใช้สไตล์กับบรรทัดแรก
sheet.Cells.ApplyRowStyle(0, style, flag);
```

## ขั้นตอนที่ 5: การปกป้องแผ่นงาน

สุดท้ายนี้ เราจะปกป้องแผ่นงาน Excel ทั้งหมดเพื่อป้องกันการแก้ไขโดยไม่ได้รับอนุญาต มีวิธีดังนี้:

```csharp
// ป้องกันแผ่นงาน
sheet.Protect(ProtectionType.All);
```

## ขั้นตอนที่ 6: บันทึกไฟล์ Excel ที่ได้รับการป้องกัน

เมื่อคุณปกป้องแถวที่ต้องการในเวิร์กชีท Excel เสร็จแล้ว คุณสามารถบันทึกไฟล์ Excel ที่ได้รับการป้องกันลงในระบบของคุณได้ มีวิธีดังนี้:

```csharp
// บันทึกไฟล์ Excel
wb.Save(dataDir + "output.out.xls", SaveFormat.Excel97To2003);
```

หลังจากทำตามขั้นตอนเหล่านี้ คุณจะป้องกันแถวที่ต้องการในสเปรดชีต Excel ของคุณได้สำเร็จโดยใช้ Aspose.Cells for .NET

### ซอร์สโค้ดตัวอย่างสำหรับการป้องกันแถวเฉพาะในแผ่นงาน Excel โดยใช้ Aspose.Cells สำหรับ .NET 
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
// รับสไตล์แถวแรก
style = sheet.Cells.Rows[0].Style;
// ล็อคมัน.
style.IsLocked = true;
//ยกตัวอย่างธง
flag = new StyleFlag();
// ตั้งค่าการล็อค
flag.Locked = true;
// ใช้สไตล์กับแถวแรก
sheet.Cells.ApplyRowStyle(0, style, flag);
// ป้องกันแผ่น
sheet.Protect(ProtectionType.All);
// บันทึกไฟล์ Excel
wb.Save(dataDir + "output.out.xls", SaveFormat.Excel97To2003);
```

## บทสรุป

การปกป้องข้อมูลในไฟล์ Excel ถือเป็นสิ่งสำคัญในการป้องกันการเข้าถึงโดยไม่ได้รับอนุญาตหรือการแก้ไขที่ไม่พึงประสงค์ การใช้ไลบรารี Aspose.Cells สำหรับ .NET ทำให้คุณสามารถป้องกันแถวที่ต้องการในสเปรดชีต Excel ได้อย่างง่ายดายโดยใช้ซอร์สโค้ด C# ที่ให้มา ทำตามคำแนะนำทีละขั้นตอนนี้เพื่อเพิ่มระดับการรักษาความปลอดภัยเพิ่มเติมให้กับไฟล์ Excel ของคุณ

### คำถามที่พบบ่อย

#### การป้องกันแถวเฉพาะทำงานใน Excel ทุกเวอร์ชันหรือไม่

ใช่ การป้องกันแถวเฉพาะโดยใช้ Aspose.Cells สำหรับ .NET ทำงานได้กับ Excel เวอร์ชันที่รองรับทั้งหมด

#### ฉันสามารถป้องกันแถวเฉพาะหลายแถวในสเปรดชีต Excel ได้หรือไม่

ได้ คุณสามารถป้องกันแถวเฉพาะได้หลายแถวโดยใช้วิธีการที่คล้ายกันซึ่งอธิบายไว้ในคู่มือนี้

#### ฉันจะปลดล็อคแถวเฉพาะในสเปรดชีต Excel ได้อย่างไร

 หากต้องการปลดล็อกแถวใดแถวหนึ่ง คุณต้องแก้ไขซอร์สโค้ดตามนั้นโดยใช้`IsLocked` วิธีการของ`Style` วัตถุ.