---
title: แผ่นงานคัดลอก Excel จากสมุดงานอื่น
linktitle: แผ่นงานคัดลอก Excel จากสมุดงานอื่น
second_title: Aspose.Cells สำหรับการอ้างอิง .NET API
description: คัดลอกแผ่นงาน Excel จากสมุดงานหนึ่งไปยังอีกสมุดงานได้อย่างง่ายดายโดยใช้ Aspose.Cells for .NET
type: docs
weight: 10
url: /th/net/excel-copy-worksheet/excel-copy-worksheet-from-other-workbook/
---
ในบทช่วยสอนนี้ เราจะแนะนำคุณตลอดขั้นตอนในการคัดลอกเวิร์กชีท Excel จากสมุดงานอื่นโดยใช้ไลบรารี Aspose.Cells สำหรับ .NET ทำตามคำแนะนำด้านล่างเพื่อทำภารกิจนี้ให้เสร็จสิ้น

## ขั้นตอนที่ 1: การเตรียมการ

ก่อนที่คุณจะเริ่มต้น ตรวจสอบให้แน่ใจว่าคุณได้ติดตั้ง Aspose.Cells สำหรับ .NET และสร้างโปรเจ็กต์ C# ในสภาพแวดล้อมการพัฒนาแบบรวม (IDE) ที่คุณต้องการ

## ขั้นตอนที่ 2: ตั้งค่าเส้นทางไดเรกทอรีเอกสาร

 ประกาศ ก`dataDir` ตัวแปรและเริ่มต้นด้วยเส้นทางไปยังไดเร็กทอรีเอกสารของคุณ ตัวอย่างเช่น :

```csharp
string dataDir = "YOUR_DIRECTORY_OF_DOCUMENTS";
```

 อย่าลืมเปลี่ยน`"YOUR_DOCUMENTS_DIRECTORY"` พร้อมเส้นทางจริงไปยังไดเร็กทอรีของคุณ

## ขั้นตอนที่ 3: สร้างสมุดงาน Excel ใหม่

 ใช้`Workbook` คลาสจาก Aspose.Cells เพื่อสร้างสมุดงาน Excel ใหม่:

```csharp
Workbook excelWorkbook0 = new Workbook();
```

## ขั้นตอนที่ 4: รับแผ่นงานแรกในสมุดงาน

นำทางไปยังแผ่นงานแรกในสมุดงานโดยใช้ดัชนี 0:

```csharp
Worksheet ws0 = excelWorkbook0.Worksheets[0];
```

## ขั้นตอนที่ 5: เพิ่มข้อมูลลงในแถวส่วนหัว (A1:A4)

 ใช้`for` วนซ้ำเพื่อเพิ่มข้อมูลลงในแถวส่วนหัว (A1:A4):

```csharp
for (int i = 0; i < 5; i++)
{
     ws0.Cells[i, 0].PutValue(string.Format("Header row {0}", i));
}
```

## ขั้นตอนที่ 6: เพิ่มข้อมูลโดยละเอียด (A5:A999)

 ใช้อันอื่น`for` วนซ้ำเพื่อเพิ่มข้อมูลโดยละเอียด (A5:A999):

```csharp
for (int i = 5; i < 1000; i++)
{
     ws0.Cells[i, 0].PutValue(string.Format("Detail row {0}", i));
}
```

## ขั้นตอนที่ 7: ตั้งค่าตัวเลือกเค้าโครง

 ตั้งค่าตัวเลือกการตั้งค่าหน้าสำหรับแผ่นงานโดยใช้`PageSetup` วัตถุ:

```csharp
PageSetup pagesetup = ws0.PageSetup;
pagesetup.PrintTitleRows = "$1:$5";
```

## ขั้นตอนที่ 8: สร้างสมุดงาน Excel อื่น

สร้างสมุดงาน Excel อื่น:

```csharp
Workbook excelWorkbook1 = new Workbook();
```

## ขั้นตอนที่ 9: รับแผ่นงานแรกจากสมุดงานที่สอง

นำทางไปยังแผ่นงานแรกในสมุดงานที่สอง:

```csharp
Worksheet ws1 = excelWorkbook1.Worksheets[0];
```

## ขั้นตอนที่ 10: ตั้งชื่อแผ่นงาน

ตั้งชื่อไฟ

เกาะการคำนวณ:

```csharp
ws1.Name = "MySheet";
```

## ขั้นตอนที่ 11: คัดลอกข้อมูลจากแผ่นงานแรกของสมุดงานแรกไปยังแผ่นงานแรกของสมุดงานที่สอง

