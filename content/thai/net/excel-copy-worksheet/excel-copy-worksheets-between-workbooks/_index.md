---
title: แผ่นงานคัดลอก Excel ระหว่างสมุดงาน
linktitle: แผ่นงานคัดลอก Excel ระหว่างสมุดงาน
second_title: Aspose.Cells สำหรับการอ้างอิง .NET API
description: คัดลอกแผ่นงานระหว่างสมุดงาน Excel ได้อย่างง่ายดายโดยใช้ Aspose.Cells สำหรับ .NET
type: docs
weight: 30
url: /th/net/excel-copy-worksheet/excel-copy-worksheets-between-workbooks/
---
ในบทช่วยสอนนี้ เราจะแนะนำคุณตลอดขั้นตอนในการคัดลอกเวิร์กชีทระหว่างสมุดงาน Excel โดยใช้ไลบรารี Aspose.Cells สำหรับ .NET ทำตามคำแนะนำด้านล่างเพื่อทำภารกิจนี้ให้เสร็จสิ้น

## ขั้นตอนที่ 1: การเตรียมการ

ตรวจสอบให้แน่ใจว่าคุณได้ติดตั้ง Aspose.Cells สำหรับ .NET และสร้างโปรเจ็กต์ C# ในสภาพแวดล้อมการพัฒนาแบบรวม (IDE) ที่คุณต้องการ

## ขั้นตอนที่ 2: ตั้งค่าเส้นทางไดเรกทอรีเอกสาร

 ประกาศ ก`dataDir` ตัวแปรและเริ่มต้นด้วยเส้นทางไปยังไดเร็กทอรีเอกสารของคุณ ตัวอย่างเช่น :

```csharp
string dataDir = "YOUR_DIRECTORY_OF_DOCUMENTS";
```

 อย่าลืมเปลี่ยน`"YOUR_DOCUMENTS_DIRECTORY"` พร้อมเส้นทางจริงไปยังไดเร็กทอรีของคุณ

## ขั้นตอนที่ 3: กำหนดเส้นทางไฟล์อินพุต

 ประกาศก`InputPath` ตัวแปรและเริ่มต้นด้วยเส้นทางแบบเต็มของไฟล์ Excel ที่คุณต้องการคัดลอกสเปรดชีต ตัวอย่างเช่น :

```csharp
string InputPath = dataDir + "book1.xls";
```

 ตรวจสอบให้แน่ใจว่าคุณมีไฟล์ Excel`book1.xls` ในไดเร็กทอรีเอกสารของคุณหรือระบุชื่อไฟล์และตำแหน่งที่ถูกต้อง

## ขั้นตอนที่ 4: สร้างเวิร์กบุ๊ก Excel แรก

 ใช้`Workbook` คลาสของ Aspose.Cells เพื่อสร้างเวิร์กบุ๊ก Excel แรกและเปิดไฟล์ที่ระบุ:

```csharp
Workbook excelWorkbook0 = new Workbook(InputPath);
```

## ขั้นตอนที่ 5: สร้างเวิร์กบุ๊ก Excel ที่สอง

สร้างสมุดงาน Excel ที่สอง:

```csharp
Workbook excelWorkbook1 = new Workbook();
```

## ขั้นตอนที่ 6: คัดลอกแผ่นงานจากสมุดงานแรกไปยังสมุดงานที่สอง

 ใช้`Copy`วิธีการคัดลอกแผ่นงานแรกจากสมุดงานแรกไปยังสมุดงานที่สอง:

```csharp
excelWorkbook1.Worksheets[0].Copy(excelWorkbook0.Worksheets[0]);
```

## ขั้นตอนที่ 7: บันทึกไฟล์ Excel

บันทึกไฟล์ Excel ที่มีสเปรดชีตที่คัดลอก:

```csharp
excelWorkbook1.Save(dataDir + "Copy WorksheetsBetweenWorkbooks_out.xls");
```

อย่าลืมระบุเส้นทางและชื่อไฟล์ที่ต้องการสำหรับไฟล์เอาต์พุต

### ตัวอย่างซอร์สโค้ดสำหรับแผ่นงานคัดลอก Excel ระหว่างสมุดงานโดยใช้ Aspose.Cells สำหรับ .NET 
```csharp
//เส้นทางไปยังไดเร็กทอรีเอกสาร
string dataDir = "YOUR DOCUMENT DIRECTORY";
string InputPath = dataDir + "book1.xls";
// สร้างสมุดงาน
// เปิดไฟล์ลงในหนังสือเล่มแรก
Workbook excelWorkbook0 = new Workbook(InputPath);
// สร้างสมุดงานอื่น
Workbook excelWorkbook1 = new Workbook();
// คัดลอกแผ่นแรกของหนังสือเล่มแรกลงในหนังสือเล่มที่สอง
excelWorkbook1.Worksheets[0].Copy(excelWorkbook0.Worksheets[0]);
// บันทึกไฟล์.
excelWorkbook1.Save(dataDir + "CopyWorksheetsBetweenWorkbooks_out.xls");
```

## บทสรุป

ขอแสดงความยินดี! ตอนนี้คุณได้เรียนรู้วิธีคัดลอกแผ่นงานระหว่างสมุดงาน Excel โดยใช้ Aspose.Cells สำหรับ .NET แล้ว คุณสามารถใช้วิธีนี้ในโครงการของคุณเองเพื่อจัดการไฟล์ Excel ได้อย่างมีประสิทธิภาพ

### คำถามที่พบบ่อย

#### ถาม: จำเป็นต้องมีไลบรารีใดบ้างเพื่อใช้ Aspose.Cells สำหรับ .NET

A. หากต้องการใช้ Aspose.Cells สำหรับ .NET คุณต้องรวมไลบรารี Aspose.Cells ไว้ในโปรเจ็กต์ของคุณ ตรวจสอบให้แน่ใจว่าคุณได้อ้างอิงไลบรารีนี้อย่างถูกต้องในสภาพแวดล้อมการพัฒนาแบบรวม (IDE) ของคุณ

#### ถาม Aspose.Cells รองรับไฟล์ Excel รูปแบบอื่นๆ เช่น XLSX หรือไม่

A. ใช่ Aspose.Cells รองรับไฟล์ Excel หลากหลายรูปแบบ รวมถึง XLSX, XLS, CSV, HTML และอื่นๆ อีกมากมาย คุณสามารถจัดการรูปแบบไฟล์เหล่านี้ได้โดยใช้คุณสมบัติของ Aspose.Cells สำหรับ .NET

#### ถาม: ฉันสามารถปรับแต่งตัวเลือกเค้าโครงเมื่อคัดลอกสเปรดชีตได้หรือไม่

A.  ได้ คุณสามารถปรับแต่งตัวเลือกการตั้งค่าหน้าได้เมื่อคัดลอกสเปรดชีตโดยใช้คุณสมบัติของ`PageSetup` วัตถุ. คุณสามารถระบุส่วนหัวของหน้า ท้ายกระดาษ ระยะขอบ การวางแนว ฯลฯ