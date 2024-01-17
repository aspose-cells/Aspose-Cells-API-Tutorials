---
title: การทำงานกับคุณสมบัติประเภทเนื้อหา
linktitle: การทำงานกับคุณสมบัติประเภทเนื้อหา
second_title: Aspose.Cells สำหรับการอ้างอิง .NET API
description: เรียนรู้วิธีทำงานกับคุณสมบัติประเภทเนื้อหาโดยใช้ Aspose.Cells สำหรับ .NET
type: docs
weight: 180
url: /th/net/excel-workbook/working-with-content-type-properties/
---
คุณสมบัติประเภทเนื้อหามีบทบาทสำคัญในการจัดการและจัดการไฟล์ Excel โดยใช้ไลบรารี Aspose.Cells สำหรับ .NET คุณสมบัติเหล่านี้ช่วยให้คุณสามารถกำหนดข้อมูลเมตาเพิ่มเติมสำหรับไฟล์ Excel ทำให้ง่ายต่อการจัดระเบียบและค้นหาข้อมูล ในบทช่วยสอนนี้ เราจะอธิบายทีละขั้นตอนเพื่อทำความเข้าใจและทำงานกับคุณสมบัติชนิดเนื้อหาโดยใช้โค้ด C# ตัวอย่าง

## ข้อกำหนดเบื้องต้น

ก่อนที่คุณจะเริ่มต้น ตรวจสอบให้แน่ใจว่าคุณมีสิ่งต่อไปนี้:

- ติดตั้ง Aspose.Cells สำหรับ .NET บนเครื่องพัฒนาของคุณ
- สภาพแวดล้อมการพัฒนาแบบรวม (IDE) ที่เข้ากันได้กับ C# เช่น Visual Studio

## ขั้นตอนที่ 1: การตั้งค่าสภาพแวดล้อม

ก่อนที่คุณจะเริ่มทำงานกับคุณสมบัติชนิดเนื้อหา ตรวจสอบให้แน่ใจว่าคุณได้ตั้งค่าสภาพแวดล้อมการพัฒนาของคุณด้วย Aspose.Cells สำหรับ .NET คุณสามารถเพิ่มการอ้างอิงไปยังไลบรารี Aspose.Cells ในโปรเจ็กต์ของคุณและนำเข้าเนมสเปซที่ต้องการลงในคลาสของคุณ

```csharp
using Aspose.Cells;
```

## ขั้นตอนที่ 2: การสร้างสมุดงาน Excel ใหม่

 ขั้นแรก เราจะสร้างสมุดงาน Excel ใหม่โดยใช้`Workbook`คลาสจัดทำโดย Aspose.Cells รหัสต่อไปนี้แสดงวิธีการสร้างเวิร์กบุ๊ก Excel ใหม่และจัดเก็บไว้ในไดเร็กทอรีเอาต์พุตที่ระบุ

```csharp
// ไดเรกทอรีปลายทาง
string outputDir = RunExamples.Get_OutputDirectory();

// สร้างสมุดงาน Excel ใหม่
Workbook workbook = new Workbook(FileFormatType.Xlsx);
```

## ขั้นตอนที่ 3: การเพิ่มคุณสมบัติประเภทเนื้อหา

 ตอนนี้เรามีสมุดงาน Excel แล้ว เราสามารถเพิ่มคุณสมบัติประเภทเนื้อหาได้โดยใช้`Add` วิธีการของ`ContentTypeProperties` คอลเลกชันของ`Workbook` ระดับ. แต่ละคุณสมบัติจะแสดงด้วยชื่อและค่า คุณ

  คุณยังสามารถระบุประเภทข้อมูลของคุณสมบัติได้

```csharp
// เพิ่มคุณสมบัติชนิดเนื้อหาแรก
int index = workbook.ContentTypeProperties.Add("MK31", "Simple Data");
workbook.ContentTypeProperties[index].IsNillable = false;

// เพิ่มคุณสมบัติชนิดเนื้อหาที่สอง
index = workbook.ContentTypeProperties.Add("MK32", DateTime.Now.ToString("yyyy-MM-dd'T'hh:mm:ss"), "DateTime");
workbook.ContentTypeProperties[index].IsNillable = true;
```

## ขั้นตอนที่ 4: บันทึกสมุดงาน Excel

 หลังจากเพิ่มคุณสมบัติชนิดเนื้อหาแล้ว เราสามารถบันทึกเวิร์กบุ๊ก Excel ที่มีการเปลี่ยนแปลงได้ ใช้`Save` วิธีการของ`Workbook` คลาสเพื่อระบุไดเร็กทอรีเอาต์พุตและชื่อไฟล์

```csharp
// บันทึกสมุดงาน Excel
workbook.Save(outputDir + "WorkingWithContentTypeProperties_out.xlsx");
```

### ตัวอย่างซอร์สโค้ดสำหรับการทำงานกับคุณสมบัติประเภทเนื้อหาโดยใช้ Aspose.Cells สำหรับ .NET 
```csharp
//ไดเรกทอรีต้นทาง
string outputDir = RunExamples.Get_OutputDirectory();
Workbook workbook = new Workbook(FileFormatType.Xlsx);
int index = workbook.ContentTypeProperties.Add("MK31", "Simple Data");
workbook.ContentTypeProperties[index].IsNillable = false;
index = workbook.ContentTypeProperties.Add("MK32", DateTime.Now.ToString("yyyy-MM-dd'T'hh:mm:ss"), "DateTime");
workbook.ContentTypeProperties[index].IsNillable = true;
workbook.Save(outputDir + "WorkingWithContentTypeProperties_out.xlsx");
Console.WriteLine("WorkingWithContentTypeProperties executed successfully.");
```

## บทสรุป

ขอแสดงความยินดี! คุณได้เรียนรู้วิธีทำงานกับคุณสมบัติชนิดเนื้อหาโดยใช้ Aspose.Cells สำหรับ .NET ตอนนี้คุณสามารถเพิ่มข้อมูลเมตาที่กำหนดเองลงในไฟล์ Excel ของคุณและจัดการไฟล์เหล่านั้นได้อย่างมีประสิทธิภาพมากขึ้น

### คำถามที่พบบ่อย

#### ถาม: คุณสมบัติชนิดเนื้อหาเข้ากันได้กับ Excel ทุกเวอร์ชันหรือไม่

ตอบ: ใช่ คุณสมบัติชนิดเนื้อหาเข้ากันได้กับไฟล์ Excel ที่สร้างใน Excel ทุกเวอร์ชัน

#### ถาม: ฉันสามารถแก้ไขคุณสมบัติชนิดเนื้อหาหลังจากเพิ่มลงในเวิร์กบุ๊ก Excel ได้หรือไม่

 ตอบ: ได้ คุณสามารถเปลี่ยนคุณสมบัติชนิดเนื้อหาได้ตลอดเวลาโดยไปที่`ContentTypeProperties` คอลเลกชันของ`Workbook` คลาสและการใช้วิธีการและ p คุณสมบัติที่เหมาะสม

#### ถาม: คุณสมบัติชนิดเนื้อหาได้รับการสนับสนุนเมื่อบันทึกเป็น PDF หรือไม่

ตอบ: ไม่ ไม่รองรับคุณสมบัติประเภทเนื้อหาเมื่อบันทึกเป็น PDF เป็นไฟล์ Excel โดยเฉพาะ