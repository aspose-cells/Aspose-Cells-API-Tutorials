---
title: การตั้งค่าการป้องกันขั้นสูงสำหรับแผ่นงาน Excel
linktitle: การตั้งค่าการป้องกันขั้นสูงสำหรับแผ่นงาน Excel
second_title: Aspose.Cells สำหรับการอ้างอิง .NET API
description: ปกป้องไฟล์ Excel ของคุณด้วยการตั้งค่าการป้องกันขั้นสูงด้วย Aspose.Cells สำหรับ .NET
type: docs
weight: 10
url: /th/net/excel-security/advanced-protection-settings-for-excel-worksheet/
---
ในบทช่วยสอนนี้ เราจะแนะนำคุณตลอดขั้นตอนในการตั้งค่าการป้องกันขั้นสูงสำหรับสเปรดชีต Excel โดยใช้ไลบรารี Aspose.Cells สำหรับ .NET ทำตามคำแนะนำด้านล่างเพื่อทำภารกิจนี้ให้เสร็จสิ้น

## ขั้นตอนที่ 1: การเตรียมการ

ตรวจสอบให้แน่ใจว่าคุณได้ติดตั้ง Aspose.Cells สำหรับ .NET และสร้างโปรเจ็กต์ C# ในสภาพแวดล้อมการพัฒนาแบบรวม (IDE) ที่คุณต้องการ

## ขั้นตอนที่ 2: ตั้งค่าเส้นทางไดเรกทอรีเอกสาร

 ประกาศ ก`dataDir` ตัวแปรและเริ่มต้นด้วยเส้นทางไปยังไดเร็กทอรีเอกสารของคุณ ตัวอย่างเช่น :

```csharp
string dataDir = "YOUR_DIRECTORY_OF_DOCUMENTS";
```

 อย่าลืมเปลี่ยน`"YOUR_DOCUMENTS_DIRECTORY"` พร้อมเส้นทางจริงไปยังไดเร็กทอรีของคุณ

## ขั้นตอนที่ 3: สร้างสตรีมไฟล์เพื่อเปิดไฟล์ Excel

 สร้างก`FileStream` วัตถุที่มีไฟล์ Excel ที่จะเปิด:

```csharp
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
```

 ตรวจสอบให้แน่ใจว่าคุณมีไฟล์ Excel`book1.xls` ในไดเร็กทอรีเอกสารของคุณหรือระบุชื่อไฟล์และตำแหน่งที่ถูกต้อง

## ขั้นตอนที่ 4: สร้างอินสแตนซ์ของวัตถุสมุดงานและเปิดไฟล์ Excel

 ใช้`Workbook`คลาสจาก Aspose.Cells เพื่อสร้างอินสแตนซ์ของวัตถุ Workbook และเปิดไฟล์ Excel ที่ระบุผ่านสตรีมไฟล์:

```csharp
Workbook excel = new Workbook(fstream);
```

## ขั้นตอนที่ 5: เข้าถึงแผ่นงานแรก

ไปที่แผ่นงานแรกของไฟล์ Excel:

```csharp
Worksheet worksheet = excel.Worksheets[0];
```

## ขั้นตอนที่ 6: ตั้งค่าการตั้งค่าการป้องกันแผ่นงาน

ใช้คุณสมบัติออบเจ็กต์เวิร์กชีตเพื่อตั้งค่าการป้องกันเวิร์กชีตตามต้องการ ตัวอย่างเช่น :

```csharp
worksheet.Protection.AllowDeletingColumn = false;
worksheet.Protection.AllowDeletingRow = false;
worksheet.Protection.AllowEditingContent = false;
worksheet.Protection.AllowEditingObject = false;
// ... ตั้งค่าการป้องกันอื่นๆ ตามต้องการ...
```

## ขั้นตอนที่ 7: บันทึกไฟล์ Excel ที่แก้ไข

 บันทึกไฟล์ Excel ที่แก้ไขโดยใช้นามสกุล`Save` วิธีการของวัตถุสมุดงาน:

```csharp
excel.Save(dataDir + "output.xls", SaveFormat.Excel97To2003);
```

อย่าลืมระบุเส้นทางและชื่อไฟล์ที่ต้องการสำหรับไฟล์เอาต์พุต

## ขั้นตอนที่ 8: ปิดสตรีมไฟล์

เมื่อบันทึกแล้ว ให้ปิดสตรีมไฟล์เพื่อเผยแพร่ทรัพยากรที่เกี่ยวข้องทั้งหมด:

```csharp
fstream.Close();
```
	
