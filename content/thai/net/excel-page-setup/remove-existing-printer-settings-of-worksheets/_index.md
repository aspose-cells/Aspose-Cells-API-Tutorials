---
title: ลบการตั้งค่าเครื่องพิมพ์ที่มีอยู่ของแผ่นงาน
linktitle: ลบการตั้งค่าเครื่องพิมพ์ที่มีอยู่ของแผ่นงาน
second_title: Aspose.Cells สำหรับการอ้างอิง .NET API
description: เรียนรู้วิธีลบการตั้งค่าเครื่องพิมพ์ที่มีอยู่ออกจากสเปรดชีต Excel ด้วย Aspose.Cells for .NET
type: docs
weight: 80
url: /th/net/excel-page-setup/remove-existing-printer-settings-of-worksheets/
---
ในบทช่วยสอนนี้ เราจะอธิบายวิธีการลบการตั้งค่าเครื่องพิมพ์ที่มีอยู่ออกจากเวิร์กชีตใน Excel ทีละขั้นตอนโดยใช้ Aspose.Cells for .NET เราจะใช้ซอร์สโค้ด C# เพื่อแสดงกระบวนการ

## ขั้นตอนที่ 1: การตั้งค่าสภาพแวดล้อม

ตรวจสอบให้แน่ใจว่าคุณได้ติดตั้ง Aspose.Cells สำหรับ .NET บนเครื่องของคุณแล้ว สร้างโปรเจ็กต์ใหม่ในสภาพแวดล้อมการพัฒนาที่คุณต้องการ

## ขั้นตอนที่ 2: นำเข้าไลบรารีที่จำเป็น

ในไฟล์โค้ดของคุณ ให้นำเข้าไลบรารีที่จำเป็นในการทำงานกับ Aspose.Cells นี่คือรหัสที่เกี่ยวข้อง:

```csharp
using Aspose.Cells;
```

## ขั้นตอนที่ 3: ตั้งค่าไดเร็กทอรีต้นทางและเอาต์พุต

ตั้งค่าไดเร็กทอรีต้นทางและเอาต์พุตซึ่งมีไฟล์ Excel ต้นฉบับอยู่ และตำแหน่งที่คุณต้องการบันทึกไฟล์ที่แก้ไขตามลำดับ ใช้รหัสต่อไปนี้:

```csharp
string sourceDir = "SOURCE DIRECTORY PATH";
string outputDir = "OUTPUT DIRECTORY PATH";
```

อย่าลืมระบุเส้นทางไดเร็กทอรีแบบเต็ม

## ขั้นตอนที่ 4: กำลังโหลดไฟล์ Excel ต้นฉบับ

โหลดไฟล์ Excel ต้นฉบับโดยใช้รหัสต่อไปนี้:

```csharp
Workbook wb = new Workbook(sourceDir + "fileName.xlsx");
```

ซึ่งจะโหลดไฟล์ Excel ที่ระบุลงในวัตถุสมุดงาน

## ขั้นตอนที่ 5: นำทางแผ่นงาน

วนซ้ำแผ่นงานทั้งหมดในสมุดงานโดยใช้การวนซ้ำ ใช้รหัสต่อไปนี้:

```csharp
int sheetCount = wb. Worksheets. Count;

for (int i = 0; i < sheetCount; i++)
{
     Worksheet ws = wb.Worksheets[i];
     // รหัสที่เหลือจะถูกเพิ่มในขั้นตอนถัดไป
}
```

## ขั้นตอนที่ 6: ลบการตั้งค่าเครื่องพิมพ์ที่มีอยู่

ตรวจสอบว่ามีการตั้งค่าเครื่องพิมพ์สำหรับแต่ละเวิร์กชีตหรือไม่ และลบทิ้งหากจำเป็น ใช้รหัสต่อไปนี้:

```csharp
PageSetup ps = ws.PageSetup;

if (ps.PrinterSettings != null)
{
     Console.WriteLine("Printer settings for this spreadsheet exist.");
     Console.WriteLine("Sheet name: " + ws.Name);
     Console.WriteLine("Paper size: " + ps.PaperSize);

     ps.PrinterSettings = null;

     Console.WriteLine("Printer settings for this spreadsheet have been removed by setting them to null.");
     Console.WriteLine("");
}
```

## ขั้นตอนที่ 7: บันทึกสมุดงานที่แก้ไข

บันทึกสมุดงานที่แก้ไขโดยใช้รหัสต่อไปนี้:

```csharp
wb.Save(outputDir + "modifiedFilename.xlsx");
```

วิธีนี้จะบันทึกสมุดงานที่แก้ไขไปยังไดเร็กทอรีเอาต์พุตที่ระบุ

