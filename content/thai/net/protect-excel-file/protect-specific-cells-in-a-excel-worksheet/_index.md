---
title: ปกป้องเซลล์เฉพาะในแผ่นงาน Excel
linktitle: ปกป้องเซลล์เฉพาะในแผ่นงาน Excel
second_title: Aspose.Cells สำหรับการอ้างอิง .NET API
description: เรียนรู้วิธีปกป้องเซลล์เฉพาะใน Excel ด้วย Aspose.Cells สำหรับ .NET บทช่วยสอนทีละขั้นตอนใน C#
type: docs
weight: 70
url: /th/net/protect-excel-file/protect-specific-cells-in-a-excel-worksheet/
---
ในบทช่วยสอนนี้ เราจะดูซอร์สโค้ด C# ที่ใช้ไลบรารี Aspose.Cells เพื่อปกป้องเซลล์เฉพาะในสเปรดชีต Excel เราจะอธิบายแต่ละขั้นตอนของโค้ดและอธิบายวิธีการทำงาน ปฏิบัติตามคำแนะนำอย่างระมัดระวังเพื่อให้ได้ผลลัพธ์ที่ต้องการ

## ขั้นตอนที่ 1: ข้อกำหนดเบื้องต้น

ก่อนที่คุณจะเริ่มต้น ตรวจสอบให้แน่ใจว่าคุณได้ติดตั้งไลบรารี Aspose.Cells สำหรับ .NET แล้ว คุณสามารถรับได้จากเว็บไซต์อย่างเป็นทางการของ Aspose ตรวจสอบให้แน่ใจว่าคุณมี Visual Studio เวอร์ชันล่าสุดหรือสภาพแวดล้อมการพัฒนา C# อื่น ๆ

## ขั้นตอนที่ 2: นำเข้าเนมสเปซที่จำเป็น

หากต้องการใช้ไลบรารี Aspose.Cells เราจำเป็นต้องนำเข้าเนมสเปซที่จำเป็นลงในโค้ดของเรา เพิ่มบรรทัดต่อไปนี้ที่ด้านบนของไฟล์ต้นฉบับ C# ของคุณ:

```csharp
using Aspose.Cells;
```

## ขั้นตอนที่ 3: การสร้างสมุดงาน Excel

ในขั้นตอนนี้ เราจะสร้างสมุดงาน Excel ใหม่ ใช้รหัสต่อไปนี้เพื่อสร้างสมุดงาน Excel:

```csharp
// พาธไปยังไดเร็กทอรีเอกสาร
string dataDir = "YOUR_DIRECTORY_OF_DOCUMENTS";

// สร้างสมุดงานใหม่
Workbook wb = new Workbook();
```

 อย่าลืมเปลี่ยน`"YOUR_DOCUMENTS_DIR"` ด้วยเส้นทางที่เหมาะสมไปยังไดเร็กทอรีเอกสารของคุณ

## ขั้นตอนที่ 4: การสร้างสเปรดชีต

ตอนนี้เราได้สร้างสมุดงาน Excel แล้ว มาสร้างแผ่นงานและรับแผ่นงานแรกกัน ใช้รหัสต่อไปนี้:

```csharp
// สร้างวัตถุสเปรดชีตและรับแผ่นงานแรก
Worksheet sheet = wb.Worksheets[0];
```

## ขั้นตอนที่ 5: การกำหนดสไตล์

ในขั้นตอนนี้ เราจะกำหนดสไตล์เพื่อนำไปใช้กับเซลล์ที่ต้องการ ใช้รหัสต่อไปนี้:

```csharp
// คำจำกัดความของวัตถุสไตล์
Styling styling;
```

## ขั้นตอนที่ 6: วนซ้ำเพื่อปลดล็อกคอลัมน์ทั้งหมด

ตอนนี้เราจะวนซ้ำคอลัมน์ทั้งหมดในแผ่นงานและปลดล็อค ใช้รหัสต่อไปนี้:

```csharp
// วนซ้ำคอลัมน์ทั้งหมดในแผ่นงานและปลดล็อค
for (int i = 0; i <= 255; i++)
{
     style = sheet.Cells.Columns[(byte)i].Style;
     style. IsLocked = false;
     sheet.Cells.Columns[(byte)i].ApplyStyle(style);
}
```

## ขั้นตอนที่ 7: การล็อคเซลล์เฉพาะ

ในขั้นตอนนี้ เราจะล็อคเซลล์เฉพาะ ใช้รหัสต่อไปนี้:

```csharp
//กำลังล็อคทั้งสามเซลล์... เช่น A1, B1, C1
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

## ขั้นตอนที่ 8: การปกป้องแผ่นงาน

สุดท้ายนี้ เราจะปกป้องแผ่นงานเพื่อป้องกันไม่ให้เซลล์ใดเซลล์หนึ่งถูกแก้ไข ใช้รหัสต่อไปนี้:

```csharp
// ป้องกันแผ่นงาน
sheet.Protect(ProtectionType.All);
```

## ขั้นตอนที่ 9: บันทึกไฟล์ Excel

ตอนนี้เราจะบันทึกไฟล์ Excel ที่แก้ไขแล้ว ใช้รหัสต่อไปนี้:

```csharp
// บันทึกไฟล์ Excel
wb.Save(dataDir + "output.out.xls", SaveFormat.Excel97To2003);
```

ตรวจสอบให้แน่ใจว่าได้ระบุเส้นทางที่ถูกต้องเพื่อบันทึกไฟล์ Excel ที่แก้ไข

### ซอร์สโค้ดตัวอย่างสำหรับการป้องกันเซลล์เฉพาะในแผ่นงาน Excel โดยใช้ Aspose.Cells สำหรับ .NET 
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
wb.Save(dataDir + "output.out.xls", SaveFormat.Excel97To2003);
```


## บทสรุป

ขอแสดงความยินดี! ขณะนี้คุณมีซอร์สโค้ด C# ที่ช่วยให้คุณสามารถปกป้องเซลล์เฉพาะในแผ่นงาน Excel โดยใช้ไลบรารี Aspose.Cells สำหรับ .NET คุณสามารถปรับแต่งโค้ดให้เหมาะกับความต้องการเฉพาะของคุณได้

### คำถามที่พบบ่อย (คำถามที่พบบ่อย)

#### รหัสนี้ใช้ได้กับ Excel เวอร์ชันล่าสุดหรือไม่

ใช่ รหัสนี้ใช้ได้กับ Excel เวอร์ชันล่าสุด รวมถึงไฟล์ในรูปแบบ Excel 2010 และสูงกว่า

#### ฉันสามารถปกป้องเซลล์อื่นนอกเหนือจาก A1, B1 และ C1 ได้หรือไม่

ได้ คุณสามารถแก้ไขโค้ดเพื่อล็อกเซลล์อื่นๆ ได้โดยการปรับการอ้างอิงเซลล์ในบรรทัดโค้ดที่เกี่ยวข้อง

#### ฉันจะปลดล็อคเซลล์ที่ถูกล็อคอีกครั้งได้อย่างไร?

 คุณสามารถใช้ได้`SetStyle` วิธีการด้วย`IsLocked` ตั้งค่าให้`false` เพื่อปลดล็อคเซลล์

#### ฉันสามารถเพิ่มแผ่นงานเพิ่มเติมลงในสมุดงานได้หรือไม่

 ใช่ คุณสามารถเพิ่มแผ่นงานอื่นๆ ลงในสมุดงานได้โดยใช้`Worksheets.Add()`และทำซ้ำขั้นตอนการป้องกันเซลล์สำหรับแผ่นงานแต่ละแผ่น

#### ฉันจะเปลี่ยนรูปแบบการบันทึกของไฟล์ Excel ได้อย่างไร

 คุณสามารถเปลี่ยนรูปแบบการบันทึกโดยใช้ไฟล์`SaveFormat` วิธีการที่มีรูปแบบที่ต้องการ เช่น`SaveFormat.Xlsx` สำหรับ Excel 2007 และใหม่กว่า