### ตัวอย่างซอร์สโค้ดสำหรับการตั้งค่าการป้องกันขั้นสูงสำหรับแผ่นงาน Excel โดยใช้ Aspose.Cells สำหรับ .NET 
```csharp
//เส้นทางไปยังไดเร็กทอรีเอกสาร
string dataDir = "YOUR DOCUMENT DIRECTORY";
// การสร้างสตรีมไฟล์ที่มีไฟล์ Excel ที่จะเปิด
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
// การสร้างอินสแตนซ์วัตถุสมุดงาน
// การเปิดไฟล์ Excel ผ่านการสตรีมไฟล์
Workbook excel = new Workbook(fstream);
// การเข้าถึงแผ่นงานแรกในไฟล์ Excel
Worksheet worksheet = excel.Worksheets[0];
// การจำกัดผู้ใช้ให้ลบคอลัมน์ของแผ่นงาน
worksheet.Protection.AllowDeletingColumn = false;
// การจำกัดผู้ใช้ให้ลบแถวของแผ่นงาน
worksheet.Protection.AllowDeletingRow = false;
// การจำกัดผู้ใช้ให้แก้ไขเนื้อหาของแผ่นงาน
worksheet.Protection.AllowEditingContent = false;
// การจำกัดผู้ใช้ให้แก้ไขอ็อบเจ็กต์ของเวิร์กชีต
worksheet.Protection.AllowEditingObject = false;
// การจำกัดผู้ใช้ให้แก้ไขสถานการณ์ของแผ่นงาน
worksheet.Protection.AllowEditingScenario = false;
//การจำกัดผู้ใช้ในการกรอง
worksheet.Protection.AllowFiltering = false;
// อนุญาตให้ผู้ใช้จัดรูปแบบเซลล์ของแผ่นงาน
worksheet.Protection.AllowFormattingCell = true;
// อนุญาตให้ผู้ใช้จัดรูปแบบแถวของแผ่นงาน
worksheet.Protection.AllowFormattingRow = true;
// อนุญาตให้ผู้ใช้แทรกคอลัมน์ในแผ่นงาน
worksheet.Protection.AllowFormattingColumn = true;
// อนุญาตให้ผู้ใช้แทรกไฮเปอร์ลิงก์ในแผ่นงาน
worksheet.Protection.AllowInsertingHyperlink = true;
// อนุญาตให้ผู้ใช้แทรกแถวในแผ่นงาน
worksheet.Protection.AllowInsertingRow = true;
// อนุญาตให้ผู้ใช้เลือกเซลล์ที่ถูกล็อกของแผ่นงาน
worksheet.Protection.AllowSelectingLockedCell = true;
// อนุญาตให้ผู้ใช้เลือกเซลล์ที่ปลดล็อคของแผ่นงาน
worksheet.Protection.AllowSelectingUnlockedCell = true;
// อนุญาตให้ผู้ใช้เรียงลำดับ
worksheet.Protection.AllowSorting = true;
// อนุญาตให้ผู้ใช้ใช้ตารางเดือยในแผ่นงาน
worksheet.Protection.AllowUsingPivotTable = true;
// บันทึกไฟล์ Excel ที่แก้ไข
excel.Save(dataDir + "output.xls", SaveFormat.Excel97To2003);
// การปิดสตรีมไฟล์เพื่อเพิ่มทรัพยากรทั้งหมด
fstream.Close();
```

## บทสรุป

ขอแสดงความยินดี! ตอนนี้คุณได้เรียนรู้วิธีการตั้งค่าการป้องกันขั้นสูงสำหรับสเปรดชีต Excel โดยใช้ Aspose.Cells สำหรับ .NET แล้ว ใช้ความรู้นี้เพื่อรักษาความปลอดภัยไฟล์ Excel ของคุณและจำกัดการกระทำของผู้ใช้

### คำถามที่พบบ่อย

#### ถาม: ฉันจะสร้างโปรเจ็กต์ C# ใหม่ใน IDE ของฉันได้อย่างไร

ตอบ: ขั้นตอนในการสร้างโปรเจ็กต์ C# ใหม่อาจแตกต่างกันไปขึ้นอยู่กับ IDE ที่คุณใช้ ศึกษาเอกสารประกอบของ IDE ของคุณสำหรับคำแนะนำโดยละเอียด

#### ถาม: เป็นไปได้หรือไม่ที่จะตั้งค่าการป้องกันแบบกำหนดเองนอกเหนือจากที่กล่าวไว้ในบทช่วยสอน?

ตอบ: ได้ Aspose.Cells มีการตั้งค่าการป้องกันที่หลากหลายซึ่งคุณสามารถปรับแต่งตามความต้องการเฉพาะของคุณได้ ดูเอกสารประกอบ Aspose.Cells สำหรับรายละเอียดเพิ่มเติม

#### ถาม: รูปแบบไฟล์ที่ใช้ในการบันทึกไฟล์ Excel ที่แก้ไขในโค้ดตัวอย่างคืออะไร

ตอบ: ในโค้ดตัวอย่าง ไฟล์ Excel ที่แก้ไขจะถูกบันทึกในรูปแบบ Excel 97-2003 (.xls) คุณสามารถเลือกรูปแบบอื่นที่ Aspose.Cells รองรับได้หากต้องการ

#### ถาม: ฉันจะเข้าถึงแผ่นงานอื่นในไฟล์ Excel ได้อย่างไร

 ตอบ: คุณสามารถเข้าถึงเวิร์กชีตอื่นได้โดยใช้ชื่อดัชนีหรือชีต ตัวอย่างเช่น:`Worksheet worksheet = excel.Worksheets[1];` หรือ`Worksheet worksheet = excel.Worksheets[" SheetName"];`.