คัดลอกข้อมูลจากแผ่นงานแรกของสมุดงานแรกไปยังแผ่นงานแรกของสมุดงานที่สอง:

```csharp
ws1.Copy(ws0);
```

## ขั้นตอนที่ 12: บันทึกไฟล์ Excel

บันทึกไฟล์ Excel:

```csharp
excelWorkbook1.Save(dataDir + "CopyWorkbookSheetToOther_out.xls");
```

อย่าลืมระบุเส้นทางและชื่อไฟล์ที่ต้องการสำหรับไฟล์เอาต์พุต

### ตัวอย่างซอร์สโค้ดสำหรับแผ่นงานคัดลอก Excel จากสมุดงานอื่นโดยใช้ Aspose.Cells สำหรับ .NET 
```csharp
//เส้นทางไปยังไดเร็กทอรีเอกสาร
string dataDir = "YOUR DOCUMENT DIRECTORY";
// สร้างสมุดงานใหม่
Workbook excelWorkbook0 = new Workbook();
// รับแผ่นงานแรกในหนังสือ
Worksheet ws0 = excelWorkbook0.Worksheets[0];
// ใส่ข้อมูลบางส่วนลงในแถวส่วนหัว (A1:A4)
for (int i = 0; i < 5; i++)
{
	ws0.Cells[i, 0].PutValue(string.Format("Header Row {0}", i));
}
// ใส่ข้อมูลรายละเอียดบางส่วน (A5:A999)
for (int i = 5; i < 1000; i++)
{
	ws0.Cells[i, 0].PutValue(string.Format("Detail Row {0}", i));
}
// กำหนดวัตถุ pagesetup ตามแผ่นงานแรก
PageSetup pagesetup = ws0.PageSetup;
// ห้าแถวแรกจะทำซ้ำในแต่ละหน้า...
// สามารถดูได้ในหน้าตัวอย่างก่อนพิมพ์
pagesetup.PrintTitleRows = "$1:$5";
// สร้างสมุดงานอื่น
Workbook excelWorkbook1 = new Workbook();
// รับแผ่นงานแรกในหนังสือ
Worksheet ws1 = excelWorkbook1.Worksheets[0];
// ตั้งชื่อแผ่นงาน
ws1.Name = "MySheet";
// คัดลอกข้อมูลจากแผ่นงานแรกของสมุดงานแรกลงใน
// แผ่นงานแรกของสมุดงานที่สอง
ws1.Copy(ws0);
// บันทึกไฟล์ Excel
excelWorkbook1.Save(dataDir + "CopyWorksheetFromWorkbookToOther_out.xls");
```

## บทสรุป

ขอแสดงความยินดี! ตอนนี้คุณได้เรียนรู้วิธีคัดลอกแผ่นงาน Excel จากสมุดงานอื่นโดยใช้ Aspose.Cells สำหรับ .NET แล้ว คุณสามารถใช้วิธีนี้ในโครงการของคุณเองเพื่อจัดการไฟล์ Excel ได้อย่างมีประสิทธิภาพ

### คำถามที่พบบ่อย

#### ถาม: จำเป็นต้องมีไลบรารีใดบ้างเพื่อใช้ Aspose.Cells สำหรับ .NET

A. หากต้องการใช้ Aspose.Cells สำหรับ .NET คุณต้องรวมไลบรารี Aspose.Cells ไว้ในโปรเจ็กต์ของคุณ ตรวจสอบให้แน่ใจว่าคุณได้อ้างอิงไลบรารีนี้อย่างถูกต้องในสภาพแวดล้อมการพัฒนาแบบรวม (IDE) ของคุณ

#### ถาม Aspose.Cells รองรับไฟล์ Excel รูปแบบอื่นๆ เช่น XLSX หรือไม่

A. ใช่ Aspose.Cells รองรับไฟล์ Excel หลากหลายรูปแบบ รวมถึง XLSX, XLS, CSV, HTML และอื่นๆ อีกมากมาย คุณสามารถจัดการรูปแบบไฟล์เหล่านี้ได้โดยใช้คุณสมบัติของ Aspose.Cells สำหรับ .NET

#### ถาม ฉันสามารถปรับแต่งตัวเลือกเค้าโครงเมื่อคัดลอกแผ่นงานได้หรือไม่

A.  ได้ คุณสามารถปรับแต่งตัวเลือกการตั้งค่าหน้ากระดาษได้เมื่อคัดลอกแผ่นงานโดยใช้คุณสมบัติของ`PageSetup` วัตถุ. คุณสามารถระบุส่วนหัวของหน้า ท้ายกระดาษ ระยะขอบ การวางแนว ฯลฯ