### ตัวอย่างซอร์สโค้ดสำหรับการลบการตั้งค่าเครื่องพิมพ์ที่มีอยู่ของแผ่นงานโดยใช้ Aspose.Cells สำหรับ .NET 
```csharp
//ไดเรกทอรีต้นทาง
string sourceDir = RunExamples.Get_SourceDirectory();
//ไดเร็กทอรีเอาต์พุต
string outputDir = RunExamples.Get_OutputDirectory();
//โหลดไฟล์ Excel ซอร์ส
Workbook wb = new Workbook(sourceDir + "sampleRemoveExistingPrinterSettingsOfWorksheets.xlsx");
//รับจำนวนแผ่นงานของสมุดงาน
int sheetCount = wb.Worksheets.Count;
//ทำซ้ำทุกแผ่น
for (int i = 0; i < sheetCount; i++)
{
    //เข้าถึงแผ่นงาน i-th
    Worksheet ws = wb.Worksheets[i];
    //เข้าถึงการตั้งค่าหน้าแผ่นงาน
    PageSetup ps = ws.PageSetup;
    //ตรวจสอบว่ามีการตั้งค่าเครื่องพิมพ์สำหรับเวิร์กชีทนี้อยู่หรือไม่
    if (ps.PrinterSettings != null)
    {
        //พิมพ์ข้อความต่อไปนี้
        Console.WriteLine("PrinterSettings of this worksheet exist.");
        //พิมพ์ชื่อแผ่นงานและขนาดกระดาษ
        Console.WriteLine("Sheet Name: " + ws.Name);
        Console.WriteLine("Paper Size: " + ps.PaperSize);
        //ลบการตั้งค่าเครื่องพิมพ์โดยตั้งค่าเป็นโมฆะ
        ps.PrinterSettings = null;
        Console.WriteLine("Printer settings of this worksheet are now removed by setting it null.");
        Console.WriteLine("");
    }//ถ้า
}//สำหรับ
//บันทึกสมุดงาน
wb.Save(outputDir + "outputRemoveExistingPrinterSettingsOfWorksheets.xlsx");
```

## บทสรุป

ตอนนี้คุณได้เรียนรู้วิธีลบการตั้งค่าเครื่องพิมพ์ที่มีอยู่ออกจากเวิร์กชีตใน Excel โดยใช้ Aspose.Cells for .NET บทช่วยสอนนี้จะอธิบายให้คุณทราบทุกขั้นตอนของกระบวนการ ตั้งแต่การตั้งค่าสภาพแวดล้อมไปจนถึงการนำทางผ่านสเปรดชีตและการล้างการตั้งค่าเครื่องพิมพ์ ตอนนี้คุณสามารถใช้ความรู้นี้เพื่อจัดการการตั้งค่าเครื่องพิมพ์ในไฟล์ Excel ของคุณได้

### คำถามที่พบบ่อย

#### คำถามที่ 1: ฉันจะทราบได้อย่างไรว่าสเปรดชีตมีการตั้งค่าเครื่องพิมพ์อยู่แล้ว

 A1: คุณสามารถตรวจสอบว่ามีการตั้งค่าเครื่องพิมพ์สำหรับแผ่นงานหรือไม่โดยเข้าไปที่`PrinterSettings` ทรัพย์สินของ`PageSetup` วัตถุ. หากค่าไม่เป็นค่าว่าง แสดงว่ายังมีการตั้งค่าเครื่องพิมพ์อยู่

#### คำถามที่ 2: ฉันสามารถลบการตั้งค่าเครื่องพิมพ์สำหรับสเปรดชีตที่ระบุเท่านั้นได้หรือไม่

 A2: ได้ คุณสามารถใช้แนวทางเดียวกันเพื่อลบการตั้งค่าเครื่องพิมพ์สำหรับแผ่นงานเฉพาะโดยการเข้าถึงของแผ่นงานนั้น`PageSetup` วัตถุ.

#### คำถามที่ 3: วิธีการนี้จะลบการตั้งค่าเค้าโครงอื่นๆ ด้วยหรือไม่

A3: ไม่ วิธีการนี้จะลบเฉพาะการตั้งค่าเครื่องพิมพ์เท่านั้น การตั้งค่าเค้าโครงอื่นๆ เช่น ระยะขอบ การวางแนวกระดาษ ฯลฯ ยังคงไม่เปลี่ยนแปลง

#### คำถามที่ 4: วิธีนี้ใช้ได้กับไฟล์ Excel ทุกรูปแบบ เช่น .xls และ .xlsx หรือไม่

A4: ใช่ วิธีนี้ใช้ได้กับไฟล์ Excel ทุกรูปแบบที่ Aspose.Cells รองรับ รวมถึง .xls และ .xlsx

#### คำถามที่ 5: การเปลี่ยนแปลงการตั้งค่าเครื่องพิมพ์จะมีผลถาวรในไฟล์ Excel ที่แก้ไขหรือไม่

A5: ใช่ การเปลี่ยนแปลงการตั้งค่าเครื่องพิมพ์จะถูกบันทึกอย่างถาวรในไฟล์ Excel ที่แก้ไขแล้ว