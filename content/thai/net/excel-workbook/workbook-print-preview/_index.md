---
title: ตัวอย่างก่อนพิมพ์สมุดงาน
linktitle: ตัวอย่างก่อนพิมพ์สมุดงาน
second_title: Aspose.Cells สำหรับการอ้างอิง .NET API
description: เรียนรู้วิธีสร้างตัวอย่างก่อนพิมพ์ของสมุดงานโดยใช้ Aspose.Cells for .NET
type: docs
weight: 170
url: /th/net/excel-workbook/workbook-print-preview/
---
การแสดงตัวอย่างก่อนพิมพ์สมุดงานเป็นคุณสมบัติที่สำคัญเมื่อทำงานกับไฟล์ Excel ด้วย Aspose.Cells สำหรับ .NET คุณสามารถสร้างตัวอย่างก่อนพิมพ์ได้อย่างง่ายดายโดยทำตามขั้นตอนเหล่านี้:

## ขั้นตอนที่ 1: ระบุไดเร็กทอรีต้นทาง

ขั้นแรก คุณต้องระบุไดเร็กทอรีต้นทางซึ่งมีไฟล์ Excel ที่คุณต้องการแสดงตัวอย่างอยู่ ต่อไปนี้เป็นวิธีดำเนินการ:

```csharp
// ไดเรกทอรีต้นทาง
string sourceDir = RunExamples.Get_SourceDirectory();
```

## ขั้นตอนที่ 2: โหลดสมุดงาน

จากนั้นคุณจะต้องโหลดสมุดงานสมุดงานจากไฟล์ Excel ที่ระบุ ต่อไปนี้เป็นวิธีดำเนินการ:

```csharp
// โหลดสมุดงานสมุดงาน
Workbook workbook = new Workbook(sourceDir + "Book1.xlsx");
```

## ขั้นตอนที่ 3: กำหนดค่าตัวเลือกรูปภาพและการพิมพ์

ก่อนที่จะสร้างตัวอย่างก่อนพิมพ์ คุณสามารถกำหนดค่าตัวเลือกรูปภาพและการพิมพ์ได้ตามต้องการ ในตัวอย่างนี้ เรากำลังใช้ตัวเลือกเริ่มต้น ต่อไปนี้เป็นวิธีดำเนินการ:

```csharp
// ตัวเลือกรูปภาพและการพิมพ์
ImageOrPrintOptions imgOptions = new ImageOrPrintOptions();
```

## ขั้นตอนที่ 4: สร้างตัวอย่างก่อนพิมพ์ของสมุดงาน

ตอนนี้คุณสามารถสร้างตัวอย่างก่อนพิมพ์ของสมุดงาน Workbook ได้โดยใช้คลาส WorkbookPrintingPreview ต่อไปนี้เป็นวิธีดำเนินการ:

```csharp
// ตัวอย่างก่อนพิมพ์ของสมุดงาน
WorkbookPrintingPreview preview = new WorkbookPrintingPreview(workbook, imgOptions);
Console.WriteLine("Workbook page count: " + preview.EvaluatedPageCount);
```

## ขั้นตอนที่ 5: สร้างตัวอย่างก่อนพิมพ์ของแผ่นงาน

หากคุณต้องการสร้างตัวอย่างก่อนพิมพ์ของแผ่นงานเฉพาะ คุณสามารถใช้คลาส SheetPrintingPreview นี่คือตัวอย่าง:

```csharp
// ตัวอย่างก่อนพิมพ์ของแผ่นงาน
SheetPrintingPreview preview2 = new SheetPrintingPreview(workbook.Worksheets[0], imgOptions);
Console.WriteLine("Number of worksheet pages: " + preview2.EvaluatedPageCount);
```

### ตัวอย่างซอร์สโค้ดสำหรับตัวอย่างก่อนพิมพ์สมุดงานโดยใช้ Aspose.Cells สำหรับ .NET 
```csharp
//ไดเรกทอรีต้นทาง
string sourceDir = RunExamples.Get_SourceDirectory();
Workbook workbook = new Workbook(sourceDir + "Book1.xlsx");
ImageOrPrintOptions imgOptions = new ImageOrPrintOptions();
WorkbookPrintingPreview preview = new WorkbookPrintingPreview(workbook, imgOptions);
Console.WriteLine("Workbook page count: " + preview.EvaluatedPageCount);
SheetPrintingPreview preview2 = new SheetPrintingPreview(workbook.Worksheets[0], imgOptions);
Console.WriteLine("Worksheet page count: " + preview2.EvaluatedPageCount);
Console.WriteLine("PrintPreview executed successfully.");
```

## บทสรุป

การสร้างตัวอย่างก่อนพิมพ์ของสมุดงานเป็นคุณสมบัติอันทรงพลังที่นำเสนอโดย Aspose.Cells สำหรับ .NET ด้วยการทำตามขั้นตอนข้างต้น คุณสามารถดูตัวอย่างสมุดงาน Excel และรับข้อมูลเกี่ยวกับจำนวนหน้าที่จะพิมพ์ได้อย่างง่ายดาย

### คำถามที่พบบ่อย

#### ถาม: ฉันจะระบุไดเรกทอรีต้นทางอื่นเพื่อโหลดสมุดงานของฉันได้อย่างไร
    
 ตอบ: คุณสามารถใช้`Set_SourceDirectory` วิธีการระบุไดเร็กทอรีต้นทางอื่น ตัวอย่างเช่น:`RunExamples.Set_SourceDirectory("Path_to_the_source_directory")`.

#### ถาม: ฉันสามารถปรับแต่งตัวเลือกรูปภาพและการพิมพ์เมื่อสร้างตัวอย่างก่อนพิมพ์ได้หรือไม่
    
 ตอบ: ได้ คุณสามารถปรับแต่งตัวเลือกรูปภาพและการพิมพ์ได้โดยการเปลี่ยนคุณสมบัติของ`ImageOrPrintOptions` วัตถุ. ตัวอย่างเช่น คุณสามารถตั้งค่าความละเอียดของภาพ รูปแบบไฟล์เอาต์พุต ฯลฯ

#### ถาม: เป็นไปได้ไหมที่จะสร้างตัวอย่างก่อนพิมพ์สำหรับแผ่นงานหลายแผ่นในสมุดงาน
    
ตอบ: ได้ คุณสามารถวนซ้ำแผ่นงานต่างๆ ในสมุดงาน และสร้างตัวอย่างก่อนพิมพ์สำหรับแต่ละแผ่นงานโดยใช้`SheetPrintingPreview` ระดับ.

#### ถาม: ฉันจะบันทึกตัวอย่างก่อนพิมพ์เป็นไฟล์รูปภาพหรือ PDF ได้อย่างไร
    
 ตอบ: คุณสามารถใช้ได้`ToImage` หรือ`ToPdf` วิธีการของ`WorkbookPrintingPreview` หรือ`SheetPrintingPreview` วัตถุเพื่อบันทึกตัวอย่างก่อนพิมพ์เป็นไฟล์รูปภาพหรือ PDF

#### ถาม: เมื่อสร้างตัวอย่างก่อนพิมพ์แล้ว ฉันจะทำอะไรได้บ้าง
    
ตอบ: เมื่อคุณสร้างตัวอย่างก่อนพิมพ์แล้ว คุณสามารถดูบนหน้าจอ บันทึกเป็นรูปภาพหรือไฟล์ PDF หรือใช้สำหรับการดำเนินการอื่น ๆ เช่น การส่งทางอีเมลหรือการพิมพ์
	